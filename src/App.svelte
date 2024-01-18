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
    <h2>Wypróbuj</h2>
    <p>
        Zobacz, poczuj i przekonaj się, czym jest CUPRA. Poznaj
        samochody, które są wyjątkowym połączeniem technologii,
        mocy, elegancji i komfortu.
    </p>

    <div class="dark-section-gallery">
        <div class="dark-section-gallery__item">
            <figure>
                <img src={cupra1} alt="cupra 1">
                <figcaption>Design inspirowany wyścigami, stworzony z niezwykłą dbałością o detale.</figcaption>
            </figure>
        </div>
        <div class="dark-section-gallery__item">
            <figure>
                <img src={cupra2} alt="cupra 2">
                <figcaption>Podróżuj z rozmachem bez kompromisów.</figcaption>
            </figure>
        </div>
    </div>

    <!--    obrazki w gridzie-->
    <h2>Tylko dla odważnych</h2>
    <p>
        Model CUPRA, który idealnie wpisuje się DNA marki.
        Unikalny SUVm cope, wyjątkowy, odważny i innowacyjny -
        zapewni Ci to, co najlepsze w marce CUPRA.
    </p>
    <a href="#" class="btn btn--dark">Umów jazdę próbną</a>
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

<Contact />

<Footer />

<style>
    .dark-section {
        background-color: #1B1B1B;
        color: #fff;
        padding: 3rem 1.2rem;
    }

    h2 {
        font-weight: 400;
        font-size: 2.8rem;
        margin-bottom: 1.6rem;
    }

    h2 + p {
        margin-bottom: 2.2rem;
    }

    p {
        color: rgba(255, 255, 255, 0.50);
    }

    .dark-section-gallery img {
        margin-bottom: 2rem;
    }

    .dark-section-gallery figcaption {
        color: rgba(255, 255, 255, 0.50);
        margin-bottom: 3.2rem;
        display: block;
    }
</style>
