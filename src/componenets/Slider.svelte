<script>
    import Swiper from 'swiper';
    import { onMount } from "svelte";
    import cupra1 from '../assets/cupra-slider-2.png';
    import cupra2 from '../assets/cupra-slider-1.png';
    import cupra3 from '../assets/cupra-slider-3.png';

    let mySwiper;
    let slides = [];

    onMount(async () => {
        
        slides = [{
            title: 'CUPRA Ateca',
            image: cupra1,
            description: 'CUPRA Ateca to pierwszy model marki CUPRA, który łączy w sobie sportowy charakter, wyjątkowy design i funkcjonalność. To samochód, który zapewnia niezapomniane wrażenia z jazdy, a jednocześnie jest gotowy na każdą przygodę.',
            leasingInfo: 'Leasing już od 1 999 zł netto/mies.',
            netRate: '1 999 zł',
            price: '246 000 zł',
        }, {
            title: 'CUPRA Ateca',
            image: cupra1,
            description: 'CUPRA Ateca to pierwszy model marki CUPRA, który łączy w sobie sportowy charakter, wyjątkowy design i funkcjonalność. To samochód, który zapewnia niezapomniane wrażenia z jazdy, a jednocześnie jest gotowy na każdą przygodę.',
            leasingInfo: 'Leasing już od 1 999 zł netto/mies.',
            netRate: '1 999 zł',
            price: '246 000 zł',
        },
        {
            title: 'CUPRA Ateca',
            image: cupra1,
            description: 'CUPRA Ateca to pierwszy model marki CUPRA, który łączy w sobie sportowy charakter, wyjątkowy design i funkcjonalność. To samochód, który zapewnia niezapomniane wrażenia z jazdy, a jednocześnie jest gotowy na każdą przygodę.',
            leasingInfo: 'Leasing już od 1 999 zł netto/mies.',
            netRate: '1 999 zł',
            price: '246 000 zł',
        },
        {
            title: 'CUPRA Ateca',
            image: cupra1,
            description: 'CUPRA Ateca to pierwszy model marki CUPRA, który łączy w sobie sportowy charakter, wyjątkowy design i funkcjonalność. To samochód, który zapewnia niezapomniane wrażenia z jazdy, a jednocześnie jest gotowy na każdą przygodę.',
            leasingInfo: 'Leasing już od 1 999 zł netto/mies.',
            netRate: '1 999 zł',
            price: '246 000 zł',
        }]

        mySwiper = new Swiper('.swiper-container', {
            slidesPerView: 1,
            autoplay: {
                delay: 2500,
                disableOnInteraction: false,
            },
            loop: true,
            spaceBetween: 30,
            centeredSlides: true,
            breakpoints: {
                640: {
                    slidesPerView: 2,
                    spaceBetween: 30,
                    centeredSlides: true,
                },
                768: {
                    slidesPerView: 2,
                    spaceBetween: 30,
                    centeredSlides: true,
                },
            }
        });
    });
</script>

<div style="max-width: 100%; overflow: hidden;">
    <div class="swiper-container">
        <div class="swiper-wrapper">
            {#each slides as slide}
                <div class="swiper-slide">
                    <h2>{slide.title}</h2>
                    <img src={slide.image} alt="">
                    <p>{slide.description}</p>
                    <div>
                        <div>
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
                    <a href="#contact">Umow jazdę próbna</a>
                </div>
            {/each}
        </div>
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
</style>
