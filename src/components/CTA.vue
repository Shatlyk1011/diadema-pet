<template>
  <section class="section-cta">
    <div class="cta">
      <div class="grid">
        <div class="wrap">
          <h2>
            fashionable <br />
            hats
          </h2>
          <button type="button">промокод</button>
        </div>
        <img src="./../assets/bg-hats.png" alt="girl with hats" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "@/globals";
.section-cta {
  background-color: $color-white;
  height: 52rem;
  display: flex;
  align-items: end;
  justify-content: center;
  position: relative;

  @include respond(tab-land) {
    height: 40rem;
  }

  @include respond(tab-port) {
    height: 30rem;
  }

  @include respond(phone) {
    height: 100%;
  }

  .dark & {
    background-color: $color-black-9;
    margin-top: -1px;
  }
  .cta {
    background-color: $bg-white;
    width: 100vw;

    .dark & {
      background-color: $color-black-9;
    }

    &::after {
      content: "";
      position: absolute;
      height: 4rem;
      width: 100%;
      background-color: $color-gray-1;
      bottom: -4rem;
      left: 0;
      z-index: 100;

      @include respond(tab-port) {
        height: 2.5rem;
        bottom: -2.5rem;
      }

      .dark & {
        background-color: $color-black;
      }
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      max-width: 144rem;
      margin: 0 auto;

      @include respond(tab-port) {
        padding-top: 3rem;
      }

      @include respond(phone) {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: min-content 1fr;
        justify-content: center;
        gap: 2rem;
      }
      .wrap {
        display: flex;
        flex-direction: column;
        gap: 2.6rem;
        justify-content: center;
        align-items: center;
        grid-column: 2 / span 4;
        text-align: center;

        @include respond(phone) {
          grid-column: auto;
        }

        h2 {
          font-size: 5rem;
          text-transform: uppercase;
          font-family: $ff-garamond;
          line-height: 1.1;

          @include respond(tab-land) {
            font-size: 4rem;
          }

          @include respond(tab-port) {
            font-size: 3rem;
          }

          @include respond(phone) {
            font-size: 2.4rem;
          }

          .dark & {
            color: $color-main;
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
          border: 1px solid currentColor;
          font-weight: 700;
          transition: all 0.2s ease-in-out;

          @include respond(tab-land) {
            padding: 1rem 3rem;
          }

          &:hover,
          .dark &:hover {
            background-color: $color-accent;
            color: $color-white;
            border: 1px solid $color-accent;
          }

          .dark & {
            color: $color-accent;
          }
        }
      }

      img {
        margin-top: -8rem;
        grid-column: 6 / 11;
        width: 100%;

        @include respond(tab-land) {
          margin-top: -6rem;
          grid-column: 7 / -1;
          width: 80%;
        }

        @include respond(tab-port) {
          width: 70%;
        }

        @include respond(phone) {
          width: 40%;
          margin-top: 0;
          grid-column: auto;
          margin: 0 auto;
        }
      }
    }
  }
}
</style>
