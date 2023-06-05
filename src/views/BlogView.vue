<template>
  <main class="blog-view">
    <Hero />

    <section class="blog">
      <h2>Наш блог</h2>
      <div class="container">
        <div class="item" v-for="(post, index) in posts">
          <router-link
            :to="{ name: 'Article', params: { id: index } }"
            class="content"
          >
            <div class="topic">{{ post.topic }}</div>
            <div class="title">
              {{ post.title }}
            </div>
            <div class="text">
              {{ post.text }}
            </div>

            <div class="info">
              <div class="comments">
                <img src="./../assets/icons/comment.svg" alt="comment icon" />
                <span>{{ post.comments.length }}</span>
              </div>

              <div class="time">
                <img src="./../assets/icons/time.svg" alt="time icon" />

                <span>{{ post.time }} минут назад</span>
              </div>
            </div>
          </router-link>
          <div class="img-container">
            <img class="bg-image" :src="post.imgUrl" alt="" />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import Hero from "@/components/Hero.vue"

const posts = [
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1447752875215-b2761acb3c5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1682686581030-7fa4ea2b96c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDJ8fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1685703206366-d514f27076ef?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1171&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1682685795557-976f03aca7b2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1171&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1666870747605-cca30ed154c5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1332&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1441974231531-c6227db76b6e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1171&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1472214103451-9374bd1c798e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
  },
  {
    topic: "Travel",
    title: "Для ежедневного исправления советов по покупкам, идей нарядов.",
    text: "Делайте покупки напрямую у наших любимых независимых брендов и винтажных бутиков.",
    comments: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    time: 9,
    imgUrl:
      "https://images.unsplash.com/photo-1507371341162-763b5e419408?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=739&q=80",
  },
]
</script>

<style lang="scss" scoped>
@import "@/globals";
.blog-view {
  h2 {
    font-family: $ff-garamond;
    font-size: 4rem;
  }

  .blog {
    padding: 11rem 5rem;

    .dark & {
      background-color: $color-black-9;
    }

    .container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);

      max-width: 114rem;
      margin: 5rem auto 0;
      gap: 3rem;
      .item {
        color: $color-white;
        text-align: left;
        position: relative;
        cursor: pointer;
        max-width: 36rem;
        min-height: 36rem;

        &:nth-child(4) {
          grid-column: 1 / span 2;
          max-width: 100%;
        }

        .content {
          display: flex;
          position: relative;
          flex-direction: column;
          padding: 4rem;
          gap: 1rem;
          height: 100%;
          box-sizing: border-box;
          z-index: 10;
          text-decoration: none;
          color: inherit;
          .topic {
            font-size: 1rem;
            font-weight: 700;
            text-transform: uppercase;
          }

          .title {
            font-size: 2.6rem;
            font-family: $ff-garamond;
            line-height: 1.2;
            font-weight: 500;
            margin-top: 3.5rem;

            // show max 2 lines
            display: -webkit-box;
            overflow: hidden;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
          }

          .text {
            font-size: 1.8rem;
            line-height: 1.6;
            // show max 3 lines
            display: -webkit-box;
            overflow: hidden;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
          }

          .info {
            display: flex;
            padding-top: 1rem;
            justify-content: space-between;
            border-top: 1px solid currentColor;
            margin-top: auto;

            .comments,
            .time {
              font-size: 1.4rem;
              line-height: 1.4;
              display: flex;
              align-items: center;
              justify-content: center;
              gap: 1rem;
            }
            .comments {
              img {
              }

              span {
              }
            }

            .time {
              img {
              }

              span {
              }
            }
          }
        }

        .img-container {
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          z-index: 5;

          &:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
              180deg,
              rgba($color-black, 0.4) 0,
              rgba(#000, 0.8) 80%
            );
          }

          .bg-image {
            object-fit: cover;
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>
