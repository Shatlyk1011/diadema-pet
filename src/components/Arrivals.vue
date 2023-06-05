<template>
  <section class="section-arrivals align-center">
    <h2>Новая Коллекция</h2>
    <div class="arrivals">
      <div class="wrap" v-for="(arrival, index) in arrivals" :key="index">
        <div class="img">
          <img :src="arrival.imgUrl" alt="" />
        </div>
        <h4>{{ arrival.title }}</h4>
        <p>usd {{ arrival.price }}</p>
      </div>
    </div>

    <div class="show-all">Показать все</div>
  </section>
</template>

<script setup>
const arrivals = [
  {
    imgUrl:
      "https://images.unsplash.com/photo-1605733513597-a8f8341084e6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1229&q=80",
    title: "Стиль из истории",
    price: 200,
  },
  {
    imgUrl:
      "https://img.freepik.com/free-photo/pink-canvas-sneakers-with-polka-dot-unisex-footwear-fashion_53876-106039.jpg?w=996&t=st=1685809743~exp=1685810343~hmac=61b0700d8adb262643d749e6aa1320835de0380c8d0dfb5e48b9ce45daecb3e9",
    title: "Стиль из истории",
    price: 200,
  },
  {
    imgUrl:
      "https://img.freepik.com/free-photo/fashion-portrait-young-elegant-woman_1328-2743.jpg?w=996&t=st=1685809797~exp=1685810397~hmac=c9d6d3c2855a2a99c92a83261022946c97a151cb5534e0c4f8e806abb9eb1f9f",
    title: "Стиль из истории",
    price: 200,
  },
  {
    imgUrl:
      "https://img.freepik.com/free-photo/basic-white-sneakers-unisex-streetwear-fashion-shoot_53876-102115.jpg?w=996&t=st=1685812139~exp=1685812739~hmac=76d153a9ea424f668767ceaabd2635199017b9679a1e226321e7e5b88ecb9239",
    title: "Стиль из истории",
    price: 200,
  },
  {
    imgUrl:
      "https://images.unsplash.com/photo-1566150902887-9679ecc155ba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
    title: "Стиль из истории",
    price: 200,
  },
  {
    imgUrl:
      "https://images.unsplash.com/photo-1527523413008-edd47b9485b4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
    title: "Стиль из истории",
    price: 200,
  },
]
</script>

<style lang="scss" scoped>
@import "@/globals";
.section-arrivals {
  background-color: $color-white;
  padding: 11rem 5rem 3px; /* ?? */
  height: 100%;

  .dark & {
    background-color: $color-black-9;
  }

  h2 {
    font-family: $ff-garamond;
    font-size: 4rem;

    .dark & {
    }
  }

  .arrivals {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 37rem);
    max-width: 114rem;
    margin: 0 auto;
    column-gap: 4.5rem;
    row-gap: 8rem;
    margin-top: 5rem;

    .wrap {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      height: 37rem;
      box-sizing: content-box;

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
    margin: 7rem auto;
    cursor: pointer;
    transition: all 0.2s ease-in-out;

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
