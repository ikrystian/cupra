<script>
    import Top from '../assets/top.webp'
</script>
<section class="top">
    <img loading="lazy" src={Top} alt="">
    <div class="container">
        <div>
            <h2><span>Cupra</span> Formentor</h2>
            <h1>Wejdź do świata Cupra. Poznaj prawdziwą moc i&nbsp;sportowego ducha marki.</h1>
            <a class="btn btn--dark" href="#contact">Ruszaj na jazdę testową</a>
        </div>
    </div>
</section>


<style lang="scss">
  .top {
    height: 60dvh;
    max-height: 400px;
    max-width: 100%;
    position: relative;
    padding: 5% 1.2rem;
    display: flex;
    align-items: flex-end;
    z-index: 2;
    background-color: #093E52;
    box-shadow: 0 0 72px 0 rgba(0, 0, 0, 1);

    @media (min-width: 768px) {
      padding: 5% 2.4rem;
      max-height: 600px;
    }

    @media screen and (min-width: 1400px) {
      height: 100dvh;
      max-height: 100dvh;
    }

    > div {
      position: relative;
      color: var(--color-11);

      > div {
        @media (min-width: 768px) {
          max-width: 742px;
        }
      }

      h2 {
        font-weight: 300;
        color: rgba(255, 255, 255, 0.50);
        font-size: 2rem;
        line-height: 1.2;

        @media (min-width: 768px) {
          line-height: 2.4rem;
        }

        span {
          text-transform: uppercase;
        }
      }

      h1 {
        font-weight: 300;
        font-size: 2.8rem;
        margin-bottom: 2.4rem;
        text-wrap: balance;

        @media (min-width: 768px) {
          font-size: 4.8rem;
          margin-bottom: 3.6rem;
        }

        @media (min-width: 1400px) {
          font-size: 6rem;
          margin-bottom: 4.8rem;
        }
      }
    }

    img {
      width: 100%;
      height: 100%;
      max-width: 100%;
      max-height: 100%;
      left: 0;
      top: 0;
      object-fit: cover;
      position: absolute;
      object-position: right;
    }
  }
</style>
