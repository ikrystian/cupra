<script>
    import cupraList1 from "../assets/cupra-list-1.png";
    import cupraList2 from "../assets/cupra-list-2.png";
    import cupraList3 from "../assets/cupra-list-3.png";
    import cupraList4 from "../assets/cupra-list-4.png";
    import cupraList5 from "../assets/cupra-list-5.png";
</script>
<section class="section contact" id="contact">
    <div class="contact__container container">
        <span class="contact__subtitle">Jazda probna</span>
        <h2 class="contact__title">Umow się na bezpłatna jazdę próbna</h2>
    </div>

    <form class="form" action="">

        <div class="car-select">
            <div class="car-select__item">
                <img src={cupraList1} alt="">
                <span>Cupra Formentor</span>
            </div>
            <div class="car-select__item">
                <img src={cupraList2} alt="">
                <span>Cupra Leon</span>
            </div>
            <div class="car-select__item">
                <img src={cupraList3} alt="">
                <span>Cupra Leon Sportstourer</span>
            </div>
            <div class="car-select__item">
                <img src={cupraList4} alt="">
                <span>Cupra Ateca</span>
            </div>
            <div class="car-select__item">
                <img src={cupraList5} alt="">
                <span>Nowa Cupra Born</span>
            </div>
        </div>

        <div class="form__group">
            <label class="form__label" for="name">Imię *</label>
            <input type="text" id="name" class="form__input" placeholder="Imię *">
        </div>

        <div class="form__group">
            <label class="form__label" for="surname">Nazwisko (opcjonalnie)</label>
            <input type="text" id="surname" class="form__input" placeholder="Nazwisko (opcjonalnie)">
        </div>

        <div class="form__group">
            <label class="form__label" for="email">Adres e-mail*</label>
            <input type="email" id="email" class="form__input" placeholder="Adres e-mail*">
        </div>

        <div class="form__group">
            <label class="form__label" for="phone">Nr. telefonu *</label>
            <input type="tel" id="phone" class="form__input" placeholder="Nr. telefonu *">
        </div>
        <p>* Pole wymagane</p>
        <div class="form__description">
            <p>Wysłanie uzupełnionego formularza oznacza Twoją zgodę na kontakt w celu przedstawienia informacji
                handlowej w wybrany przez Ciebie sposób w związku
                <a href="#">Czytaj więcej</a>
            </p>
            <p>Prosimy Cię też o wyrażenie poniższych zgód w celu możliwości przedstawiania Ci atrakcyjnych ofert /
                promocji produktów, akcesoriów i usług marki CUPRA w przyszłości.</p>
        </div>

        <div class="form__privacy">
            <div class="fake-checkbox">
                <input type="checkbox" id="privacy1">
                <label for="privacy1"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"/></svg></label>
            </div>
            <label for="privacy1">Zgadzam się na przetwarzanie moich danych osobowych przez Plichta spółka z ograniczoną
                odpowiedzialnością Spółka Komandytowa w celu przedstawienia mi informacji marketingowych i handlowych
                dotyczących produktów i usług marki CUPRA oraz innych powiązanych z marką CUPRA akcesoriów, produktów i
                usług motoryzacyjnych za pomocą:</label>
        </div>

        <div class="form__privacy">
            <div class="fake-checkbox">
                <input type="checkbox" id="privacy2">
                <label for="privacy2"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"/></svg></label>
            </div>
            <label for="privacy2">E-mail</label>
        </div>

        <div class="form__privacy">
            <div class="fake-checkbox">
                <input type="checkbox" id="privacy3">
                <label for="privacy3"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"/></svg></label>
            </div>
            <label for="privacy3">Telefon</label>
        </div>

        <div class="form__privacy">
            <div class="fake-checkbox">
                <input type="checkbox" id="privacy4">
                <label for="privacy4"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M438.6 105.4c12.5 12.5 12.5 32.8 0 45.3l-256 256c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0L160 338.7 393.4 105.4c12.5-12.5 32.8-12.5 45.3 0z"/></svg></label>
            </div>
            <label for="privacy4">Wiadomość SMS/MMS</label>
        </div>

        <div class="form__description">
            <p>Masz prawo do wglądu, modyfikacji, ograniczenia przetwarzania i usunięcia swoich danych oraz do wycofania
                w każdym momencie swojej zgody.</p>
            <p>Twoje dane będą przetwarzane tylko w stopniu umożliwiającym realizację wymienionego celu.</p>
            <p>Administratorem Twoich danych jest Plichta spółka z ograniczoną odpowiedzialnością Spółka Komandytowa, z
                siedzibą w Wejherowie przy ulicy Gdańskiej 13c. Zapraszamy do zapoznania się z naszą polityką
                prywatności umieszczoną pod linkiem: https://www.plichta.com.pl/polityka-prywatnosci</p>
        </div>

        <div class="form__footer">
            <button class="btn btn--secondary">Umów jazdę próbną</button>
        </div>

    </form>

</section>

<style lang="scss">
  .contact {
    padding: 2rem 1.2rem;

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
      color: var(--color-1)
    }

    &__description {
      margin-top: 2.4rem;
      font-size: 1.3rem;

      p {
        margin-bottom: 2.4rem;

        a {
          color: var(--primary-color);
        }
      }
    }

    &__group {
      display: flex;
      flex-direction: column;
      margin-top: 3rem;

      label {
        font-size: 0;
      }

      input {
        border: 0;
        border-bottom: 1px solid #D5D5D5;
        color: #242221;
        padding-block: 1.2rem;
        font-size: 1.6rem;

        &:focus {
          outline: 0;
        }
      }
    }

    &__privacy {
      display: flex;
      gap: 1.2rem;
      margin-bottom: 2.4rem;
    }
  }

  .car-select {
  }

  .car-select__item {
    border: 0.1rem solid #D5D5D5;
    margin-left: 5rem;
    height: 10.5rem;
    display: flex;
    position: relative;
    align-items: center;

    &:not(:first-of-type) {
      display: none;
    }
  }

  .car-select__item span {
    white-space: nowrap;
    background-color: rgba(255, 255, 255, 0.8);
    position: absolute;
    top: 50%;
    left: 50%;
    padding: 0.4rem 0.8rem;
    transform: translateY(-50%);
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
      border: 1px solid #D5D5D5;
      cursor: pointer;

      svg {
        width: 16px;
        height: 16px;
        opacity: 0;
        transform: scale(0);
        transition: opacity 0.2s ease-in-out, transform 0.2s ease-in-out;
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
</style>
