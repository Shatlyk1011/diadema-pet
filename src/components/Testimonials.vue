<template>
  <section class="section-testimonials align-center">
    <h3>Что говорят люди</h3>
    <p class="subtitle">
      «После использования различных платформ я изменился!»
    </p>

    <div class="testimonials">
      <div class="testimonial" v-for="t in testimonials" :key="t.socialLink">
        <div class="info">
          <img class="info__img" :src="t.imgUrl" alt="" />
          <div class="logs">
            <p class="name">{{ t.name }}</p>
            <span>{{ t.socialLink }}</span>
          </div>
          <div class="social">
            <img src="../assets/icons/twitter.svg" alt="" />
          </div>
        </div>

        <p class="text">"{{ t.text }}"</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    imgUrl:
      "https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NXx8Z2lybCUyMGZhY2V8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=500&q=60",
    name: "Луиза Рамирес",
    socialLink: "@ramirezzz",
    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius praesentium quae asperiores inventore omnis placeat minus nisi explicabo nemo ipsum.",
  },
  {
    imgUrl:
      "https://images.unsplash.com/photo-1553514029-1318c9127859?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=464&q=80",
    name: "Джози Норман",
    socialLink: "@josienorman",
    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius praesentium quae asperiores inventore omnis placeat minus nisi explicabo nemo ipsum.",
  },
  {
    imgUrl:
      "https://images.unsplash.com/photo-1605017661025-104f4dbb650f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=764&q=80",
    name: "Светлана Николаевна",
    socialLink: "@sup_borsh",
    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius praesentium quae asperiores inventore omnis placeat minus nisi explicabo nemo ipsum.",
  },
]
</script>

<style lang="scss" scoped>
@import "@/globals";
.section-testimonials {
  padding: 9rem 5.5rem 4rem;

  h3 {
    font-size: 4.4rem;
    text-transform: capitalize;
    font-family: $ff-garamond;
  }

  .subtitle {
    color: $color-gray-2;
    margin-top: 2.4rem;
  }

  .testimonials {
    margin-top: 5rem;
    display: flex;
    gap: 3rem;
    text-align: left;
    max-width: 144rem;
    margin: 0 auto;
    .testimonial {
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
      background-color: $color-gray-1;
      padding: 3rem;
      .info {
        display: flex;
        gap: 2rem;
        align-items: center;
        &__img {
          width: 5.6rem;
          height: 5.6rem;
          border-radius: 100%;
          object-fit: cover;
        }

        .logs {
          display: flex;
          flex-direction: column;
          gap: 4px;
          justify-content: center;
          .name {
            font-size: 1.8rem;
            font-weight: 500;
          }

          span {
            font-size: 1rem;
            font-weight: 700;
            color: $color-gray-2;
          }
        }
        .social {
          margin-left: auto;
          width: 2rem;
          cursor: pointer;
        }
      }
      .text {
        line-height: 1.5;
      }
    }
  }
}
</style>
