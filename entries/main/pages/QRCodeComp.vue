<template lang="pug">
.QRCode
    //- Title based on window size. If SSR, this will prevent cumulative layout shift.
  
     //- button(@click="causeError") Cause Error 
      nuxt-link.btn(to="/sample") Sample Page
      ButtonCounter
      
     
    <body class ="backG"> 
      <div class = "border">
        <img class ="picture" src="@/assets/images/image-qr-code.png" width ="288" height="288" >
        <p class = "attribution"> Improve your front-end skills by building projects
        <p class= "secText"> Scan the QR code to visit Frontend Mentor and take your coding skills to the next level </p>
      </div>
    </body>
</template>

<style lang="scss" scoped>
.picture {
  display: flex;
  align-items: center;
  border-radius: 10px;
  justify-content: center;
  margin-top: 16px;
}
.border {
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  border-radius: 18px;
  justify-content: center;
  align-items: center;
  width: 320px;
  height: 495px;
}
.attribution {
  font-stretch: expanded;
  font-family: 'Outfit', sans-serif;
  font-weight: bold;
  font-size: 22px;
  text-align: center;
  margin-inline: 25px;
  margin-top: 25px;
  line-height: 28px;
}
.secText {
  font-family: 'Outfit', sans-serif;
  font-size: 15px;
  text-align: center;
  margin-inline: 30px;
  margin-top: 0px;
  margin-bottom: 37px;
  color: rgb(159, 161, 170);
  line-height: 19px;
  word-spacing: 0.04em;
}
.backG {
  background-color: #d5e1ef;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
}
</style>
