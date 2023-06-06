<template>
  <section class="section-subscribe">
    <div class="container">
      <div class="wrap">
        <h4>Подпишитесь на наши новости</h4>
        <p class="subtitle">Подпишитесь на нашу еженедельную рассылку</p>
        <button type="button">подписаться</button>
      </div>
      <img src="./../assets/bg-cta.png" alt="girl" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "@/globals";
.section-subscribe {
  background-color: $bg-white;

  .dark & {
    background-color: $color-black;
  }
  .container {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    @include respond(phone) {
      padding: 2rem;
    }

    @include respond(smallest) {
      grid-template-columns: 1fr;
    }

    .wrap {
      grid-column: 3 / span 5;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      gap: 2.4rem;

      @include respond(tab-land) {
        grid-column: 2 / span 5;
      }

      @include respond(smallest) {
        align-items: center;
        gap: 1.5rem;
        text-align: center;
      }

      h4 {
        font-size: 4.2rem;
        font-family: $ff-garamond;

        @include respond(tab-port) {
          font-size: 3.2rem;
        }
      }

      p {
        font-size: 1.8rem;
        color: $color-gray-2;

        @include respond(tab-port) {
          font-size: 1.6rem;
        }
      }

      button {
        all: unset;
        cursor: pointer;
        padding: 1.4rem 4.8rem;
        text-transform: uppercase;
        font-size: 1rem;
        letter-spacing: 0.4px;
        font-weight: 500;
        border: 1px solid $color-gray-2;
        font-weight: 700;

        transition: all 0.2s ease-in-out;

        @include respond(tab-port) {
          padding: 1rem 2.4rem;
        }
        &:hover {
          color: $color-gray-1;
          background-color: $color-accent;
        }
        .dark & {
          &:hover {
            color: $color-gray-1;
            background-color: $color-accent;
          }
        }
      }
    }

    img {
      grid-column: 8 / -1;

      @include respond(tab-land) {
        grid-column: 7 / -1;
      }

      @include respond(tab-port) {
        width: 100%;
      }
    }
  }
}
</style>
