<template>
  <header>
    <div class="nav">
      <div class="logo"><router-link to="/">Diadema</router-link></div>
      <img
        v-on-click-outside="closeMenu"
        class="menu"
        @click="toggleMenu"
        src="./../assets/icons/menu.svg"
        alt=""
      />

      <div class="container" ref="container">
        <ul class="links">
          <li>
            <router-link class="link" :to="{ name: 'Blog' }">Блог</router-link>
          </li>
          <li>
            <router-link class="link" :to="{ name: 'Blog' }"
              >Контакты</router-link
            >
          </li>
        </ul>

        <ul class="icons">
          <li type="button" @click="toggleDark()">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="ionicon"
              viewBox="0 0 512 512"
            >
              <path
                d="M160 136c0-30.62 4.51-61.61 16-88C99.57 81.27 48 159.32 48 248c0 119.29 96.71 216 216 216 88.68 0 166.73-51.57 200-128-26.39 11.49-57.38 16-88 16-119.29 0-216-96.71-216-216z"
                stroke="isDark ? '#8d8d8d' : '#deac7c'"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="32"
                :fill="isDark ? '#8d8d8d' : '#deac7c'"
              />
            </svg>
          </li>
          <li>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              <path
                d="M160 112c0-35.3 28.7-64 64-64s64 28.7 64 64v48H160V112zm-48 48H48c-26.5 0-48 21.5-48 48V416c0 53 43 96 96 96H352c53 0 96-43 96-96V208c0-26.5-21.5-48-48-48H336V112C336 50.1 285.9 0 224 0S112 50.1 112 112v48zm24 48a24 24 0 1 1 0 48 24 24 0 1 1 0-48zm152 24a24 24 0 1 1 48 0 24 24 0 1 1 -48 0z"
              />
            </svg>
          </li>
          <li>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
              <path
                d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
              />
            </svg>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue"
import { useDark, useToggle } from "@vueuse/core"
import { vOnClickOutside } from "@vueuse/components"

const isDark = useDark({
  selector: "body",
})
const toggleDark = useToggle(isDark)

const container = ref()

const toggleMenu = () => container.value.classList.toggle("active")
const closeMenu = () => container.value.classList.remove("active")
</script>

<style lang="scss" scoped>
@import "@/globals";

header {
  padding: 5rem 15rem;
  background-color: $bg-white;
  position: relative;

  @include respond(tab-land) {
    padding: 3rem 9rem;
  }

  @include respond(tab-port) {
    padding: 2rem 4rem;
  }

  .dark & {
    background-color: $color-black;
  }

  .logo {
    flex-grow: 1;
    font-weight: 700;
    font-size: 3rem;

    @include respond(tab-port) {
      font-size: 2.4rem;
    }

    a {
      text-decoration: none;
      color: inherit;
      .dark & {
        color: $color-main;
      }
    }
  }

  .menu {
    display: none;

    @include respond(phone) {
      display: block;
      z-index: 100;
    }
  }

  .nav {
    display: flex;
    align-items: center;
    max-width: 144rem;
    margin: 0 auto;
    gap: 4rem;

    @include respond(tab-port) {
      gap: 3rem;
    }

    .container {
      display: flex;
      align-items: center;
      flex-grow: 1;
      justify-content: space-between;
      gap: 4rem;

      @include respond(phone) {
        position: absolute;
        top: 0;
        right: 0;
        width: 100%;
        height: 100vh;
        background-color: rgba($color-black, 0.2);
        backdrop-filter: blur(4px);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: 3.2rem;
        z-index: 40;

        transition: all 0.2s ease-in-out;

        opacity: 0;
        visibility: hidden;
        user-select: none;
        transform: translateX(100%);

        &.active {
          opacity: 1;
          visibility: visible;
          user-select: auto;
          transform: translateX(0);
        }
      }

      .links,
      .icons {
        display: flex;
        transition: all 0.3s ease-in-out;
      }

      .links {
        gap: 4.8rem;
        font-size: 1.4rem;
        text-transform: uppercase;
        letter-spacing: 1px;
        font-weight: 500;
        margin-left: auto;

        @include respond(tab-port) {
          gap: 2.4rem;
        }
        @include respond(phone) {
          margin: 0;
          flex-direction: column;
          font-size: 2rem;
          align-items: center;
        }

        li,
        .link {
          &:link,
          &:visited {
            text-decoration: none;
            color: inherit;

            transition: all 0.2s ease-in-out;
            cursor: pointer;
            &:hover {
              color: $color-main;
            }
          }
        }
      }

      .icons {
        gap: 3rem;

        @include respond(tab-port) {
          gap: 2rem;
        }
        li {
          cursor: pointer;
          svg {
            transition: all 0.2s ease-in-out;
            fill: $color-gray-2;
            height: 2rem;
            width: 2rem;

            @include respond(tab-port) {
              height: 1.8rem;
              width: 1.8rem;
            }
            &:hover {
              fill: $color-main;
            }
          }
        }
      }
    }
  }
}
</style>
