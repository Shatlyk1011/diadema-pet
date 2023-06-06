<template>
  <section class="section-comments">
    <div class="comments">
      <h3>Коментарии</h3>

      <div class="comment" v-for="comment in comments" :key="comment.name">
        <img :src="comment.imgUrl" alt="" />
        <div class="wrap">
          <div class="user">
            <div class="name">{{ comment.name }}</div>
            <!-- time would be converted via date-fns -->
            <span>{{ comment.time }}</span>
          </div>
          <div class="text">
            {{ comment.text }}
          </div>
        </div>
      </div>

      <div class="add">
        <div class="new-comment">
          <img :src="user.imgUrl" :alt="user.name" />
          <textarea />
        </div>

        <button type="button">Опубликовать</button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { comments, user } from "@/db"
</script>

<style lang="scss" scoped>
@import "@/globals";

.section-comments {
  padding: 4.2rem 0;

  @include respond(tab-port) {
    padding: 4.2rem 2rem;
  }
  .dark & {
    background-color: $color-black;
  }

  .comments {
    display: flex;
    flex-direction: column;

    max-width: 62rem;
    padding-bottom: 10rem;
    margin: 0 auto;

    @include respond(tab-land) {
      padding-bottom: 6rem;
    }

    h3 {
      font-size: 3rem;
      text-align: center;
      margin-bottom: 4rem;
      @include respond(tab-land) {
        margin-bottom: 3rem;
      }
    }

    .comment {
      display: flex;
      gap: 1.4rem;
      align-items: start;
      &:not(:last-child) {
        margin-bottom: 6rem;

        @include respond(tab-land) {
          margin-bottom: 4rem;
        }
      }

      img {
        width: 4.2rem;
        height: 4.2rem;
        border-radius: 100%;
        object-fit: cover;
        flex-shrink: 0;
        transition: all 0.2s ease-in-out;

        &:hover {
          transform: scale(2);
        }
      }

      .wrap {
        display: flex;

        flex-direction: column;
        gap: 1rem;
        .user {
          display: flex;
          align-items: center;
          gap: 1.4rem;

          .name {
            font-size: 1.4rem;
            text-transform: uppercase;
            font-weight: 500;
          }

          span {
            color: $color-gray-2;
            font-size: 1.2rem;
          }
        }

        .text {
          font-size: 1.6rem;
          line-height: 1.4;
        }
      }
    }
    .add {
      display: flex;
      flex-direction: column;
      gap: 1.8rem;
      .new-comment {
        display: flex;
        gap: 1.8rem;

        img {
          width: 4.2rem;
          height: 4.2rem;
          border-radius: 100%;
          object-fit: cover;
          flex-shrink: 0;
        }

        textarea {
          all: unset;
          border: 1px solid $color-gray-2;
          padding: 1rem;
          min-height: 8rem;
          flex-grow: 1;

          &:active,
          &:focus {
            border: 1px solid $color-black;

            .dark & {
              border-color: $color-main;
            }
          }
        }
      }

      button {
        all: unset;
        display: inline-block;
        align-self: flex-end;
        padding: 1.2rem 1.8rem;
        color: $color-gray-2;
        border: 1px solid currentColor;
        transition: all 0.2s ease-in-out;
        &:hover {
          background-color: $color-accent;
          color: $color-white;

          .dark & {
            background-color: $color-main;
          }
        }

        .dark & {
          color: $color-white;
        }
      }
    }
  }
}
</style>
