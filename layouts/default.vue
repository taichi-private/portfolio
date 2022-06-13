<template>
  <div>
    <Header />
    <main>
      <nuxt />
    </main>
    <Footer />
  </div>
</template>

<script lang="ts">
import Header from "~/components/DefaultHeader.vue"
import Footer from "~/components/DefaultFooter.vue"

export default {
  name: 'defaultLayout',
  components: {
    Header,
    Footer,
  },
}
</script>
