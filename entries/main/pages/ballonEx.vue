<template lang="pug">
.container
  p.text Forever Tropical
   <div class="main-tool-bar"></div>
     <div class="scrollable-area"></div>

</template>

<script>
//
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger)
// gsap.defaults({ ease: 'none', duration: 2 })

export default {
  mounted () {
    this.$gsap.to('.container .text', {
      // yPercent: -80,
      scrollTrigger: {
        scrub: true,
        markers: true,
        id: 'hello',
        start: 'center center += 100px', // where in your scrolling it will start to fade away. where the trigger is activated or "triggered."
        end: '+=400px', // not sure what this does
        onEnter: 'play',
        pin: '.text'
      }
    })
    this.$gsap.to('.main-tool-bar', {
      scrollTrigger: {
        markers: {
          startColor: 'purple',
          endColor: 'fuchsia',
          fontSize: '4rem',
          indent: 300,
          fontWeight: 'bold'
        },
        scrub: true,
        id: 'world',
        // HOW DO I MAKE START BELOW A FUNCTION OF END FROM ABOVE?
        start: 'center center' + '-=400px', // where in your scrolling it will start to fade away. where the trigger is activated or "triggered."
        end: 'bottom bottom'
      },
      y: -800,
      ease: 'Power0.easeNone'
    }
    ) // .progress(1)

    // onEnter - scrolling down, start meets scroller-start
    // onLeave - scrolling down, end meets scroller-end
    // onEnterBack - scrolling up, end meets scroller-end
    // onLeaveBack - scrolling up, start meets scroller-start

    // ScrollTrigger.create({
    //   start: 10, // where in your scrolling it will start to fade away. where the trigger is activated or "triggered."
    //   end: 99999, // not sure what this does
    //   scrub: true //
    // onUpdate: (self) => {
    //   self.direction === -1 ? showAnim.play() : showAnim.reverse()
    // }

    // })
  }
}
</script>
<style>
body {
  font-family: sans-serif;
  font-weight: 400;
  margin: 0;
  padding: 0;
}
.container {
  background-color: bisque;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.main-tool-bar {
  height: 900px;
  background: url("@/assets/images/photo_of_Beach.jpeg");
  background-size: cover;
   display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  width:100%;
  left: 0;
  top: 0;
}
.text {
  display: flex;
  font-family: fantasy ;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: #655c5c;
  font-size: 3rem;
  z-index: 1;
  width: 100%;
}

.scrollable-area {
  height: 300vh;
}</style>
