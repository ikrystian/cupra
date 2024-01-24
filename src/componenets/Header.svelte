<script>
    import Nav from "./Nav.svelte";

    let showNav = false;

    const toggleMenu = () => {
        showNav = !showNav;
    }
</script>

<header class="header">
    <div class="header__container container">
    <a href="/" class="logo-link">
        <svg class="logo" id="MARCA_POSITIVO_P2718" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 692.95 99.21">
            <defs>
                <style>.cls-1 {
                    fill-rule: evenodd;
                }
                </style>
            </defs>
            <title>AF_01_IMAGOTYPE_LANDSCAPE_RGB_PITCH-BLACK</title>
            <path d="M176.64,268.49l-20.95,10.25h0l12.77,4.9c2.63,1,5.76,2.29,6.91,5.4s-.56,6-2.09,8.45l-7,10.92q-12.41,19.43-24.84,38.83,0-6,0-12h0q4.76-15,9.26-30,1.27-4.28,2.52-8.56c.5-1.72.18-2.75-1.48-3.57L139,286.84l-12.69,6.26c-1.66.82-2,1.85-1.48,3.57q1.24,4.29,2.52,8.56,4.48,15.06,9.26,30h0q0,6,0,12-12.45-19.4-24.84-38.83l-7-10.92c-1.54-2.41-3.27-5.26-2.09-8.45s4.28-4.39,6.91-5.4l12.77-4.9h0l-20.95-10.25h0l6.53,10.95-10.8,4.15Q85.79,265.81,74.47,248c21.5,7.62,43,15.31,64.56,22.68,21.59-7.37,43.06-15.05,64.56-22.68q-11.3,17.79-22.66,35.54l-10.8-4.15,6.53-10.95"
                  transform="translate(-74.47 -248.03)"/>
            <path class="cls-1"
                  d="M587.22,284.19v11.23H647.6a2.24,2.24,0,0,0,2.32-2.14v-6.94a2.24,2.24,0,0,0-2.32-2.14ZM572,321.53l0-47.82h78.28c7.27,0,13.17,4.45,13.17,11.18v9.89c0,6.91-4.6,11.59-9.26,11.59l10.42,15.18h-17l-9-14.58H587.22v14.58Z"
                  transform="translate(-74.47 -248.03)"/>
            <path d="M352,321.56H273.72c-7.27,0-13.17-5.46-13.17-12.19V285.91c0-6.73,5.9-12.19,13.17-12.19H352v13.09H276.35A2.24,2.24,0,0,0,274,289v17.37a2.24,2.24,0,0,0,2.32,2.14H352Zm103.85-47.85v35.66c0,6.73-5.9,12.19-13.17,12.19H377.46c-7.27,0-13.17-5.46-13.17-12.19V273.72H380v32.61a2.23,2.23,0,0,0,2.32,2.14H437.8a2.24,2.24,0,0,0,2.32-2.14V273.72Zm296.77,21.67v-11.2H692.86a2.24,2.24,0,0,0-2.32,2.14v9C690.54,295.22,731.29,295.33,752.62,295.38Zm14.8,26.18h-14.8V307h-62v14.58h-14.8l-.13-35.66c0-6.73,5.9-12.19,13.17-12.19h78.28c.14.1.22.05.23,0ZM482.83,295.42h61.08a2.24,2.24,0,0,0,2.32-2.14v-6.94a2.24,2.24,0,0,0-2.32-2.14H482.83Zm63.71-21.7c9.67,0,13.17,4.45,13.17,11.18v9.89c0,6.73-3,12.19-13.17,12.19H482.83v14.58H468V273.72Z"
                  transform="translate(-74.47 -248.03)"/>
        </svg>
    </a>
    <Nav {showNav} />

    <div class="header__nav-content">
        <a href="tel:+48585066565" class="btn btn--secondary btn--icon phone-button" title="+48 58 506 65 65">
            <svg xmlns="http://www.w3.org/2000/svg" height="16" width="16" viewBox="0 0 512 512">
                <path d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"/>
            </svg>
        </a>
        <a class="header__phone" href="tel:+48 585066565">+48 58 506 65 65</a>
        <div class="header__buttons">
            <a href="#" class="btn btn--primary">Zapytaj o ofertę</a>
            <a href="#contact" class="btn btn--secondary">Umów na jazdę próbną</a>
        </div>
        <button class="btn btn--primary mobile-nav-button btn--icon" on:click={toggleMenu} title="Toggle menu">
            <svg xmlns="http://www.w3.org/2000/svg" height="16" width="14" viewBox="0 0 448 512">
                <path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/>
            </svg>
        </button>
    </div>
    </div>
</header>

<style lang="scss">
  .header {
    position: fixed;
    z-index: 4;
    left: 0;
    right: 0;

    gap: 1.2rem;
    background-color: #F5F5F5;

    &__container {
      padding: 1.98rem 1.2rem;
      display: flex;
      justify-content: space-between;
    }

    &__buttons {
      display: none;

      @media screen and (min-width: 678px) {
        display: flex;
        align-items: center;
        gap: 1.2rem;
      }
    }

    &__nav-content {
      display: flex;
      gap: 1.6rem;
      align-items: center;
      flex: 1 1 auto;
      justify-content: flex-end;

      @media screen and (min-width: 1230px) {
        flex: unset;
        gap: 4.8rem;
      }
    }

    &__phone {
      display: none;

      @media screen and (min-width: 810px) {
        display: block;
        color: var(--color-1);
        text-decoration: none;
      }
    }
  }

  .phone-button {
    @media screen and (min-width: 810px) {
      display: none;
    }
  }

  .logo-link {
    display: flex;
  }

  .logo {
    min-width: 18.2rem
  }

  .mobile-nav-button {
    @media screen and (min-width: 1230px) {
        display: none;
    }
  }
</style>
