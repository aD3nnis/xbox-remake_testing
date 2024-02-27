<template lang="pug">
.test.page
  h1 Test
  ButtonCounter
</template>

<script>
import ButtonCounter from '~~/components/ButtonCount.vue'
export default {
  components: {
    ButtonCounter,
  },
}
</script>
