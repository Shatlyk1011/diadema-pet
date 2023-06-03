<template>
  <section class="section-hero">
    <div class="hero">
      <div class="content">
        <h1>Женская компания</h1>
        <p>Повседневная коллекция</p>

        <a href="" class="link">Узнать больше </a>
      </div>
      <div class="img">
        <img src="./../assets/bg-main.png" alt="main girl" />
      </div>
    </div>

    <div class="pagination">
      <div class="page active"></div>
      <div class="page"></div>
      <div class="page"></div>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss">
@import "@/globals";

.section-hero {
  height: 100%;
  background: $color-gray-1;
  position: relative;

  .dark & {
    background: red;
  }
  .hero {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    align-items: center;
    max-width: 144rem;
    margin: 0 auto;

    .content {
      display: flex;
      flex-direction: column;
      grid-column: 3 / span 5;
      margin-bottom: 4rem;

      h1 {
        font-family: $ff-garamond;
        font-size: 6rem;
      }

      p {
        color: $color-gray-2;
        font-size: 1.8rem;
        margin-top: 1.6rem;
      }

      .link {
        &:link,
        &:visited {
          display: inline-block;
          align-self: flex-start;
          text-decoration: none;
          margin-top: 3.2rem;
          font-size: 1.2rem;
          font-weight: 700;
          padding-bottom: 4px;
          border-bottom: 1px solid currentColor;
          letter-spacing: 0.2px;
          text-transform: uppercase;
          color: inherit;
        }
      }
    }

    .img {
      /* include min-width 144rem and increse grid column */
      grid-column: 8 / 12;
      display: flex;
      justify-content: flex-start;
      img {
        width: fit-content;
      }
    }
  }

  .pagination {
    position: absolute;
    display: flex;
    gap: 1rem;
    bottom: 4rem;
    left: 50%;
    transform: translateX(-50%);

    .page {
      width: 6rem;
      height: 2px;
      background: #c4c4c4;
      &.active {
        background: $color-gray-2;
      }
    }
  }
}
</style>
