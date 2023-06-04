<template>
  <section class="section-cta">
    <div class="cta">
      <div class="grid">
        <div class="wrap">
          <h2>
            fashionable <br />
            hats
          </h2>
          <button>промокод</button>
        </div>
        <img src="./../assets/bg-hats.png" alt="girl with hats" />
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "@/globals";
.section-cta {
  background-color: $color-white;
  height: 52rem;
  display: flex;
  align-items: end;
  justify-content: center;
  .cta {
    position: relative;
    background-color: $bg-white;
    width: 100vw;

    &::after {
      content: "";
      position: absolute;

      height: 4rem;
      width: 100%;
      background-color: $color-gray-1;
      bottom: -4rem;
      left: 0;
      z-index: 100;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      max-width: 144rem;
      margin: 0 auto;
      .wrap {
        display: flex;
        flex-direction: column;
        gap: 2.6rem;
        justify-content: center;
        align-items: center;
        grid-column: 2 / span 4;
        text-align: center;

        h2 {
          font-size: 5rem;
          text-transform: uppercase;
          font-family: $ff-garamond;
          line-height: 1.1;
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
        margin-top: -8rem;
        grid-column: 6 / 11;
        width: 100%;
      }
    }
  }
}
</style>
