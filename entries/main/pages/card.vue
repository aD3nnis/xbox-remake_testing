<template lang="pug">
.Card
   .border
      .alignment
         p.text Get <span> insights </span> that help your business grow.
         p.text2 Discover the benefits of data analytics and make better decisions regarding revenue, customer experience, and overall efficiency.
         //- p.text4 10k+ 314 12M+
         //- p.text3 companies templates queries
         .stats
            p <span>10K+</span> companies
            p <span>314</span> templates
            p <span>12M+</span> queries
      .image-container
//-   <img class = "image" src= "@/assets/images/image-header-desktop.jpg" width ="538" height="448">
</template>

<style lang="scss" scoped>
  // @include media-breakpoint-up(md) {
  //   flex-direction: row;
  // }
.Card {
  background-color: hsl(233, 47%, 7%);
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
  .border {
    display: flex;
    background-color: hsl(244, 38%, 16%);
    align-items: center;
    justify-content: center;
    width: 1079px;
    height: 448px;
    border-radius: 5px;
    overflow: hidden;
    @media screen and (max-width: 768px) {
         background-color: red;
      }
  }

}
.stats {
font-family: 'Lexend Deca', sans-serif;
  font-weight: 400;
  color: hsla(0, 0%, 100%, 0.6);
  word-spacing: 60px;
//   text-align: center;
  margin-left: 40px;
  text-transform: uppercase;
  text-align: left;
  margin-bottom: -85px;
  display: flex;
  flex-direction: row;
}
.stats span {
   font-family: 'Inter', sans-serif;
  font-weight: 500;
  font-size: 23px;
  color: hsl(0, 11%, 88%);
  word-spacing: 87px;
  text-align: left;
  padding-bottom: 5rem;
}
.text {
   display: block;
  // align-items: center;
  text-align: left;
  // flex-wrap: wrap;
  // flex-direction: column;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 34px;
  color: hsl(0, 0%, 100%);
//   max-width: 400px;
  padding-left: 3rem;
  padding-right: 3rem;
  padding-bottom: 3rem;
//   margin-left: 44px;
   margin-top: -3rem;
//   margin-bottom: 28px;
  word-spacing: 5px;
  line-height: 45px;
}
.text span {
  color: rgba(168, 88, 218, 0.7);
}
.text2 {
  // display: flex;
  // align-items: center;
  // justify-content: center;
  // flex-wrap: wrap;
  // flex-direction: column;
  font-family: 'Inter', sans-serif;
  font-weight: 300;
  text-align: left;
  padding-left: 3rem;
  padding-right: 9rem;
  padding-bottom: 3rem;
  margin-top: -2rem;
  font-size: 15px;
  color: hsla(0, 0%, 100%, 0.75);
  line-height: 25px;
}
.image-container {
  flex: 1;
  height: 100%;
  background-image: linear-gradient(
      0deg,
      rgba(168, 88, 218, 0.7),
      rgba(168, 88, 218, 0.7)
    ),
    url('@/assets/images/image-header-desktop.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  // img {
  //   height: 100%;
  //   width: auto;
  // }
}

.alignment {
  display: flex;
  flex-direction: column;
  flex: 1;
}
@media screen and (max-width: 1024px) {
  .Card {
    .border {
      height: 380px;
    }
  .text {
    font-size: 30px;
    padding-top: 120px;
  }
    .stats {
    padding-bottom: 9rem;
  }
  .text2 {
    padding-bottom: 2rem;
    margin-top: -3rem;
    margin-bottom: -1rem;
    margin-right: -5rem;
    font-size: 15px;
  }
 }
}
@media screen and (max-width: 640px) {
        .Card{
          .text {
            font-size: 28px;
          }
          .text2{
            font-size: 15px;
          }
        }
      }
@media screen and (max-width: 768px) {
   .Card {
      .border {
         background-color: hsl(244, 38%, 16%);
         display: flex;
         flex-direction: column-reverse;
         margin-left: 11%;
         margin-right: 11%;
         height: 90%;
      }
         .image-container{
         display: block;
         flex-direction: column;
         width: 100%;
         max-height: 30%;
      }
      .stats{
         text-align: center;
         display: block;
         max-width: min-content;
         line-height: 2rem;
         padding-top: 2rem;
         margin: 0 auto;
      }
      .stats span {
            text-align: center;
            line-height: 3rem;
            font-size: 1.7rem;
      }
      .text {
         display: block;
         text-align: center;
         padding-right: 4rem;
         padding-top: 5rem;
         margin-right: -2rem;
         margin-left: -2rem;
         margin-bottom: -1rem;
         margin-top: -3rem;
      }
       .text2 {
         display: block;
         text-align: center;
         padding-right: 9rem;
         padding-left: 3.5rem;
         padding-bottom: 1rem;
         padding-top: 1rem;
         font-size: 15px;
      }
   }
}
</style>
