<script>
    import Header from "./componenets/Header.svelte";
    import Top from "./componenets/Top.svelte";
    import Slider from "./componenets/Slider.svelte";

    import cupra1 from "./assets/cupra-1.webp"
    import cupra2 from "./assets/cupra-2.webp"
    import cupra3 from "./assets/cupra-3.webp"
    import cupra4 from "./assets/cupra-4.webp"
    import cupra5 from "./assets/cupra-5.webp"
    import Footer from "./componenets/Footer.svelte";
    import Contact from "./componenets/Contact.svelte";
</script>
<Header/>
<Top/>

<section class="dark-section try-it">
    <div class="container try-it__container">
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
                        <img loading="lazy" src={cupra1} alt="cupra 1">
                    </div>
                    <figcaption>Design inspirowany wyścigami, stworzony z niezwykłą dbałością o detale.</figcaption>
                </figure>
            </div>
            <div class="dark-section-gallery__item">
                <figure>
                    <div>
                        <img loading="lazy" src={cupra2} alt="cupra 2">
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
        <a href="#contact" class="btn btn--dark">Umów jazdę próbną</a>
    </div>
</section>

<section>
    <Slider/>
</section>

<section class="dark-section ">
    <div class="container">
        <div class="dark-section__row ">
            <figure>
                <img loading="lazy" src={cupra3} alt="">
            </figure>
            <div class="dark-section__content-box">
                <span>Technologia</span>
                <h2>Poczuj pełna wolność jazdy dzieki licznym innowacjom.</h2>
                <a href="#contact" class="btn btn--darker">Umów jazdę próbną</a>
            </div>
        </div>
        <div class="dark-section__row">
            <figure>
                <img loading="lazy" src={cupra4} alt="">
            </figure>
            <div class="dark-section__content-box">
                <span>Potęga Designu</span>
                <h2>Crossover emanujący gracją, dynamizmem i czystym wyrafinowaniem.</h2>
                <a href="#contact" class="btn btn--darker">Umów jazdę próbną</a>
            </div>
        </div>
        <div class="dark-section__row">
            <figure>
                <img loading="lazy" src={cupra5} alt="">
            </figure>
            <div class="dark-section__content-box">
                <span>Design wnętrza</span>
                <h2>Idealny komfort. Unikalny wystrój wnętrza stworzony w stylu CUPRY.</h2>
                <a href="#contact" class="btn btn--darker">Umów jazdę próbną</a>
            </div>
        </div>
    </div>
</section>

<Contact/>

<Footer/>

<style lang="scss">
  .dark-section {
    background-color: var(--color-3);
    color: var(--color-11);
    padding: 3rem 1.2rem;

    @media screen and (min-width: 768px) {
      padding: 5% 2.4rem
    }

    &__row {
      position: relative;
      margin-bottom: 2rem;

      //@media screen and (min-width: 768px) {
      //  display: grid;
      //  grid-template-columns: 1fr 1fr;
      //  grid-gap: 2rem;
      //  align-items: center;
      //  margin-bottom: 5rem;
      //}

      @media screen and (min-width: 1100px) {
        display: flex;
        gap: 1.2rem;
        margin-bottom: 7.5rem;
      }
      @media screen and (min-width: 1400px) {
        margin-bottom: 15rem;
      }

      &:nth-child(even) {
        @media screen and (min-width: 1100px) {
          flex-direction: row-reverse;

          .dark-section__content-box {
            left: 0;
            right: auto;
          }
        }
      }

      figure {
        position: relative;
        display: block;
        overflow: hidden;
        margin-bottom: 2rem;

        @media screen and (min-width: 1100px) {
          width: 787px;
          margin-bottom: 0;
        }
      }
    }

    &__content-box {
      @media screen and (min-width: 1100px) {
        position: absolute;
        right: 0;
        top: 0;
        width: 670px;
        background-color: var(--color-3);
        padding-inline: 11.7rem;
        padding-bottom: 6.4rem;
      }

      span {
        display: block;
        margin-bottom: 0.8rem;
      }

      h2 {
        font-size: 2rem;
        text-transform: none;
        margin-bottom: 1.6rem;

        @media screen and (min-width: 1100px) {
          margin-bottom: 2.4rem;
        }

        @media screen and (min-width: 1100px) {
          font-size: 3.9rem;
          line-height: 4.6rem;
          margin-bottom: 3.6rem;
        }
      }
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
        transition: transform 2s ease-in-out;
      }
    }

    figcaption {
      margin-top: 2rem;

      @media screen and (min-width: 1100px) {
        margin-top: 3.2rem;
      }
    }

    &__item {
      figure > div {
        position: relative;

        &::after {
          content: '';
          position: absolute;
          left: 2rem;
          top: 2rem;
          right: 2rem;
          bottom: 2rem;
          border: 5px solid rgba(255, 255, 255, 0.4);
          transform: scale(0.8);
          opacity: 0;
          transition: transform 0.2s ease-in-out, opacity 0.2s ease-in-out;
        }

        &:hover {
          &::after {
            opacity: 1;
            transform: scale(1)
          }

          img {
            transform: scale(1.1)
          }
        }
      }


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

  .try-it {
    @media screen and (min-width: 1400px) {
      height: 300vh;
      margin-top: -100dvh;
      z-index: 1;
    }

    &__container {
      @media screen and (min-width: 1400px) {
        position: sticky;
        top: 90px;
        min-height: 100dvh;
      }
    }
  }
</style>
