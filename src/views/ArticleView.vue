<template>
  <main class="article-view">
    <div class="img-container">
      <img src="./../assets/sample.jpg" alt="freedom girl" />
    </div>
    <div class="content">
      <div class="topic">{{ post.topic }}</div>
      <div class="title">
        {{ post.title }}
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
      <div class="blog">
        <blockquote class="q">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Distinctio,
          deleniti? Voluptas eveniet rerum voluptatum, accusantium maiores,
          mollitia veniam dolore accusamus excepturi, nihil totam ea in quis
          dicta repudiandae asperiores natus.
        </blockquote>

        <h4>Какова история вашего бренда?</h4>
        <p>
          Я думаю, что это родилось из разочарования. У меня были все эти идеи и
          образы в голове, но я не мог понять, как я хочу превратить их в
          рисунок. В то же время мне было очень скучно со всей моей одеждой,
          поэтому я просто купил пачку чистых футболок и красок и пошел на это.
          Это был действительно хороший способ преодолеть мой творческий блок.
          Ну, я также работаю в ресторане, поэтому я изо всех сил стараюсь
          заполнить большую часть своего свободного времени творчеством! Но мне
          повезло, что меня окружает множество творческих людей, поэтому, даже
          когда я не занимаюсь искусством, я всегда чувствую творческий подъем и
          стимул. Я также ем много закусок, стараюсь ухаживать за своими
          растениями и дружу с собаками. Каждое мое изделие расписано вручную.
          Изначально у меня было несколько дизайнов, которые я делал на заказ,
          но рисовать одно и то же по шаблону снова и снова стало очень
          утомительно. Так что теперь я просто делаю продукты, которые являются
          единственными в своем роде. На самом деле для этого нет никакого
          реального плана или процесса.
        </p>

        <img class="image" src="./../assets/sample-2.jpg" alt="" />

        <h4>
          Расскажите нам больше о своем стиле рисования и о том, как вы его
          разработали.
        </h4>

        <p>
          Когда я впервые начал рисовать тушью, я использовал кисти для
          каллиграфии или суми-э, которые очень мягкие и вмещают много чернил.
          Меня это очень привлекало, потому что это помогало мне рисовать с
          определенной раскованностью, которой у меня обычно нет. В конце
          концов. Самое смешное, что рисование на одежде акварельными кистями
          очень похоже на рисование кистями для каллиграфии на бумаге. Из-за
          этого мне не хватало этих качеств в моей живописи, поэтому я снова
          поиграл с кистями суми-э. Это было довольно сложно, я забыл, как их
          использовать, но я думаю, что искусство — это постоянный процесс
          разучивания того, что вы знаете, а затем повторного изучения этого
          по-новому снова и снова.
        </p>

        <blockquote class="quote">
          Пожалуйста, узнайте больше о количестве процедур, которые вам могут
          понадобиться, ожидаемых результатах, побочных эффектах и квалификации
          специалиста, прежде чем приступить к лечению.
        </blockquote>
        <p>
          Наконец-то мне удалось купить одно из ее плетеных одеял, и я очень им
          довольна. Я всегда восхищался ее магазином и многое связывал с ее
          эстетикой. В каком-то смысле это побудило меня начать собственное
          дело. На самом деле я переместил свое рабочее место… в другую комнату
          в своей квартире, которая выглядит как увеличенная версия моего
          старого пространства. Ха-ха! Я очень люблю комфорт, когда дело доходит
          до моей работы. Наверное, поэтому моя комната так похожа на мои
          рисунки. Интересно рисовать в музеях или набрасывать идеи, когда я в
          кафе, на пляже или где-то в этом роде. Но когда я действительно готов
          воплотить идею в жизнь, мне нужно быть в своем собственном
          пространстве, окруженном всеми моими инструментами и вещами именно
          так, как мне нравится.
        </p>

        <div class="share">
          <div class="user">
            <img :src="post.user.imgUrl" alt="" />
            <p>{{ post.user.name }}</p>
          </div>
          <div class="links">
            <p>Поделиться:</p>
            <svg
              fill="#999999"
              width="8"
              height="18"
              viewBox="0 0 8 18"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M7 9H5V18H2V9H0V6H2V4C2 2.53 1.708 0 5 0H8V3H6C5.45348 3.01368 5.01368 3.45348 5 4V6H8L7 9Z"
              />
            </svg>

            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              fill="#999999"
              class="ionicon"
              viewBox="0 0 512 512"
            >
              <path
                d="M496 109.5a201.8 201.8 0 01-56.55 15.3 97.51 97.51 0 0043.33-53.6 197.74 197.74 0 01-62.56 23.5A99.14 99.14 0 00348.31 64c-54.42 0-98.46 43.4-98.46 96.9a93.21 93.21 0 002.54 22.1 280.7 280.7 0 01-203-101.3A95.69 95.69 0 0036 130.4c0 33.6 17.53 63.3 44 80.7A97.5 97.5 0 0135.22 199v1.2c0 47 34 86.1 79 95a100.76 100.76 0 01-25.94 3.4 94.38 94.38 0 01-18.51-1.8c12.51 38.5 48.92 66.5 92.05 67.3A199.59 199.59 0 0139.5 405.6a203 203 0 01-23.5-1.4A278.68 278.68 0 00166.74 448c181.36 0 280.44-147.7 280.44-275.8 0-4.2-.11-8.4-.31-12.5A198.48 198.48 0 00496 109.5z"
              />
            </svg>
            <svg
              width="31"
              height="20"
              viewBox="0 0 31 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M9.99999 12V9H19C19.61 13.31 17.66 19.01 10.13 19.01C6.05468 19.041 2.4601 16.3475 1.34548 12.4274C0.230855 8.50739 1.87048 4.32555 5.35243 2.20774C8.83438 0.089938 13.3018 0.557343 16.27 3.35C15.0068 4.52062 14.6052 4.96515 14.2612 5.34605C14.085 5.54107 13.924 5.71941 13.67 5.97C12.694 5.10823 11.4318 4.64116 10.13 4.66C7.17802 4.66 4.78499 7.05303 4.78499 10.005C4.78499 12.957 7.17802 15.35 10.13 15.35C13.09 15.35 14.29 14.09 15.06 11.78C13.64 11.78 9.99999 12 9.99999 12ZM28 6V9H31V12H28V15L25 14.99V12H22V9H25V6H28Z"
                fill="#999999"
              />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <ArticleComments />
  </main>
</template>

<script setup>
import ArticleComments from "@/components/ArticleComments.vue"
import { post } from "@/db"
</script>

<style lang="scss" scoped>
@import "@/globals";
.article-view {
  .dark & {
    color: $color-white;
    background-color: $color-black-9;
  }
  .img-container {
    .dark & {
      background-color: $color-black-9;
    }

    img {
      width: 100%;
      height: auto;
      object-fit: cover;
    }
  }

  .content {
    padding: 4.2rem 25rem 0;

    @include respond(tab-land) {
      padding: 3.2rem 10rem 0;
    }

    @include respond(tab-port) {
      padding: 2.4rem 6rem 0;
    }
    @include respond(phone) {
      padding: 2.4rem 4rem 0;
    }

    .dark & {
      background-color: $color-black-9;
    }
    .topic {
      font-size: 1.2rem;
      color: $color-gray-2;
      text-align: center;
    }

    .title {
      margin-top: 3rem;
      font-size: 5.6rem;
      font-weight: 500;
      font-family: $ff-garamond;
      text-align: center;

      @include respond(tab-port) {
        font-size: 4rem;
        line-height: 0.9;
      }
    }

    .info {
      margin-top: 4.5rem;
      display: flex;
      justify-content: space-between;
      color: $color-black;
      max-width: 33rem;
      margin: 4.5rem auto 0;
      .comments,
      .time {
        display: flex;
        align-items: center;
        color: $color-gray-2;
        gap: 1rem;
      }
    }

    .blog {
      blockquote,
      h4,
      p,
      .share {
        max-width: 62rem;
        margin: 0 auto;
      }
      .q {
        font-style: italic;
        text-align: center;
        padding: 4rem 0 5rem;
        font-weight: 500;
      }

      h4 {
        font-size: 2rem;
        margin-bottom: 2rem;
        line-height: 1.3;
      }

      p {
        font-size: 1.8rem;
        line-height: 1.7;
      }

      .image {
        width: 100%;
        margin: 0 auto;
        padding: 7.4rem 4rem;
        box-sizing: border-box;

        @include respond(tab-land) {
          padding: 5rem 0;
        }
      }

      .quote {
        font-style: normal;
        position: relative;
        margin: 5rem auto 4rem;
        line-height: 1.5;
        font-weight: 600;
        &:before {
          content: "";
          position: absolute;
          top: 0;
          left: -2.2rem;
          width: 2px;
          background-color: $color-black;
          height: 100%;
        }
      }

      .share {
        margin-top: 4.8rem;
        padding: 3rem 0 6rem 0;
        border-top: 1px solid $color-gray-1;
        display: flex;
        justify-content: space-between;
        color: $color-gray-2;
        font-size: 1.4rem;

        @include respond(tab-land) {
          margin-top: 2.4rem;
          padding: 2rem 0 4rem 0;
        }

        @include respond(smallest) {
          flex-direction: column;
          justify-content: center;
          align-items: center;
        }

        .user,
        .links {
          display: flex;
          gap: 1.2rem;
          align-items: center;
        }
        .user {
          img {
            width: 4.2rem;
            height: 4.2rem;
            border-radius: 100%;

            @include respond(smallest) {
              order: 2;
            }
          }

          p {
            text-transform: uppercase;
            font-size: 1.4rem;
          }
        }

        .links {
          p {
            margin-right: 6px;
            @include respond(smallest) {
              font-size: 1.4rem;
            }
          }

          img {
          }
        }
      }
    }
  }
}
</style>
