<template>
  <Nav />
  <router-view />
  <Footer />
</template>

<script setup>
import Nav from "@/components/Nav.vue"
import Footer from "@/components/Footer.vue"
import { useDark, useToggle } from "@vueuse/core"

const isDark = useDark({
  selector: "body",
})
const toggleDark = useToggle(isDark)
</script>

<style lang="scss" scoped>
p {
  height: 20px;
  width: 20px;
  position: fixed;
  // width: 100%;
  top: 0;
  right: 0;
  padding: 5rem;
  z-index: 999;
}
</style>
