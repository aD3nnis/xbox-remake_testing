<template lang="pug">
.layout
    p.word no add ons
    p.w2  display: flex
    //- p.w3  display: block
    //- p.w4 display: inline
    //- p.w5 display: grid
    //- p.w6 display: table
    p.w7 display: flex, Justify-content: center
    p.w8 display: flex, Justify-content: center, column

</template>
<style lang="scss" scoped>
.layout {
  .word {
  font-size: 30px;
  background-color: rgb(33, 144, 127);
}
  .w2 {
    display: flex;
    background-color: rgb(182, 182, 194);
    font-size: 30px;
  }
  // .w3 {
  //   display: block;
  //   background-color: rgb(238, 117, 242);
  //   font-size: 30px;
  // }
  // .w4 {
  //   display: inline;
  //   background-color: rgb(213, 150, 151);
  //   font-size: 30px;
  // }
  // .w5{
  //   display: grid;
  //   position: absolute;
  //   background-color: rgb(169, 155, 155);
  //   font-size: 30px;
  // }
  // .w6 {
  //   display:table;
  //   position: absolute;
  //   background-color: rgb(182, 213, 150);
  //   font-size: 30px;
  // }
  .w7 {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    width: 500px;
    background-color: rgb(146, 128, 173);
  }
  .w8 {
    display: flex;
    justify-content: center;
    flex-direction: row;
    font-size: 30px;
    background-color: rgb(231, 191, 210);
  }
}

</style>
