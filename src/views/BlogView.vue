<template>
  <main class="blog-view">
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
import { posts } from "@/db"
</script>

<style lang="scss" scoped>
@import "@/globals";
.blog-view {
  h2 {
    font-family: $ff-garamond;
    font-size: 4rem;
    text-align: center;

    @include respond(tab-port) {
      font-size: 3rem;
    }
  }

  .blog {
    padding: 6rem 5rem;

    @include respond(tab-land) {
      padding: 4rem 3rem;
    }

    @include respond(tab-port) {
      padding: 3rem 2rem;
    }

    @include respond(smallest) {
      padding: 2rem;
    }

    .dark & {
      background-color: $color-black-9;
    }

    .container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      max-width: 114rem;
      margin: 5rem auto 0;
      gap: 3rem;

      @include respond(tab-land) {
        gap: 2rem;
      }

      @include respond(tab-port) {
        grid-template-columns: repeat(2, 1fr);
        margin-top: 3rem;
      }
      .item {
        color: $color-white;
        position: relative;
        cursor: pointer;
        max-width: 36rem;
        min-height: 36rem;
        box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px,
          rgba(0, 0, 0, 0.23) 0px 6px 6px;
        transition: all 0.2s ease-in-out;

        @include respond(tab-land) {
          min-height: 30rem;
        }

        @include respond(smallest) {
        }

        &:hover {
          box-shadow: rgba(0, 0, 0, 0.25) 5px 10px 20px,
            rgba(0, 0, 0, 0.29) 5px 6px 6px;
        }
        &:nth-child(4) {
          grid-column: 1 / span 2;
          max-width: 100%;

          @include respond(tab-port) {
            grid-column: auto;
          }
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

          @include respond(tab-land) {
            padding: 3rem;
            gap: 0.8rem;
          }

          @include respond(smallest) {
            padding: 1.6rem;
          }
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

            @include respond(tab-land) {
              margin-top: 2.4rem;
            }
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
