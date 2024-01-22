<script>    const navItems = ['Samochody', 'Jazda próbna', 'Oferta', 'Salony Cupra']
</script>
{#if navItems.length > 0}
    <nav>
        <ul>
            {#each navItems as item}
                <li>
                    <a href="#">
                        {item}
                        <svg xmlns="http://www.w3.org/2000/svg" height="16" width="10" viewBox="0 0 320 512">
                            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
                            <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/>
                        </svg>
                    </a>

                </li>
            {/each}
        </ul>
    </nav>
{/if}

<style lang="scss">
  @media screen and (max-width: 1170px) {
    nav {
      position: fixed;
      display: none;
      top: 70px;
      left: 0;
      right: 0;
      z-index: 2;
      background-color: #fff;
      bottom: 0;
    }

    a {
      display: flex;
      padding: 1.2rem;
      justify-content: space-between;
      align-items: center;
      gap: 1.2rem;
      padding-block: 1.6rem;
      text-decoration: none;
      color: var(--color-1);
      border-bottom: 1px solid #ccc;
      letter-spacing: 1px;

      svg {
        path {
          fill: #242221;
        }
      }
    }
  }

  @media screen and (min-width: 1171px) {
    nav {
      display: flex;
      align-items: center;

      ul {
        display: flex;
        list-style: none;
        gap: 1.6rem;

        @media screen and (min-width: 1366px) {
         gap: 3.2rem;
        }
      }

      a {
        text-decoration: none;
        color: var(--color-1);

        svg {
          display: none;
        }
      }
    }
  }

</style>
