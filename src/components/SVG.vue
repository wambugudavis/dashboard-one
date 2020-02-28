<template>
  <component
    :is="icon"
  >
  </component>
</template>

<script>

  export default {
    props: {
      name: String
    },
    computed: {
      icon () {
        const name = this.name;
        return () => import(`./svgs/${name}`)
      }
    }
  }
</script>
