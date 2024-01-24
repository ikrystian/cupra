<script>
  import Swiper from 'swiper';
  import {onMount} from "svelte";
  import cupra1 from '../assets/slider-1.webp';
  import cupra2 from '../assets/slider-2.webp';
  import cupra3 from '../assets/slider-3.webp';
  import cupra4 from '../assets/slider-4.webp';
  import cupra5 from '../assets/slider-5.webp';

  import { Autoplay, Navigation } from 'swiper/modules'
  let slides = [];

  onMount( () => {

    slides = [
      {
        title: 'CUPRA Formentor',
        image: cupra1,
        description: 'Maksymalna prędkość: 204 KM/H Moc silnika: 150 KM',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '1439 zł',
        price: '127 800 zł',
      },
      {
        title: 'CUPRA Formentor VZ',
        image: cupra2,
        description: 'Maksymalna prędkość: 250 KM/H Moc silnika: 310 KM',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '1553 zł',
        price: '152 400 zł',
      },
      {
        title: 'CUPRA Ateca',
        image: cupra3,
        description: 'Maksymalna prędkość: 247 KM/H Moc silnika: 300 KM',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '2334 zł',
        price: '220 700 zł',
      },
      {
        title: 'Nowa CUPRA Born',
        image: cupra4,
        description: 'Akumulator 58 kWh moc do 204 KM²',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '1943 zł',
        price: '179 600 zł',
      },
      {
        title: 'Leon',
        image: cupra5,
        description: 'Maksymalna prędkość: 245 KM/H Moc silnika: 300 KM',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '1553 zł',
        price: '152 400 zł',
      },
      {
        title: 'Leon Sportstourer',
        image: cupra1,
        description: 'Maksymalna prędkość: 250 KM/H Moc silnika: 310 KM',
        leasingInfo: 'Dostępny w leasingu z 0% opłaty własnej',
        netRate: '1601 zł',
        price: '156 200  zł',
      },
    ]

    new Swiper('.swiper-container', {
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      slidesPerView: 1,
      initialSlide: 1,
      spaceBetween: 30,
      autoplay: {
        delay: 5000,
      },
      centeredSlides: true,
      breakpoints: {
        768: {
          slidesPerView: 2,
          spaceBetween: 60,
          centeredSlides: true,
        },
      },
    });
  });

  Swiper.use([Autoplay, Navigation])
</script>

<div class="slider">
  <div class="swiper-container">
    <div class="swiper-wrapper">
      {#each slides as slide}
        <div class="swiper-slide">
          <h2>{slide.title}</h2>
          <img  loading="lazy"  src={slide.image} alt="">
          <p>{slide.description}</p>
          <div class="slider__boxes">
            <div style="max-width: 140px;">
              <span>{slide.leasingInfo}</span>
            </div>
            <div>
              <span>Rata netto/mies. od*</span>
              <strong>{slide.netRate}</strong>
            </div>
            <div>
              <span>Cena brutto już od</span>
              <strong>{slide.price}</strong>
            </div>
          </div>
          <a href="#contact" class="slider__button btn btn--secondary">Umow jazdę próbna</a>
        </div>
      {/each}
    </div>
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
  </div>
</div>

<style lang="scss">
  @import 'swiper/swiper-bundle.css';

  .swiper-container {
    padding-block: 2rem;
    position: relative;
  }

  .swiper-slide {
    padding-inline: 1.2rem;
    transition: opacity 0.2s ease-in-out, fitler 0.2s ease-in-out;
    text-align: center;

    @media screen and (min-width: 768px) {
      padding: 5.4rem 2.4rem;
    }

    @media screen and (min-width: 1400px) {
      padding: 10.4rem 2.4rem;
    }

    &:not(.swiper-slide-active) {
      filter: grayscale(1) blur(2px);
    }

    img {
      margin-bottom: 3.8rem;
    }

    p {
      font-size: 1.4rem;
      line-height: 2rem;
      font-weight: 300;
      margin-bottom: 4.8rem;
    }

    h2 {
      font-weight: 400;
      text-align: center;
      font-size: 2.4rem;
      margin-bottom: 2rem;

      @media screen and (min-width: 578px) {
        font-size: 2.8rem;
      }

      @media screen and (min-width: 768px) {
        font-size: 3.2rem;
      }

      @media screen and (min-width: 1400px) {
        font-size: 4.8rem;
      }
    }
  }

  .slider {
    max-width: 100%;
    overflow: hidden;

    &__boxes {
      font-size: 1.4rem;
      line-height: 2rem;
      display: flex;
      gap: 4.8rem;
      margin-bottom: 4.8rem;
      justify-content: center;
      flex-wrap: wrap;
    }

    strong {
      font-weight: 500;
      line-height: 2.4rem;
      font-size: 2rem;
    }

    span {
      display: block;
    }

    &__button {
      display: inline-block;
    }
  }

  .swiper-button-next,
  .swiper-button-prev {
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--color-11);
    transition: opacity 0.2s ease-in-out;
    
    &:hover, &:focus {
      opacity: 0.5
    }

    &::after {
      font-size: 28px;
      color: var(--color-1);
    }
  }
</style>
