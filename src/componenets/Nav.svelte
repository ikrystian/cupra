<script>
  const navItems = ["Samochody", "Jazda próbna", "Oferta", "Salony Cupra"];
  export let showNav;
</script>

{#if navItems.length > 0}
  <nav class:active={showNav}>
    <ul>
      {#each navItems as item}
        <li>
          <a href="#contact">
            {item}
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="16"
              width="10"
              viewBox="0 0 320 512"
            >
              <path
                d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"
              />
            </svg>
          </a>
        </li>
      {/each}
    </ul>
    <div class="mobile-menu-buttons">
      <a href="#contact" class="btn btn--primary">Zapytaj o ofertę</a>
      <a href="#contact" class="btn btn--secondary">Umów na jazdę próbną</a>
    </div>
  </nav>
{/if}

<style lang="scss">
  @media screen and (max-width: 1230px) {
    nav {
      position: fixed;
      display: none;
      top: 70px;
      left: 0;
      right: 0;
      z-index: 2;
      background-color: var(--color-11);
      bottom: 0;

      
      &.active {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      .mobile-menu-buttons {
        display: flex;
        gap: 1.2rem;
        flex-wrap: wrap;
        margin: 1.2rem;

        a {
          justify-content: center;
          flex: 1 1 auto;

          &.btn--primary {
            border: 1px solid var(--color-12);
          }

          &.btn--secondary {
            color: var(--color-11);
          }
        }
      }
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
          fill: var(--color-1);
        }
      }
    }
  }

  @media screen and (min-width: 768px) {
    nav .mobile-menu-buttons {
      display: none;
    }
  }

  @media screen and (min-width: 1230px) {
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
        position: relative;
        padding: 10px;
        display: inline-flex;
        overflow: hidden;

        &::before,
        &::after {
          content: "";
          position: absolute;
          transition: transform 0.5s ease;
          left: 0;
          opacity: 0.2;
          width: 100%;
          height: 1px;
          background: var(--color-1);
        }

        &::before {
          bottom: 0;
          transform: translateX(-100%);
        }

        &::after {
          top: 0;
          transform: translateX(100%);
        }

        &:hover::before,
        &:hover::after {
          transform: translateX(0);
        }

        svg {
          display: none;
        }
      }
    }
  }
</style>
