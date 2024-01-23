<script>
  import * as yup from "yup";
  import { Form, Message } from "svelte-yup";
  const formSubmit = () => {
    submitted = true;
    isValid = schema.isValidSync(fields);
    console.log(fields);
  };
  let openCarDropDown = false;

  let schema = yup.object().shape({
    name: yup
      .string()
      .required("Podanie imienia jest konieczne")
      .max(30)
      .label("Imię"),
    surname: yup.string().label("Nazwisko"),
    email: yup
      .string()
      .email("Podaj poprawny adres email")
      .required("Podanie adresu email jest konieczne")
      .label("E-mail"),
    phone: yup
      .string()
      .required("Podanie numeru telefonu jest konieczne")
      .label("Numer telefonu"),
  });

  let fields = {
    name: "",
    surname: "",
    email: "",
    phone: "",
    selectedCar: 1,
  };
  let submitted = false;
  let isValid;
  let carData = [
    {
      id: 1,
      name: "CUPRA Ateca",
      image: cupraList1,
      selected: true,
    },
    {
      id: 2,
      name: "CUPRA Leon",
      image: cupraList2,
      selected: false,
    },
    {
      id: 3,
      name: "CUPRA Leon Sportstourer",
      image: cupraList3,
      selected: false,
    },
    {
      id: 4,
      name: "CUPRA Formentor",
      image: cupraList4,
      selected: false,
    },
    {
      id: 5,
      name: "CUPRA Formentor VZ",
      image: cupraList5,
    },
  ];

  import cupraList1 from "../assets/cupra-list-1.png";
  import cupraList2 from "../assets/cupra-list-2.png";
  import cupraList3 from "../assets/cupra-list-3.png";
  import cupraList4 from "../assets/cupra-list-4.png";
  import cupraList5 from "../assets/cupra-list-5.png";

  const select = (id) => () => {
    carData = carData.map((car) => {
      if (car.id === id) {
        car.selected = true;
        fields.selectedCar = car.id;
      } else {
        car.selected = false;
      }
      return car;
    });

    carData.sort((a, b) => {
      if (a.selected) return -1;
      if (b.selected) return 1;
      return 0;
    });
  };
</script>

<section class="section contact" id="contact">
  <div class="contact__container container">
    <span class="contact__subtitle">Jazda próbna</span>
    <h2 class="contact__title">Umów się na bezpłatna jazdę próbną</h2>
  </div>

  {#if submitted && isValid}
    <div class="alert" role="alert">
      Wiadomość została wysłana. Dziękujemy! ❤️
    </div>
  {/if}

  <Form class="form" {schema} {fields} submitHandler={formSubmit} {submitted}>
    <button
      type="button"
      class="car-select {openCarDropDown ? 'active' : ''}"
      on:click={() => {
        openCarDropDown = !openCarDropDown;
      }}
    >
      {#each carData as car}
        <button
          class="car-select__item"
          type="button"
          data-id={car.id}
          on:click={select(car.id)}
        >
          <img src={car.image} alt="" />
          <span>{car.name}</span>
        </button>
      {/each}
    </button>

    <div class="form__group">
      <label class="form__label" for="name">Imię *</label>
      <input
        type="text"
        id="name"
        class="form__input"
        placeholder="Imię *"
        bind:value={fields.name}
      />
      <Message name="name" />
    </div>

    <div class="form__group">
      <label class="form__label" for="surname">Nazwisko (opcjonalnie)</label>
      <input
        type="text"
        id="surname"
        class="form__input"
        placeholder="Nazwisko (opcjonalnie)"
        bind:value={fields.surnamme}
      />
      <Message name="surname" />
    </div>

    <div class="form__group">
      <label class="form__label" for="email">Adres e-mail*</label>
      <input
        type="email"
        id="email"
        class="form__input"
        placeholder="Adres e-mail*"
        bind:value={fields.email}
      />
      <Message name="email" />
    </div>

    <div class="form__group">
      <label class="form__label" for="phone">Nr. telefonu *</label>
      <input
        type="tel"
        id="phone"
        class="form__input"
        placeholder="Nr. telefonu *"
        bind:value={fields.phone}
      />
      <Message name="phone" />
    </div>
    <p class="form__group">* Pole wymagane</p>
    <div class="form__description">
      <p>
        Wysłanie uzupełnionego formularza oznacza Twoją zgodę na kontakt w celu
        przedstawienia informacji handlowej w wybrany przez Ciebie sposób w
        związku
        <a href="#">Czytaj więcej</a>
      </p>
      <p>
        Prosimy Cię też o wyrażenie poniższych zgód w celu możliwości
        przedstawiania Ci atrakcyjnych ofert / promocji produktów, akcesoriów i
        usług marki CUPRA w przyszłości.
      </p>
    </div>

    <div class="form__privacy">
      <div class="fake-checkbox">
        <input type="checkbox" id="privacy1" />
        <label for="privacy1">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
            <path
              d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"
            />
          </svg>
        </label>
      </div>
      <label for="privacy1"
        >Zgadzam się na przetwarzanie moich danych osobowych przez Plichta
        spółka z ograniczoną odpowiedzialnością Spółka Komandytowa w celu
        przedstawienia mi informacji marketingowych i handlowych dotyczących
        produktów i usług marki CUPRA oraz innych powiązanych z marką CUPRA
        akcesoriów, produktów i usług motoryzacyjnych za pomocą:</label
      >
    </div>

    <div class="form__privacy">
      <div class="fake-checkbox">
        <input type="checkbox" id="privacy2" />
        <label for="privacy2">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
            <path
              d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"
            />
          </svg>
        </label>
      </div>
      <label for="privacy2">E-mail</label>
    </div>

    <div class="form__privacy">
      <div class="fake-checkbox">
        <input type="checkbox" id="privacy3" />
        <label for="privacy3">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
            <path
              d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"
            />
          </svg>
        </label>
      </div>
      <label for="privacy3">Telefon</label>
    </div>

    <div class="form__privacy">
      <div class="fake-checkbox">
        <input type="checkbox" id="privacy4" />
        <label for="privacy4">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
            <path
              d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"
            />
          </svg>
        </label>
      </div>
      <label for="privacy4">Wiadomość SMS/MMS</label>
    </div>

    <div class="form__description">
      <p>
        Masz prawo do wglądu, modyfikacji, ograniczenia przetwarzania i
        usunięcia swoich danych oraz do wycofania w każdym momencie swojej
        zgody.
      </p>
      <p>
        Twoje dane będą przetwarzane tylko w stopniu umożliwiającym realizację
        wymienionego celu.
      </p>
      <p>
        Administratorem Twoich danych jest Plichta spółka z ograniczoną
        odpowiedzialnością Spółka Komandytowa, z siedzibą w Wejherowie przy
        ulicy Gdańskiej 13c. Zapraszamy do zapoznania się z naszą polityką
        prywatności umieszczoną pod linkiem:
        https://www.plichta.com.pl/polityka-prywatnosci
      </p>
    </div>

    <div class="form__footer">
      <button class="btn btn--secondary">Umów jazdę próbną</button>
    </div>
    <input type="hidden" name="selectedCar" />
  </Form>
</section>

<style lang="scss">
  .contact {
    padding: 2rem 1.2rem;
    background-color: #f5f5f5;
    border-bottom: 1rem solid #fff;

    &__subtitle {
      text-align: center;
      display: block;
      margin-bottom: 0.4rem;
    }

    &__title {
      text-align: center;
      font-weight: 400;
      margin-bottom: 3.2rem;
    }
  }

  .form {
    ::placeholder {
      color: var(--color-1);
    }

    max-width: 100%;
    width: 670px;
    margin-inline: auto;

    &__description {
      margin-top: 2.4rem;
      font-size: 1.3rem;

      @media screen and (min-width: 578px) {
        margin-top: 2.4rem;
      }

      @media screen and (min-width: 768px) {
        margin-top: 3.6rem;
      }

      @media screen and (min-width: 1100px) {
        margin-top: 4.8rem;
      }

      p {
        margin-bottom: 2.4rem;
        font-size: 1.3rem;

        a {
          color: var(--primary-color);
        }
      }
    }

    &__group {
      display: flex;
      flex-direction: column;
      margin-top: 3rem;
      width: 553px;
      margin-inline: auto;
      max-width: 100%;

      label {
        font-size: 0;
      }

      input {
        border: 0;
        border-bottom: 1px solid #d5d5d5;
        color: #242221;
        padding-block: 1.2rem;
        font-size: 1.6rem;
        background-color: transparent;
        margin-bottom: 0.4rem;

        &:focus {
          outline: 0;
        }
      }
    }

    &__privacy {
      display: flex;
      gap: 1.2rem;
      margin-bottom: 2.4rem;
      font-size: 1.3rem;

      label {
        flex: 1 1 auto;
        cursor: pointer;
      }
    }
  }

  .car-select {
    width: 553px;
    max-width: 100%;
    border: 0;
    background-color: transparent;

    &.active {
      .car-select__item {
        &:hover {
          &::after {
            width: 1.5rem;
            opacity: 1;
          }

          img {
            transform: scale(1.1);
          }
        }
        &:not(:first-of-type) {
          display: flex;
        }

        &:first-of-type {
          &::before {
            transform: translateY(-50%) rotate(0deg);
          }
        }
      }
    }

    &__item {
      border: 0.1rem solid #d5d5d5;
      border-top: 0;
      margin-left: 5rem;
      height: 10.5rem;
      display: flex;
      width: 100%;
      background: transparent;
      position: relative;
      align-items: center;
      cursor: pointer;

      &:first-of-type {
        &::before {
          content: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M233.4 105.4c12.5-12.5 32.8-12.5 45.3 0l192 192c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L256 173.3 86.6 342.6c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3l192-192z"/></svg>');
          display: block;
          width: 16px;
          height: 16px;
          position: absolute;
          right: 2.6rem;
          top: 50%;
          transition: transform 0.2s ease-in-out;
          transform: translateY(-50%) rotate(180deg);
        }
      }

      &::after {
        content: "";
        display: block;
        position: absolute;
        right: 0;
        top: 0;
        bottom: 0;
        width: 0;
        background-color: #d5d5d5;
        opacity: 0;
        transition:
          width 0.4s ease-in-out,
          opacity 0.2s ease-in-out;
      }

      &:nth-child(1) {
        border-top: 0.1rem solid #d5d5d5;
      }

      @media screen and (min-width: 768px) {
        height: 14.5rem;
      }

      img {
        width: auto;
        height: auto;
        transition: transform 0.2s ease-in-out;
      }

      &:not(:first-of-type) {
        display: none;
      }
    }
  }

  .car-select__item span {
    white-space: nowrap;
    background-color: #f5f5f5;
    position: absolute;
    top: 50%;
    left: 50%;
    padding: 0.4rem 0.8rem;
    transform: translateY(-50%);

    @media screen and (min-width: 768px) {
      font-size: 1.6rem;
    }
  }

  .car-select__item img {
    margin-left: -50px;
    max-width: 80%;
    height: auto;
  }

  .fake-checkbox {
    label {
      width: 20px;
      height: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: #fff;
      border: 1px solid #d5d5d5;
      cursor: pointer;

      svg {
        width: 16px;
        height: 16px;
        opacity: 0;
        transform: scale(0);
        transition:
          opacity 0.2s ease-in-out,
          transform 0.2s ease-in-out;
      }
    }

    input {
      display: none;

      &:checked + label {
        svg {
          transform: scale(1);
          opacity: 1;
        }
      }
    }
  }

  .alert {
    display: block;
    margin-bottom: 2rem;
    text-align: center;
  }
</style>
