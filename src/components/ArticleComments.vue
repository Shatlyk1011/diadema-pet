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
const comments = [
  {
    imgUrl:
      "https://images.unsplash.com/photo-1603777953703-c2c6484b0ee6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=387&q=80",
    name: "Benjamin Franklin",
    time: "Feb 12, 2017 8:24PM",
    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur repellat ea consequuntur, eum cupiditate eligendi deserunt rerum quisquam expedita a veniam ab repellendus dolor ad vitae optio odiovoluptas saepe.",
  },
  {
    imgUrl:
      "https://sun1-84.userapi.com/s/v1/if1/yZmFw4gOUyS9IrOO5x9T9LPM1215vKouKx6XdnBIatDfntsPXyA6LnVqkgqwBePTNza8UvYR.jpg?size=200x200&quality=96&crop=127,0,240,240&ava=1",
    name: " Antonio Margareti ",
    time: "Feb 12, 2017 8:24PM",
    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur repellat ea consequuntur, eum cupiditate eligendi deserunt rerum quisquam expedita a veniam ab repellendus dolor ad vitae optio odiovoluptas saepe.",
  },
]

let user = {
  name: "Ибрагим вам о чем нибдуь говорит?",
  imgUrl:
    "https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
}
</script>

<style lang="scss" scoped>
@import "@/globals";

.section-comments {
  padding: 4.2rem 0;
  .dark & {
    background-color: $color-black;
  }

  .comments {
    display: flex;
    flex-direction: column;

    max-width: 62rem;
    padding-bottom: 10rem;
    margin: 0 auto;

    h3 {
      font-size: 3rem;
      text-align: center;
      margin-bottom: 4rem;
    }

    .comment {
      display: flex;
      gap: 1.4rem;
      align-items: start;
      &:not(:last-child) {
        margin-bottom: 6rem;
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
