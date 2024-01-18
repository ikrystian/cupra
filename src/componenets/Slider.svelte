<script>
    import Swiper from 'swiper';
    import {onMount} from "svelte";
    import cupra1 from '../assets/cupra-slider-2.png';
    import cupra2 from '../assets/cupra-slider-1.png';
    import cupra3 from '../assets/cupra-slider-3.png';
    let mySwiper;

    onMount(() => {
        mySwiper = new Swiper('.swiper-container', {
            slidesPerView: 1,
            spaceBetween: 0,
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
        });
    });
</script>

<div class="swiper-container">
    <div class="swiper-wrapper">
        <div class="swiper-slide">
                <h2>Leon</h2>
                <img src={cupra1} alt="">
                <p>Akumulator 58 kWh do 204 KM</p>
                <div>
                    <div>
                        <span>Doostępny w leasingu z 0% opłaty własnej</span>
                    </div>
                    <div>
                        <span>Rata netto/mies. od*</span>
                        <strong>1943 zł</strong>
                    </div>
                    <div>
                        <span>Cena brutto już od</span>
                        <strong>179 600 zł</strong>
                    </div>
                </div>
                <a href="#">Umow jazdę próbna</a>
        </div>

        <div class="swiper-slide">
            <h2>Nowa CUPRA Born</h2>
            <img src={cupra2} alt="">
            <p>Akumulator 58 kWh do 204 KM</p>
            <div>
                <div>
                    <span>Doostępny w leasingu z 0% opłaty własnej</span>
                </div>
                <div>
                    <span>Rata netto/mies. od*</span>
                    <strong>1943 zł</strong>
                </div>
                <div>
                    <span>Cena brutto już od</span>
                    <strong>179 600 zł</strong>
                </div>
            </div>
            <a href="#" class="btn btn--secondary">Umow jazdę próbna</a>
        </div>

        <div class="swiper-slide">
            <h2>Nowa CUPRA Born</h2>
            <img src={cupra3} alt="">
            <p>Akumulator 58 kWh do 204 KM</p>
            <div>
                <div>
                    <span>Doostępny w leasingu z 0% opłaty własnej</span>
                </div>
                <div>
                    <span>Rata netto/mies. od*</span>
                    <strong>1943 zł</strong>
                </div>
                <div>
                    <span>Cena brutto już od</span>
                    <strong>179 600 zł</strong>
                </div>
            </div>
            <a href="#">Umow jazdę próbna</a>
        </div>

    </div>
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>
</div>


<style lang="scss">
    @import 'swiper/swiper-bundle.css';

    .swiper-container {
        padding-block: 2rem;
    }

    .swiper-slide {
        padding-inline: 1.2rem;

        h2 {
          font-weight: 400;
          text-align: center;
          font-size: 2.4rem;
          margin-bottom: 2rem;
        }
    }
</style>
