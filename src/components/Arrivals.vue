<template>
  <section class="section-arrivals align-center">
    <h2>Новая Коллекция</h2>
    <div class="arrivals">
      <div class="item" v-for="(arrival, index) in bb" :key="index">
        <div class="img">
          <img :src="arrival.imgUrl" alt="" />
        </div>
        <h4>{{ arrival.title }}</h4>
        <p>usd {{ arrival.price }}</p>
      </div>
    </div>

    <div class="show-all" v-if="showAll" @click="showAll = !showAll">
      Показать больше
    </div>
    <div class="show-all" v-if="!showAll" @click="showAll = !showAll">
      Показать меньше
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue"
import { arrivals } from "@/db"

const showAll = ref(true)

let bb = computed(() => {
  return showAll.value ? arrivals.value.slice(0, 6) : arrivals.value
})
</script>

<style lang="scss" scoped>
@import "@/globals";
.section-arrivals {
  background-color: $color-white;
  padding: 11rem 5rem 7rem;
  height: 100%;
  box-sizing: border-box;

  @include respond(tab-land) {
    padding: 6rem 3rem 4rem;
  }

  @include respond(tab-port) {
    padding: 4rem 2rem 3rem;
  }

  .dark & {
    background-color: $color-black-9;
  }

  h2 {
    font-family: $ff-garamond;
    font-size: 4rem;
  }

  .arrivals {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 37rem);
    max-width: 114rem;
    margin: 5rem auto 0;
    column-gap: 4.5rem;
    row-gap: 8rem;

    @include respond(tab-land) {
      column-gap: 2.4rem;
      row-gap: 5rem;
    }

    @include respond(tab-port) {
      margin: 3rem auto 0;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(2, 30rem);
      column-gap: 2rem;
      row-gap: 4rem;
    }

    .item {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      height: 37rem;
      box-sizing: content-box;
      box-shadow: rgba(0, 0, 0, 0.05) 0px 10px 20px;
      transition: all 0.2s ease-in-out;
      cursor: pointer;
      @include respond(tab-port) {
        height: 30rem;
      }

      @media (hover) {
        &:hover {
          transform: scale(1.02);
          box-shadow: rgba(0, 0, 0, 0.08) 5px 10px 20px,
            rgba(0, 0, 0, 0.09) 5px 6px 6px;
        }
      }

      &:active {
        transform: translateY(3px) scale(0.98);
        box-shadow: rgba(0, 0, 0, 0.05) 0px 10px 20px;
      }

      .img {
        flex-grow: 1;
        height: max-content;
        img {
          width: 100%;
          height: 100%;
          flex-grow: 1;
          object-fit: cover;
        }
      }

      h4 {
        font-family: $ff-garamond;
        font-size: 2.2rem;
        font-weight: 500;
        margin-top: 1.8rem;
      }

      p {
        font-size: 1.4rem;
        color: $color-gray-2;
        margin-top: 1rem;
        text-transform: uppercase;
      }
    }
  }

  .show-all {
    font-size: 1.2rem;
    text-transform: uppercase;
    color: $color-gray-2;
    padding: 1.6rem 0;
    border-top: 1px solid currentColor;
    border-bottom: 1px solid currentColor;
    max-width: 114rem;
    margin: 7rem auto 0;
    cursor: pointer;
    transition: all 0.2s ease-in-out;

    @include respond(tab-land) {
      margin-top: 4rem;
    }

    @include respond(tab-land) {
      margin-top: 3rem;
      padding: 1rem 0;
      font-size: 1rem;
    }

    &:hover {
      color: $color-black;
    }

    .dark & {
      color: $bg-white;

      &:hover {
        color: $color-main;
      }
    }
  }
}
</style>
