<template lang="pug">
.home.page
    //- Title based on window size. If SSR, this will prevent cumulative layout shift.
    client-only
      h1 {{ title }}
      h1(slot="placeholder") Loading...
    p This is a placeholder and home page, if you are looking for my Xbox project it is in the menu above titled Xbox. I am working on responsivness but for now it works best to look on a screen that is at least 1300px wide. The goal was to make it look exactly like the xbox series X console webpage. However, they updated their page before I was able to complete all of it. But what is there is almost identical to what it looked like.
    p The other menu items are some of the other things I worked on in my internship that were smaller projects
    p QRCode and Card are from https://www.frontendmentor.io/challenges
    p vimeo was working on embedding a video into the website
    .button-wrapper
      //- button(@click="causeError") Cause Error
      //- nuxt-link.btn(to="/sample") Sample Page
      //- ButtonCounter
</template>

<script>
import ButtonCounter from '~~/components/ButtonCount.vue'

export default {
  name: 'Home',
  components: {
    ButtonCounter
  },
  computed: {
    title () {
      if (this.$store.state.isMobile) {
        return 'Home - Mobile'
      } else if (this.$store.state.isTablet) {
        return 'Home - Tablet'
      } else {
        return 'Home - Desktop'
      }
    }
  },
  methods: {
    causeError () {
      throw new Error('ERROR')
    }
  }
}
</script>

<style lang="scss">
// .home {
// }
.button-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin-top: 2rem;

  button,
  .btn {
    margin: 0.5rem 0;
  }
  @include media-breakpoint-up(md) {
    flex-direction: row;

    button,
    .btn {
      margin: 0 0.5rem;
    }
  }
}
</style>
