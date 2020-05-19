<template>
  <div>
    <nuxt-link to="/users">Users</nuxt-link>&nbsp;
    <nuxt-link to="/admins">Admins</nuxt-link>
    <br />
    <input type="text" v-model="userId" />
    <button @click="onLoadUser" type="submit">LOad</button>
    <nuxt-child />
    <Footer />
  </div>
</template>
<script>
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Footer
  },
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push('/users/' + this.userId)
    }
  },
  layout: 'users'
}
</script>