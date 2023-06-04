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
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              class="ionicon"
              viewBox="0 0 512 512"
            >
              <path
                d="M496 109.5a201.8 201.8 0 01-56.55 15.3 97.51 97.51 0 0043.33-53.6 197.74 197.74 0 01-62.56 23.5A99.14 99.14 0 00348.31 64c-54.42 0-98.46 43.4-98.46 96.9a93.21 93.21 0 002.54 22.1 280.7 280.7 0 01-203-101.3A95.69 95.69 0 0036 130.4c0 33.6 17.53 63.3 44 80.7A97.5 97.5 0 0135.22 199v1.2c0 47 34 86.1 79 95a100.76 100.76 0 01-25.94 3.4 94.38 94.38 0 01-18.51-1.8c12.51 38.5 48.92 66.5 92.05 67.3A199.59 199.59 0 0139.5 405.6a203 203 0 01-23.5-1.4A278.68 278.68 0 00166.74 448c181.36 0 280.44-147.7 280.44-275.8 0-4.2-.11-8.4-.31-12.5A198.48 198.48 0 00496 109.5z"
              />
            </svg>
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
    margin: 5rem auto 0;
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

          svg {
            fill: #51aae9;
          }
        }
      }
      .text {
        line-height: 1.5;
      }
    }
  }
}
</style>
