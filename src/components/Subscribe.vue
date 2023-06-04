<template>
  <section class="section-subscribe">
    <div class="container">
      <div class="wrap">
        <h4>Подпишитесь на наши новости</h4>
        <p class="subtitle">Подпишитесь на нашу еженедельную рассылку</p>
        <button>подписаться</button>
      </div>
      <img src="./../assets/bg-cta.png" alt="girl" />
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "@/globals";
.section-subscribe {
  background-color: $bg-white;
  .container {
    display: grid;
    grid-template-columns: repeat(12, 1fr);

    .wrap {
      grid-column: 3 / span 5;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      gap: 2.4rem;
      h4 {
        font-size: 4.2rem;
        font-family: $ff-garamond;
      }

      p {
        font-size: 1.8rem;
        color: $color-gray-2;
      }

      button {
        all: unset;
        cursor: pointer;
        padding: 1.4rem 4.8rem;
        text-transform: uppercase;
        font-size: 1rem;
        letter-spacing: 0.4 px;
        font-weight: 500;
        border: 1px solid $color-gray-2;
        font-weight: 700;
      }
    }

    img {
      grid-column: 8 / -1;
    }
  }
}
</style>
