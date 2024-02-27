<template lang="pug">
.video-container_box_2
      client-only
      nav.containerfor_2nd_nav
        .containerfor_hero
          video.videosrc(autoplay loop  muted width="100%" src="https://assets.xboxservices.com/assets/11/b0/11b01ae2-f5ad-4890-bc1d-f2404d6f367a.mp4?n=Xbox-Series-X_Superhero-1084_Dream-Particles_1920x1080_02.mp4" type="video/mp4")
          .text-fadein
            h1.headingXbox XBOX SERIES X
            .greenStripe
            h2.powerDreams Power Your Dreams
            .heroPrice
              span.price-callout
                span.price-erp $499.99
                span.text-erp  ERP
                  a.hyperlink(href="#prices")
                    sup *
            a.call-to-action(href="#purchase")
              span CHECK AVAILABILITY
              .c-glyph
              .c-glyph2
            a.action-trigger(href="#")
              .play-glyph
                svg.play-glyph2(height="20" width="30")
                  polygon(points="5,3 17,11 5,19" style="fill:transparent;stroke:#9bf00b;stroke-width:2")
              span.x-hidden-focus PLAY VIDEO
        .menu
          p Xbox Series X
          ul.links
            li
              a.overview(href="#overview") OVERVIEW
            li
              a.games(href="#games") GAMES
            li
              a.specs(href="#specs") SPECS
            li
              a.gallery(href="#gallery") GALLERY
            li
              a.unbox(href="#unbox") UNBOX
          .heroPrice
            span.price-callout
              span.price-erp $499.99
                  span.text-erp  ERP
                    a.hyperlink(href="#prices")
                      sup.new *
            span.call-to-action(href="#purchase")
              span.ndCheck CHECK AVAILABILITY
              svg.play-glyph3(height="15" width="10")
                  polygon(points="0,0 3,0 6,6 3,11 0,11 4,6" style="fill:#9bf00b;stroke:#9bf00b;stroke-width:")
        XboxMenu
        xboxCompContentSection2
        xboxCompContentSection3
</template>
<script>

// polygon: x,y
// end point connects to the first point
// import { vueVimeoPlayer } from 'vue-vimeo-player'
// issues i ran into:
// 1. I put mute instead of muted
import { gsap } from 'gsap'
export default {
  name: 'XboxPage',
  // components: { vueVimeoPlayer },
  data () {
    return {
      // vidSrc: 'https://assets.xboxservices.com/assets/11/b0/11b01ae2-f5ad-4890-bc1d-f2404d6f367a.mp4?n=Xbox-Series-X_Superhero-1084_Dream-Particles_1920x1080_02.mp4',
      // videoID: '783455878',
    }
  },
  mounted () {
  // refs are generally better
  // gsap.from('.element', { duration: 5, x: 100 })
    gsap.to('.containerfor_hero', {
      scrollTrigger: {
        trigger: '.containerfor_hero',
        scrub: true,
        start: 'bottom+=450px center', // 'bottom+=450vw center'
        end: 'bottom+=900vh center', // 'bottom+=900px center'
        pinSpacing: false,
        // markers: {
        //   startColor: 'purple',
        //   endColor: 'fuchsia',
        //   fontSize: '1rem',
        //   indent: 200,
        //   fontWeight: 400
        // },
        pin: true
      }
    })
    gsap.to('.video-container_box_2', {
      scrollTrigger: {
        trigger: '.menu',
        endTrigger: '.video-container_box_2',
        scrub: true,
        start: 'top top', // 'bottom+=450vw center'
        end: 'bottom top', // 'bottom+=900px center'
        // markers: {
        //   startColor: 'grey',
        //   endColor: 'blue',
        //   fontSize: '1rem',
        //   indent: 300,
        //   fontWeight: 400
        // },
        pinSpacing: false,
        pin: '.menu'
      }
    })
    const animatedElement = document.querySelector('.menu')
    gsap.to('.menu', {
      scrollTrigger: {
        trigger: '.menu',
        endTrigger: '.video-container_box_2',
        scrub: true,
        start: 'top top', // 'bottom+=450vw center'
        end: 'bottom top', // 'bottom+=900px center'
        // markers: {
        //   startColor: 'grey',
        //   endColor: 'blue',
        //   fontSize: '1rem',
        //   indent: 300,
        //   fontWeight: 400
        // },
        onEnter: () => {
        // Callback when the start marker is hit
          gsap.to(animatedElement, {
            backgroundColor: 'rgba(0, 0, 0, .7)', // Change to your desired color
            duration: 0
          })
        },
        onLeaveBack: () => {
          // Callback when the start marker is exited
          gsap.to(animatedElement, {
            backgroundColor: 'initial' // Change back to the default color
          })
        }
      }
    })
  }
}
</script>
<style lang="scss" scoped>
.video-container_box_2 {
  width: 100vw;
  height: 10000px;
  display: flex;
  background-color: rgb(6, 6, 6);
  position: relative;
  justify-content: center;
  max-width: 1920px;
  margin: 0 auto;
  .containerfor_2nd_nav{
    background-color: rgb(101, 132, 199);
    width: 100vw;
    height: 3vh;
    justify-content: center;
    .heroPrice {
    color: white;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
    margin-top: -1.5%;
    font-size: 1vw;
    margin-bottom: 40px;
    .hyperlink {
      sup{
        vertical-align: top;
        font-size: 75%;
        color: #9bf00b;
      }
    }
  }
 .call-to-action {
    padding: 6px 20px 6px 22px;
    // margin: -36px 17px 0px 0px;
    color: #054b16;
    font-weight: 900;
    height: 11px;
    width: 11px;
    background: #9bf00b;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
    .c-glyph {
      background-color: #054b16;
      content: '';
      height: 6px;
      width: 11px;
      margin-left: 10px;
      display: inline-block;
      border-top: 6px solid transparent;
      border-left: 4px solid  #9bf00b;
      border-right: 6px solid transparent;
      border-bottom: 6px solid transparent;
    }
    .c-glyph2 {
      content: '';
      height: 6px;
      width: 11px;
      display: inline-block;
      border-top: 6px solid #9bf00b;
      border-left: 4px solid  transparent;
      border-right: 6px solid #9bf00b;
      border-bottom: 6px solid #9bf00b;
      margin-left: -7px;
    }
    span{
      max-width: 100%;
      display: inline-block;
      position: relative;
      left: 0;
      text-overflow: clip;
      overflow: hidden;
      transition: all 200ms ease-in-out;
      vertical-align: middle;
      margin-bottom: 3px;
      // line-height: 18.5px;
    }
    span:hover {
      text-decoration: underline;
      text-decoration-thickness: 2px;
    }
  }
  }
  .containerfor_hero {
    width: 100vw;
    max-width: 1920px;
    height: 0;
    padding-bottom: 50.25%;
    background-color: rgb(10, 10, 10);
    display: flex;
    justify-content: center;
    position: relative;
    margin: 0 auto;
  }
  .menu {
    position: absolute;
    display: flex;
    justify-content: center;
    max-width: 100%!important;
    width: 100%;
    top: 5vh;
    height: 50px;
    z-index: 99;
    background-color: transparent;
    .heroPrice{
      margin-top: .7vw;
      right: 0;
      position: relative;
      width: 100%;
      max-width: 1171px;
      margin-right: -15%;
      display: block;
      height: 50px;
    }
    .price-erp {
     // background-color: aqua;
      padding-right: 10px;
      font-style: italic;
      font-weight: 300;
      font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 1rem;
      sup.new {
       color: white;
       font-weight: 700;
      }
    }
    .call-to-action{
      background-color: transparent;
      border: 1px solid #9bf00b;
      margin-left: 10px;
      span.ndCheck {
        position: relative;
        right: 0;
        background-color: transparent;
        color: #9bf00b;
        font-size: .95rem;
    }
    .play-glyph3 {
      margin-left: 10px;
      vertical-align: middle;
    }
    }
    p {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-weight: 700;
      height: 100%;
      display: flex;
      align-items: center;
      color: white;
      font-size: 17px;
      width: calc(20% + 13px);
      padding-left: calc(5% + 13px);
    }
      .links{
    font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 600;
    list-style-type: none;
    height: 100%;
    width: 70%;
    max-width: 40%;
    margin-left: -1rem;
    color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
}
  .videosrc {
    position: absolute;
    max-width: 100%;
    min-height: auto;
    top: 0;
    overflow: hidden;
    display: flex;
    justify-content: center;
  }
.text-fadein {
    width: 70%;
    height: 35%;
    position: absolute;
  //  background-color: #0000ff5e;
    display: block;
    max-width: 2048px;
    margin-top: 10%;
    text-align: left;
  .headingXbox {
      position: relative;
      display: block;
      color: white;
      max-width: 35vw;
      font-size: 4.5vw;
      font-family: Segoe Pro Black,sans-serif;
     // https://www.grepper.com/answers/25651/css+system+default+font
      font-weight: 900;
      letter-spacing: -0.01em;
    }
  @media (max-width: 1399px) {
    .headingXbox {
      max-width: 280px;
      line-height: 60px;
    }
  }
    .greenStripe {
      background-color: #9bf00b;
      width: 6%;
      height: 5%;
      position: relative;
      transform: skew(-25deg);
    }
    .powerDreams {
      font-family: -apple-system,BlinkMacSystemFont,"SegoePro",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
      color: white;
      font-size: 2.3vw;
      padding-top: 3%;
      font-weight: 700
    }
    .action-trigger {
      color: white;
      display: inline;
      font-weight: 900;
      text-decoration: none;
      font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
      .play-glyph {
        background-color: transparent;
        border-radius: 60%;
        display: inline-block;
        vertical-align: middle;
        width: 40px;
        height: 40px;
        margin-left: 30px;
        margin-right: 20px;
        border:solid 2px #ccc;
        .play-glyph2 {
        //background-color: transparent;
        display: inline-block;
        vertical-align: middle;
        margin-top: 8px;
        margin-left: 8px;
        }
      }
    }
}
}
</style>
