<template lang="pug">
.sec3fullcontain
  .sec3-contentcontainer
    img.masterchief(src="https://assets.xboxservices.com/assets/87/55/8755d55b-6e23-48c9-9da8-7c7c2e4f9d29.jpg?n=XBX_A-Poweryourdreams_Background-D.jpg", alt="master chief standing")
  .power-dreams POWER YOUR
    span DREAMS
  .stagger-module
    .margin
      .background-border
      img.aliens(src="https://assets.xboxservices.com/assets/74/98/74989534-4eb2-48f1-9428-d9df92be31d5.jpg?n=Xbox-Series-X_Power-Your-Dreams_Optimized_1084_536x480.jpg", alt="aliens from destiny")
      .textcontain4SMfoto
        .size-image-text
          img.series-xs(src="https://assets.xboxservices.com/assets/6d/b1/6db18f33-26f4-48f5-ad3c-f56f504e8ec0.svg?n=XBX_A-PowerYourDreams_Optimized-Icon-FPO.svg", alt="series XS logo")
          .optomizetext OPTOMIZED FOR SERIES X|S
          .reduceloadtimestext Games built with the
            span  Xbox Series X|S development kit showcase significantly reduced load times and stunning visuals at up to 120FPS.
              a.hyperlink(href="#prices")
                sup *
          a.learnmore(href="https://www.xbox.com/en-US/games/optimized")  LEARN MORE
            svg.play-glyph3(height="15" width="10")
              polygon(points="0,0 3,0 6,6 3,11 0,11 4,6")
      img.destiny(src="https://assets.xboxservices.com/assets/7f/8c/7f8c3471-9662-4806-9689-7049cab37f3b.jpg?n=Xbox-Series-X_Power-Your-Dreams_Smart-Delivery_1084_536x480_02.jpg", alt="destiny characters")
      .textcontain-destiny
        .size-image-text
          img.smartdel-logo(src="https://assets.xboxservices.com/assets/5d/f0/5df057a4-fbdc-4f53-b0de-ca92bdb332c5.svg?n=XBX_A-PowerYourDreams_SmartDelivery-IconB-T.svg", alt="smart delivery logo")
          .optomizetext GET IT ONCE
          .reduceloadtimestext With Smart Delivery, you can buy a supported game once and always have the best available version for whatever console you play on.
      img.halo-cds(src="https://assets.xboxservices.com/assets/08/d1/08d10ecc-009b-49cf-be1d-a40c787323de.jpg?n=XBX_A-PowerYourDreams_NoGamesLeftBehind-ImageC-D_02.jpg", alt="halo masterchief CDs")
      .black-overlay
      .textcontain-halocds
        .size-image-text
          .optomizetext GAME ON
          .reduceloadtimestext From future adventures, to current obsessions, to classic titles, thousands of favorites across four generations of Xbox look and play best on Xbox Series X.
    .fade-to-black
</template>
<script>
import { gsap } from 'gsap'
export default {
  name: 'ContentSection3', // not sure why important
  computed: {
    isMain () {
      return this.$store.state.site === 'main'
    }
  },
  mounted () {
    gsap.to('.fade-to-black', {
      scrollTrigger: {
        trigger: '.fade-to-black',
        scrub: true,
        start: 'top top',
        end: 'bottom center'
        // markers: true
      },
      opacity: 0.7
    })
    gsap.to('.background-border', {
      scrollTrigger: {
        trigger: '.fade-to-black',
        scrub: true,
        start: 'center+=500 center',
        end: 'bottom+=200 center'
        // markers: true
      },
      opacity: 0.3,
      backgroundColor: 'rgb(70, 70, 70)'
    })
    gsap.to('.sec3-contentcontainer', {
      scrollTrigger: {
        trigger: '.sec3-contentcontainer',
        scrub: true,
        start: 'top center',
        end: 'center+=10 center'
        // markers: true
      },
      y: 0
    })
    gsap.to('.sec3-contentcontainer', {
      scrollTrigger: {
        trigger: '.sec3-contentcontainer',
        scrub: true,
        start: 'top top',
        end: 'bottom+=920 center',
        pinSpacing: false,
        // markers: {
        //   startColor: 'purple',
        //   endColor: 'white',
        //   fontSize: '1rem',
        //   indent: 900,
        //   fontWeight: 400
        // },
        pin: true
      }
    })
  }
}
</script>

<style lang="scss" scoped>
.sec3fullcontain{
  width: 100%;
  height: 1900px;
  background-color: aqua;
}
.sec3-contentcontainer{
  width: 100%;
  height: 67vw;
  background-color: green;
  position: relative;
  display: flex;
  align-items: baseline;
  justify-content: center;
  z-index: 10;
}
.power-dreams{
  font-size: 4.2vw;
  color: white;
  width: 100%;
  height: 100px;
  z-index: 11;
  display: flex;
  justify-content: center;
  margin-top: -24%;
  position: absolute;
  font-family: Segoe Pro Black,sans-serif;
  span {
    color: #9bf00b;
    margin-left: 1.1vw;
  }
}
.stagger-module{
    width: 100%;
    height: 1800px;
    display: flex;
    position: relative;
    z-index: 15;
    margin-top: -17%;
  }
  .margin {
    width: 90%;
    height: 100%;
    position: relative;
    margin: 0 auto;
    display: flex;
  }
.background-border{
  background-color: rgb(85, 104, 105);
  width: 60%;
  height: 100%;
  position: absolute;
  margin-left: 19%;
  opacity: 0.5;
  border: 2px solid rgb(154, 154, 154);
}
.aliens {
  width: 534px;
  height: 478px;
  z-index: 12;
  position: absolute;
  border: 1px solid rgb(109, 109, 109);
  margin-top: 180px;
}
.destiny {
  width: 534px;
  height: 478px;
  position: absolute;
  margin-top: 640px;
  right: 0;
  border: 1px solid rgb(109, 109, 109);
}
.halo-cds{
  width: 534px;
  height: 478px;
  margin-top: 1150px;
  z-index: 20;
  position: absolute;
  border: 1px solid rgb(109, 109, 109);
}
.black-overlay {
  position: absolute;
  background-color: black;
  opacity: 0.3;
  width: 534px;
  height: 478px;
  margin-top: 1150px;
  z-index: 20;
}
.fade-to-black {
  width: 100%;
  height: 100%;
  background-color: black;
  position: absolute;
  opacity: 0;
  z-index: 16;
  pointer-events: none; /* SVG-only */
}
.reduceloadtimestext {
    font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
    color: white;
    font-size: 24.5px;
    text-align: left;
    max-width: 100%;
    line-height: 28px;
    span {
      display: inline-block;
      line-height: 28px;
    }
  }
  .optomizetext {
    display: flex;
    position: relative;
    font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: bold;
    color: white;
    font-size: 24px;
    line-height: 30px;
    margin-top: 30px;
  }
  .size-image-text {
  width: 375px;
  height: 310px;
  z-index: 20;
  position: absolute;
  display: block;
  }
.textcontain4SMfoto {
  margin-left: 400px;
  margin-top: 250px;
  .series-xs {
    display: flex;
    width: 30%;
  }

  .hyperlink {
      sup{
        display: inline;
        vertical-align: top;
        font-size: 22px;
        font-family: Segoe Pro Black,sans-serif;
        color: #9bf00b;
        text-decoration: underline;
      }
    }
    .learnmore {
      font-size: 17px;
      font-family: Segoe Pro Black,sans-serif;
      color: #9bf00b;
      text-decoration: none;
      display: flex;
      margin-top: 12px;
      .play-glyph3 {
      margin-left: 10px;
      margin-top: 6px;
      fill: #9bf00b;
      stroke: #9bf00b;
    }
    }
    .learnmore:hover{
      text-decoration: underline;
      text-decoration-thickness: 2px;
      color: #8dc62c;
      .play-glyph3 {
        margin-left: 15px;
        fill: #8dc62c;
        stroke: #8dc62c;
      }
    }
}
.textcontain-destiny {
    // background-color: brown;
    // width: 375px;
    // height: 310px;
    // z-index: 12;
    // position: absolute;
    // display: block;
    margin-top: 700px;
    margin-left: 10%;
    .smartdel-logo {
      display: flex;
    }
  }
  .textcontain-halocds {
    margin-top: 1340px;
    margin-left: -10%;
  }
</style>
