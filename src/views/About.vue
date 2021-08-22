<template>
  <div class="about">
    <button @click="goBack">Voltar</button>
    <h1>This is an about page</h1>
    <h1>{{ username }}</h1>
  </div>
</template>

<script>
export default {
  methods: {
    goBack () {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push('/')
    }
  },
}
</script>
