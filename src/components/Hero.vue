<template>
  <section class="section-hero">
    <swiper
      :modules="[Pagination, Autoplay]"
      :pagination="paginationConfig"
      :autoplay="{ delay: 4000, disableOnInteraction: false }"
    >
      <swiper-slide class="hero">
        <div class="content">
          <h1>Женская компания</h1>
          <p>Повседневная коллекция</p>

          <a type="button" href="" class="link">Узнать больше </a>
        </div>
        <div class="img">
          <img src="./../assets/bg-main.png" alt="main girl" />
        </div>
      </swiper-slide>

      <swiper-slide class="hero">
        <div class="content">
          <h1>Женская коллекция</h1>
          <p>Повседневная коллекция</p>

          <a type="button" href="" class="link">Узнать больше </a>
        </div>
        <div class="img">
          <img src="./../assets/bg-main.png" alt="main girl" />
        </div>
      </swiper-slide>

      <swiper-slide class="hero">
        <div class="content">
          <h1>Женская девушка</h1>
          <p>Повседневная коллекция</p>

          <a type="button" href="" class="link">Узнать больше </a>
        </div>
        <div class="img">
          <img src="./../assets/bg-main.png" alt="main girl" />
        </div>
      </swiper-slide>
    </swiper>
    <div class="pagination"></div>
  </section>
</template>

<script setup>
import { Pagination, Autoplay } from "swiper"
import { Swiper, SwiperSlide } from "swiper/vue"
import "swiper/css"
import "swiper/css/pagination"

const paginationConfig = {
  el: ".pagination",
  bulletClass: "page",
  bulletActiveClass: "active",
  clickable: true,
}
</script>

<style lang="scss">
@import "@/globals";

.section-hero {
  height: 100%;
  background: $bg-white;
  position: relative;
  margin-top: -1px;

  .dark & {
    background-color: $color-black;
  }

  .hero {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    align-items: center;
    margin: 0 auto;

    .content {
      display: flex;
      flex-direction: column;
      grid-column: 3 / span 5;
      margin-bottom: 4rem;

      @include respond(tab-port) {
        grid-column: 2 / span 6;
      }

      h1 {
        font-family: $ff-garamond;
        font-size: 6rem;

        @include respond(tab-land) {
          font-size: 5rem;
        }

        @include respond(tab-port) {
          font-size: 4rem;
        }
        .dark & {
          color: $color-main;
        }
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

          transition: all 0.2s ease-in-out;

          &:hover {
            color: $color-main;
          }

          .dark & {
            color: $color-main;

            &:hover {
              color: $color-accent;
            }
          }
        }
      }
    }

    .img {
      /* include min-width 144rem and increse grid column */
      grid-column: 8 / 12;
      display: flex;
      justify-content: flex-start;
      user-select: none;
      img {
        @include respond(tab-port) {
          width: 100%;
        }
      }
    }
  }

  .pagination {
    text-align: center;
    width: 100%;
    z-index: 22;
    position: absolute;
    bottom: 4.5rem;

    @include respond(tab-land) {
      bottom: 3rem;
    }
    @include respond(tab-port) {
      bottom: 1.5rem;
    }

    .page {
      display: inline-block;
      width: 6rem;
      height: 2px;
      background: #c4c4c4;
      cursor: pointer;

      &:not(:last-child) {
        margin-right: 1rem;
      }

      .dark & {
        background-color: $color-accent;
      }
      &.active {
        background-color: $color-gray-2;

        .dark & {
          background-color: $color-main;
        }
      }
    }
  }
}
</style>
