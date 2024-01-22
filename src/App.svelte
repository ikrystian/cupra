<script>
    import Header from "./componenets/Header.svelte";
    import Top from "./componenets/Top.svelte";
    import Slider from "./componenets/Slider.svelte";

    import cupra1 from "./assets/cupra-1.jpg"
    import cupra2 from "./assets/cupra-2.jpg"
    import cupra3 from "./assets/cupra-3.jpg"
    import cupra4 from "./assets/cupra-4.jpg"
    import cupra5 from "./assets/cupra-5.jpg"
    import Footer from "./componenets/Footer.svelte";
    import Contact from "./componenets/Contact.svelte";
</script>
<Header/>
<Top/>

<section class="dark-section">
    <div class="container">
        <h2>Wypróbuj</h2>
        <p>
            Zobacz, poczuj i przekonaj się, czym jest CUPRA. Poznaj
            samochody, które są wyjątkowym połączeniem technologii,
            mocy, elegancji i komfortu.
        </p>

        <div class="dark-section-gallery">
            <div class="dark-section-gallery__item">
                <figure>
                    <div>
                        <img src={cupra1} alt="cupra 1">
                    </div>
                    <figcaption>Design inspirowany wyścigami, stworzony z niezwykłą dbałością o detale.</figcaption>
                </figure>
            </div>
            <div class="dark-section-gallery__item">
                <figure>
                    <div>
                        <img src={cupra2} alt="cupra 2">
                    </div>
                    <figcaption>Podróżuj z rozmachem bez kompromisów.</figcaption>
                </figure>
            </div>
        </div>

        <!--    obrazki w gridzie-->
        <h3>Tylko dla odważnych</h3>
        <p>
            Model CUPRA, który idealnie wpisuje się DNA marki.
            Unikalny SUVm cope, wyjątkowy, odważny i innowacyjny -
            zapewni Ci to, co najlepsze w marce CUPRA.
        </p>
        <a href="#" class="btn btn--dark">Umów jazdę próbną</a>
    </div>
</section>

<section>
    <Slider/>
</section>

<section class="dark-section">
    <div class="">
        <figure>
            <img src={cupra3} alt="">
        </figure>
        <div>
            <span>Technologia</span>
            <h2>Poczuj pełna wolność jazdy dzieki licznym innowacjom.</h2>
            <a href="#" class="btn btn--primary">Umów jazdę próbną</a>
        </div>
    </div>
    <div class="">
        <figure>
            <img src={cupra4} alt="">
        </figure>
        <div>
            <span>Potęga Designu</span>
            <h2>Crossover emanujący gracją, dynamizmem i czystym wyrafinowaniem.</h2>
            <a href="#" class="btn btn--primary">Umów jazdę próbną</a>
        </div>
    </div>
    <div class="">
        <figure>
            <img src={cupra4} alt="">
        </figure>
        <div>
            <span>Design wnętrza</span>
            <h2>Idealny komfort. Unikalny wystrój wnętrza stworzony w stylu CUPRY.</h2>
            <a href="#" class="btn btn--primary">Umów jazdę próbną</a>
        </div>
    </div>
</section>

<Contact/>

<Footer/>

<style lang="scss">
  .dark-section {
    background-color: #1B1B1B;
    color: #fff;
    padding: 3rem 1.2rem;

    @media screen and (min-width: 768px) {
      padding: 5% 2.4rem
    }
  }

  h2, h3 {
    font-weight: 300;
    font-size: 2.8rem;
    margin-bottom: 1.6rem;
    text-transform: uppercase;

    @media screen and (min-width: 768px) {
      font-size: 3.6rem;
      max-width: 553px;
    }

    @media screen and (min-width: 1100px) {
      font-size: 4.8rem;
    }

    @media screen and (min-width: 1400px) {
      font-size: 6rem;
    }

    + p {
      margin-bottom: 2.2rem;

      @media screen and (min-width: 768px) {
        margin-bottom: 3.6rem;
        max-width: 553px;
      }

      @media screen and (min-width: 1100px) {
        margin-bottom: 4.8rem;
      }

      @media screen and (min-width: 1400px) {
        margin-bottom: 6.8rem;
      }

    }
  }

  h3 {
    @media screen and (min-width: 1400px) {
      font-size: 4.8rem;
      margin-top: -20rem;
    }

    + p {
      @media screen and (min-width: 1400px) {
        margin-bottom: 3.2rem;
      }
    }
  }

  p {
    color: rgba(255, 255, 255, 0.50);
    font-size: 2rem;

  }


  .dark-section-gallery {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 2rem;
    margin-bottom: 3.2rem;

    @media screen and (min-width: 768px) {
      grid-template-columns: 2fr 1fr;
    }

    @media screen and (min-width: 1400px) {
      grid-template-columns: 787px 553px;
    }


    img {
      @media screen and (min-width: 768px) {
        position: absolute;
        top: 0;
        left: 0;
        max-width: 100%;
        max-height: 100%;
        object-fit: cover;
        transition: transform 3s ease-in-out;

        &:hover {
          transform: scale(1.1)
        }
      }
    }

    figcaption {
      margin-top: 2rem;

      @media screen and (min-width: 1100px) {
        margin-top: 3.2rem;
      }
    }

    &__item {
      &:nth-child(1) {
        figure > div {
          @media screen and (min-width: 768px) {
            position: relative;
            aspect-ratio: 787 / 519;
            overflow: hidden;
          }
        }
      }


      &:nth-child(2) {
        figure > div {
          @media screen and (min-width: 768px) {
            margin-top: 6rem;
            position: relative;
            aspect-ratio: 553 / 792;
            overflow: hidden;
          }
        }
      }
    }
  }

  .dark-section-gallery figcaption {
    color: rgba(255, 255, 255, 0.50);
    margin-bottom: 3.2rem;
    display: block;
  }
</style>
