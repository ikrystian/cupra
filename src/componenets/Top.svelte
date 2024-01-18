<script lang="ts">
    import Top from '../assets/top.png'
</script>
<section class="top">
    <img src={Top} alt="">
    <div>
        <h2><span>Cupra Formentor</span></h2>
        <h1>Wejdź do świata Cupra. Poznaj prawdziwą moc i&nbsp;sportowego ducha marki</h1>
        <a class="btn" href="#">Ruszaj na jazdę testową</a>
    </div>
</section>


<style lang="scss">
  .top {
    height: 60dvh;
    max-height: 400px;
    max-width: 100%;
    position: relative;
    padding: 5%;
    display: flex;
    align-items: flex-end;
    > div {
      position: relative;
      color: #fff;

      h2 {
        text-transform: uppercase;
        font-weight: 400;
        opacity: 50%;
        font-size: 2rem;
        line-height: 1.2;
      }

      h1 {
        font-weight: 400;
        font-size: 2.8rem;
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
