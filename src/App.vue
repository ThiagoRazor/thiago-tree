<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
</script>
<script>
export default {
  data() {
    return {
      services: null,
    }
  },
  mounted() {
    fetch('https://raw.githubusercontent.com/ThiagoRazor/thiago-links/main/src/data/socials.json')
      .then(res => res.json())
      .then(res => this.services = res)
      .catch(e => console.log(e))
  },
}
</script>

<template>
  <header>
    <Header />
  </header>
  <main>
    <Main />
  </main>
</template>
