<template>
  <header>
    <div class="nav">
      <div class="logo">Diadema</div>

      <ul class="links">
        <li>Блог</li>
        <li>Контакты</li>
      </ul>

      <ul class="icons">
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <path
              d="M160 112c0-35.3 28.7-64 64-64s64 28.7 64 64v48H160V112zm-48 48H48c-26.5 0-48 21.5-48 48V416c0 53 43 96 96 96H352c53 0 96-43 96-96V208c0-26.5-21.5-48-48-48H336V112C336 50.1 285.9 0 224 0S112 50.1 112 112v48zm24 48a24 24 0 1 1 0 48 24 24 0 1 1 0-48zm152 24a24 24 0 1 1 48 0 24 24 0 1 1 -48 0z"
            />
          </svg>
        </li>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
            <path
              d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
            />
          </svg>
        </li>
      </ul>
    </div>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "@/globals";

header {
  padding: 5rem 15rem;
  background-color: $bg-white;

  .nav {
    display: flex;
    align-items: center;
    max-width: 144rem;
    margin: 0 auto;
    gap: 4rem;
    .logo {
      flex-grow: 1;
      font-weight: 700;
      font-size: 3rem;
    }

    .links,
    .icons {
      display: flex;
    }

    .links {
      gap: 4.8rem;
      font-size: 1.4rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-weight: 5;
      li {
        cursor: pointer;
      }
    }

    .icons {
      gap: 3rem;
      li {
        cursor: pointer;
        svg {
          fill: $color-gray-2;
          height: 2rem;
          width: 2rem;
        }
      }
    }
  }
}
</style>
