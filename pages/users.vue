<template>
  <div>
    <nuxt-link to="/users">Users</nuxt-link>&nbsp;
    <nuxt-link to="/admins">Admins</nuxt-link>
    <br />
    <input type="text" v-model="userId" />
    <button @click="onLoadUser" type="submit">LOad</button>
    <nuxt-child />
  </div>
</template>
<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // }
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push('/users/' + this.userId)
    }
  }
}
</script>