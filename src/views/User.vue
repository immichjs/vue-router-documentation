<template>
  <div class="user">
    <h1>{{ $route.params.id }} - {{ name }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: '1', name: 'Mich'},
        { id: '2', name: 'Nicole'},
        { id: '3', name: 'Juh'},
        { id: '4', name: 'Ericka'},
    ]
    }
  },
  computed: {
    name () {
      let user
      this.users.forEach(e => {
        if (e.id === this.$route.params.id) user = e.name
      })
      return user
    }
  }
}
</script>

<style>

</style>
