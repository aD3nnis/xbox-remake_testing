<template lang="pug">
.container
  .element(ref= "myElement")
      p Hello, GSAP!
  .container2(ref= "parallaxbg")
        img.picture(src="@/assets/images/photo_of_Beach.jpeg")
        img.pictureFront(ref= "parallaxbg" "picture" src="@/assets/images/image-qr-code.png" width ="288" height="288" data-speed=".5")

</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  mounted () {
  // refs are generally better
  // gsap.from('.element', { duration: 5, x: 100 })
    gsap.from(this.$refs.myElement, { duration: 5, x: 100 })
    gsap.to(this.$refs.parallaxbg, {
      scrollTrigger: {
        scrub: true
      },
      y: (i, target) => -ScrollTrigger.maxScroll(window) * target.dataset.speed,
      ease: 'none'
    })
  }
}
</script>

<style lang="scss" scoped>
.container {
  background-color: blue;
  // background-repeat: no-repeat;
  // position: absolute;
  display: block;
  overflow: hidden;
}
.container2 { // div#parallax-bg-3 div
  background-color: rgb(63, 62, 62);
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.picture {
  width: 50rem;
  height: 40rem;
}
</style>
