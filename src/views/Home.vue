<template>
  <Header />
  <Products />
</template>

<script>
import Header from '../components/Header.vue'
import Products from '../components/Products.vue'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Home',
  components: { Header, Products }
}
</script>
