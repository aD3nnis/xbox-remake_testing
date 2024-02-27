<template lang="pug">
footer
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style lang="scss" scoped>
footer {
  //position: sticky; // -- currently wasn't changing anything about the footer--
  background: rgb(95, 175, 135);
  width: 0%; // -- self expanatory but makes it so that it changesthe width across --
  min-height: 0px; // --this changes the footer for every page and is a black box at the bottom of each page
  //-- this I believe makes a new section--
}
</style>
