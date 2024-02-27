<template lang="pug">
.test.page
  button(@click="count++") You clicked me {{ count }} times.
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    }
  },
}
</script>
