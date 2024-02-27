<template lang="pug">
.contentContainer
  img.backgroun-battle-zone(src="https://assets.xboxservices.com/assets/8b/3c/8b3cf993-31f4-4811-b5b9-086022a4867d.jpg?n=Xbox-Series-X_Parallax-Hero-Background_1084_1920x1250.jpg" alt = "background photo")
  .black-hue
  .container-armyman
    .cut-off-top
      img.army-man(src="https://assets.xboxservices.com/assets/04/f8/04f87a00-f26d-4b26-af9e-52e5f3ac821e.png?n=Xbox-Series-X_Parallax-Hero-Middle_1084_1920x1250.png", alt="army man looking behind him")
      img.fire-streaks(src="https://assets.xboxservices.com/assets/2e/e3/2ee3d736-337c-4f63-9dc1-3cf1fc7fc197.png?n=Xbox-Series-X_Parallax-Hero-Foreground_1084_1920x1250.png", alt="fire streaks")
    .text-container
      .top-text
        p.performance TRUE
          span.stats  4K
            .stat-explained Gaming
        p.performance UP TO
          span.stats 120
            .stat-explained Frames per second
        span.stats 8K
          p.performance  HDR
            .stat-explained High Dynamic Range
        .image-container-forstats
          img.triangle(src="https://assets.xboxservices.com/assets/c8/2f/c82ff85b-817e-4b95-a36e-2acdb3ea40a7.png?n=XBX_A-EngineeredForSpeed-VLogo-D.png", alt="xbox velocity architecture logo")
          .stat-explained-forimage
            .stat-explained Xbox Velocity Architecture
      .text-contain-xbox-fast
        span.stats THE FASTEST, MOST POWERFUL XBOX EVER
      .greenstripe-container
        .greenstripe
</template>

<script>
import { gsap } from 'gsap'
export default {
  name: 'ContentSection2', // not sure why important
  computed: {
    isMain () {
      return this.$store.state.site === 'main'
    }
  },
  mounted () {
    gsap.to('.black-hue', {
      scrollTrigger: {
        trigger: '.black-hue',
        scrub: true,
        start: 'top+=200 center',
        end: 'bottom center'
        // markers: true
      },
      opacity: 0.2
    })
    gsap.to('.army-man', {
      scrollTrigger: {
        trigger: '.army-man',
        scrub: true,
        start: 'top+=300 bottom',
        end: 'bottom top'
        // markers: {
        //   startColor: 'purple',
        //   endColor: 'fuchsia',
        //   fontSize: '1rem',
        //   indent: 200,
        //   fontWeight: 400
        // }
      },
      ease: 'power1.in',
      y: 250
    })
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: '.text-container',
        endTrigger: '.text-container',
        start: 'center bottom',
        end: 'bottom center',
        scrub: true
      }
    })

    tl.to('.text-container', {
      y: -100,
      opacity: 1
    }).to('.text-container', {
      y: -200,
      opacity: 0
    })
    gsap.to('.fire-streaks', {
      scrollTrigger: {
        trigger: '.army-man',
        scrub: true,
        start: 'top+=200 bottom',
        end: 'bottom center'
        // markers: {
        //   startColor: 'grey',
        //   endColor: 'blue',
        //   fontSize: '1rem',
        //   indent: 300,
        //   fontWeight: 400
        // }
      },
      y: 150
    })
  }
  // mounted () {
  // // refs are generally better
  // // gsap.from('.element', { duration: 5, x: 100 })
  //   gsap.to('.contentContainer', {
  //     scrollTrigger: {
  //       trigger: '.contentContainer',
  //       scrub: true,
  //       start: 'top-=500px center',
  //       end: 'top center',
  //       markers: true
  //     },
  //     y: -100,
  //     ease: 'none'
  //   })
  // }
  // const tl = gsap.timeline({
  //     scrollTrigger: {
  //       trigger: '.army-man',
  //       start: 'top+=200 bottom',
  //       end: 'center center',
  //       scrub: true,
  //       markers: true,
  //       toggleActions: 'play reverse play reverse'
  //     },
  //   })
  //   tl.to('text-container', { opacity: 1, duration: 0.5 })
  //   tl.to('text-container', { opacity: 0, duration: 0.5 }, 0.5)
}
</script>

<style lang="scss" scoped>
.contentContainer{
  position: relative;
  background-color: rgb(255, 101, 186);
  width: 100%;
  max-width: 1920px;
  height: 69vw;
  display: flex;
  margin-top: 270px;
  img.backgroun-battle-zone {
  z-index: 1;
  width: 100%;
  //height: calc((100vw - (100vw - 1920px)) * 0.58);
  height: 69vw;
  position: relative;
}
.black-hue {
  width: 100%;
  height: 100%;
  background-color: #000000a8;
  z-index: 10;
  position: absolute;
}
.container-armyman{
  width: 100%;
  background-color: orangered;
  height: 69vw;
  //height: calc((100vw - (100vw - 1920px)) * 0.58);
  position: absolute;
  display: flex;
  align-items: flex-end;
  overflow: hidden;
  justify-content: center;
  .cut-off-top{
    position: absolute;
    background-color: transparent;
    width: 100%;
    height: 90%;
    z-index: 1;
    overflow: hidden;
    .army-man {
      width: 100%;
      position: absolute;
      z-index: 1;
      margin-top: -50px;
    }
    .fire-streaks{
      width: 100%;
      height: 60vw;
      position: relative;
      z-index: 2;
      margin-top: -90px;
    }
  }
  .text-container {
    width: 88vw;
    height: 100%;
    position: relative;
    background-color: transparent;
    display: flex;
    justify-content: space-around;
    align-items: center;
    z-index: 11;
    line-height: 350%;
    opacity: 0;
  }
  .top-text {
    display: flex;
    width: 100%;
    justify-content: space-around;
    align-items: center;
    margin-top: -20%;
  }
  .performance {
    display: inline;
    color: white;
    font-size: 30px;
    font-family: Segoe Pro Black,sans-serif;
    text-shadow: 2px 2px 8px black;
  }
  .stats {
      font-size: 60px;
      color: white;
      font-family: Segoe Pro Black,sans-serif;
      text-shadow: 2px 2px 8px black;
      // font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
   }
   .image-container-forstats {
    display: inline-flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
   }
   .triangle {
    width: 7vw;
    size: 90%;
    display: block;
    position: relative;
   }
   .stat-explained {
    color: white;
    font-size: 20px;
    display: block;
    font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 400;
    position: relative;
    z-index: 1;
   }
   .text-contain-xbox-fast{
    display: flex;
    position: absolute;
    background-color: transparent;
   }
   .greenstripe-container{
    width: 100%;
    height: 5%;
    position: absolute;
    display: flex;
    justify-content: center;
    margin-top: 18%;
   }
   .greenstripe {
      background-color: #9bf00b;
      width: 3.5%;
      height: 17%;
      position: relative;
      transform: skew(-25deg);
      display: block;
    }
}
}
</style>
