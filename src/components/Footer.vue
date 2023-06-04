<template>
  <footer class="footer">
    <div class="container">
      <div class="logo">Diadema</div>
      <ul>
        <li>женщины</li>
        <li>мужщины</li>
        <li>коллекция</li>
        <li>разпродажа</li>
      </ul>

      <div class="social">
        <svg
          width="8"
          height="18"
          viewBox="0 0 8 18"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M7 9H5V18H2V9H0V6H2V4C2 2.53 1.708 0 5 0H8V3H6C5.45348 3.01368 5.01368 3.45348 5 4V6H8L7 9Z"
          />
        </svg>

        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          class="ionicon"
          viewBox="0 0 512 512"
        >
          <path
            d="M496 109.5a201.8 201.8 0 01-56.55 15.3 97.51 97.51 0 0043.33-53.6 197.74 197.74 0 01-62.56 23.5A99.14 99.14 0 00348.31 64c-54.42 0-98.46 43.4-98.46 96.9a93.21 93.21 0 002.54 22.1 280.7 280.7 0 01-203-101.3A95.69 95.69 0 0036 130.4c0 33.6 17.53 63.3 44 80.7A97.5 97.5 0 0135.22 199v1.2c0 47 34 86.1 79 95a100.76 100.76 0 01-25.94 3.4 94.38 94.38 0 01-18.51-1.8c12.51 38.5 48.92 66.5 92.05 67.3A199.59 199.59 0 0139.5 405.6a203 203 0 01-23.5-1.4A278.68 278.68 0 00166.74 448c181.36 0 280.44-147.7 280.44-275.8 0-4.2-.11-8.4-.31-12.5A198.48 198.48 0 00496 109.5z"
          />
        </svg>

        <svg
          width="21"
          height="21"
          viewBox="0 0 21 21"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0_0_84)">
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M6 0H15C18.3137 0 21 2.68629 21 6V15C21 18.3137 18.3137 21 15 21H6C2.68629 21 0 18.3137 0 15V6C0 2.68629 2.68629 0 6 0ZM6 2H15C17.2091 2 19 3.79086 19 6V15C19 17.2091 17.2091 19 15 19H6C3.79086 19 2 17.2091 2 15V6C2 3.79086 3.79086 2 6 2ZM16 10.5C16 7.46243 13.5376 5 10.5 5C7.50628 5.10332 5.10332 7.50628 5 10.5C5 13.5376 7.46243 16 10.5 16C13.5376 16 16 13.5376 16 10.5ZM10.58 7C11.4874 6.99947 12.3578 7.35956 12.9996 8.00099C13.6414 8.64242 14.002 9.51261 14.002 10.42C13.947 12.3648 12.3819 13.9277 10.437 13.98C9.52971 13.9805 8.6594 13.6204 8.01776 12.979C7.37611 12.3375 7.01573 11.4673 7.016 10.56C7.07151 8.61578 8.63572 7.05332 10.58 7ZM17 5C17 4.44772 16.5523 4 16 4C15.4477 4 15 4.44772 15 5C15 5.55228 15.4477 6 16 6C16.5523 6 17 5.55228 17 5Z"
            />
          </g>
          <defs>
            <clipPath id="clip0_0_84">
              <rect width="21" height="21" fill="white" />
            </clipPath>
          </defs>
        </svg>

        <svg
          width="31"
          height="20"
          viewBox="0 0 31 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M9.99999 12V9H19C19.61 13.31 17.66 19.01 10.13 19.01C6.05468 19.041 2.4601 16.3475 1.34548 12.4274C0.230855 8.50739 1.87048 4.32555 5.35243 2.20774C8.83438 0.089938 13.3018 0.557343 16.27 3.35C15.0068 4.52062 14.6052 4.96515 14.2612 5.34605C14.085 5.54107 13.924 5.71941 13.67 5.97C12.694 5.10823 11.4318 4.64116 10.13 4.66C7.17802 4.66 4.78499 7.05303 4.78499 10.005C4.78499 12.957 7.17802 15.35 10.13 15.35C13.09 15.35 14.29 14.09 15.06 11.78C13.64 11.78 9.99999 12 9.99999 12ZM28 6V9H31V12H28V15L25 14.99V12H22V9H25V6H28Z"
          />
        </svg>
      </div>
    </div>

    <div class="rights">
      <div class="cr">&copy; 2023 все права защищены.</div>

      <div class="figma">
        <a href="">ссылка на макет</a>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style lang="scss">
@import "@/globals";
.footer {
  padding: 6.5rem 15rem 5rem;
  background: $bg-white;
  border-top: 1px solid $color-gray-2;

  .dark & {
    background-color: $color-black-9;
  }
  .container {
    display: flex;
    justify-content: space-between;
    gap: 2rem;
    align-items: center;
    padding-bottom: 4.2rem;

    .logo {
      font-weight: 700;
      font-size: 3rem;
      color: $color-gray-2;
      .dark & {
        color: $color-main;
      }
    }

    ul {
      display: flex;
      gap: 4rem;
      font-size: 1.2rem;
      text-transform: uppercase;
      li {
        cursor: pointer;
        transition: all 0.2s ease-in-out;

        &:hover {
          color: $color-gray-2;
        }

        &:active {
          transform: translateY(3px);
        }
      }
    }

    .social {
      display: flex;
      gap: 3rem;

      svg {
        fill: $color-gray-2;
        cursor: pointer;
        transition: all 0.15s ease-in-out;

        &:hover {
          transform: translateY(-3px) scale(1.05);
          fill: $color-main;
        }
      }
    }
  }

  .rights {
    display: flex;
    justify-content: space-between;
    color: $color-gray-2;
    font-size: 1.2rem;
    border-top: 1px solid rgba($color-gray-2, 0.5);
    padding: 3rem 0 0;

    .figma {
      a {
        all: unset;
        border-bottom: 1px solid currentColor;
      }
    }
  }
}
</style>
