<template lang="pug">
header
  a.link(id="skipToMainContent" href="#mainContent") Skip to main content
  nav
    nuxt-link(to="/") Home
    template(v-if="isMain")
      nuxt-link(to="/xbox") Xbox
      //- nuxt-link(to="/sample") Sample
      nuxt-link(to="/test") Test
      nuxt-link(to="/QRCodeComp") QRCode
      nuxt-link(to="/card") Card
      //- nuxt-link(to="/layout") Layout
      //- nuxt-link(to="/gsapTest") gsap Test
      //- nuxt-link(to="/ballonEx") ballon
      nuxt-link(to="/vimeoStuff") vimeo
      .link-wrapper
        //- nuxt-link(to="/login") Log In
        //- span &nbsp; / &nbsp;
        //- nuxt-link(to="/register") Register

</template>

<script>
export default {
  name: 'AppHeader',
  computed: {
    isMain () {
      return this.$store.state.site === 'main'
    }
  }
}
</script>

<style lang="scss" scoped>
header {
  position: relative;
  width: 100%;
  height: 3rem;
  padding: 2rem;
  background: rgb(95, 140, 156);
  text-align: left;
  color: rgb(234, 234, 234);
}

nav {
  display: flex;
  justify-content: right;
  & > * {
    margin: 0 0.5rem;
  }
}
</style>
