<template>
  <div>
    <h1>Most Popular Rivers in the World</h1>
    <ul>
      <li v-for="(river, index) in rivers" :key="`river-${index}`">
        {{ river.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  // async asyncData ({ $http }) {
  //   const res = await $http.$get('https://api.nuxtjs.dev/rivers')
  //   return {
  //     rivers: res
  //   }
  // },

  data () {
    return {
      rivers: []
    }
  },
  async fetch () {
    const res = await this.$http.$get('https://api.nuxtjs.dev/rivers')
    this.rivers = res
  }
}
</script>
