<template lang="pug">
.xboxMenu-container
  img.microsoft-image(src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE1MmB8?ver=6c43g", alt="Microsoft logo")
  img.xbox-image(src="https://img-prod-cms-rt-microsoft-com.akamaized.net//cms/api/am/imageFileData/RW8TP2?ver=d2e0", alt="xbox logo")
  nav.top-menu-nav
    ul
      li.nested-menu
        button.dropdownMenuButton( re="menu") Game Pass
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          li
            a.menu-nav-link(href="#xbox game pass") Join Game Pass
          li
            a.menu-nav-link(href="#brows games") Browse Games
          li
            a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
          li
            a.menu-nav-link(href="#PC Game Pass") PC Game Pass
          li
            a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
          li
            a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        button.dropdownMenuButton( re="menu") Games
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title2 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title3 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        button.dropdownMenuButton( re="menu") Devices
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title2 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title3 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        a.dropdownMenuButtonplay( re="menu") Play
      li.nested-menu
        button.dropdownMenuButton( re="menu")
          span.Community Community
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title2 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title4 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title3 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        button.dropdownMenuButton( re="menu")
          span.Community Support
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title0 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        button.dropdownMenuButton( re="menu")
          span.Community My Xbox
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title0 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
      li.nested-menu
        button.dropdownMenuButton( re="menu")
          span.Community Developers
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title0 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
    ul.left-side-nav
      li.nested-menu
        button.dropdownMenuButton( re="menu")
          span.Microsoft All Microsoft
          svg.arrow-glyph
            polygon(points="0,0 4,4 8,0 4,4 0,0" style="fill:transparent;stroke:white;stroke-width:0.5")
        ul.dropdown-GamePass
          .title Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title2 Console Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title4 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
        ul.dropdown-GamePass
          .title3 All Games
            li
              a.menu-nav-link(href="#xbox game pass") Join Game Pass
            li
              a.menu-nav-link(href="#brows games") Browse Games
            li
              a.menu-nav-link(href="#Game Pass Ultimate") Game Pass Ultimate
            li
              a.menu-nav-link(href="#PC Game Pass") PC Game Pass
            li
              a.menu-nav-link(href="#Xbox Cloud Gaming") Xbox Cloud Gaming (Beta)
            li
              a.menu-nav-link(href="#Xbox Live Gold") Xbox Live Gold
</template>
<script>
export default {
  name: 'xboxMenu',
  computed: {
    isMain () {
      return this.$store.state.site === 'main'
    }
  }
}
// Vue({
//   el: '#app',
//   data: {
//     openClose: false
//   },
//   methods: {
//     toggleDropdown () {
//       this.openClose = !this.openClose
//     }
//   }
// })
</script>
<style lang="scss" scoped>
.xboxMenu-container{
  width: 100vw;
  max-width: 1920px;
  height: 4vh;
  display: flex;
  position: absolute;
  align-items: center;
  z-index: 100;
  top: 0;
  background-color: transparent;
  .microsoft-image{
    width: 6%;
    margin-left: 100px;
  }
  .xbox-image {
    width: 4%;
    margin-left: 3%;
  }
  .top-menu-nav {
    margin: 0 3%;
    z-index: 100;
  }
  .left-side-nav{
    margin-left: 100px;
  }
  ul{
    list-style: none;
    display: inline-flex;
    background-color: transparent;
    justify-content: center;
    align-items: center;
    height: 4vh;
    padding: 0;
    margin-bottom: 0;
  }
  li.nested-menu{
    display: inline-flex;
    position: relative;
    z-index: 10;
    .dropdownMenuButton{
      border: transparent;
      background-color: transparent;
      color: white;
      font-weight: 300;
      font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
      font-size: .85rem;
      display: inline-block;
      padding: 0;
      width: 6rem;
      height: 4vh;
    }
    .title{
      background-color: orange;
      margin-left: 100%;
      width: 100%;
    }
    .title2{
      background-color: rgb(173, 75, 119);
      margin-left: 200%;
      width: 100%;
    }
    .title4{
      background-color: rgb(118, 126, 178);
      margin-left: 300%;
      width: 100%;
    }

   ul.dropdown-GamePass {
      background-color: rgb(75, 70, 70);
      position: absolute;
      width: 100%;
      height: 330px;
      z-index: 990;
      display: none; // change to none
      li {
        display: block;
        z-index: 10;
      }
      li a{
        display: block;
        padding: 18px 25px;
        color: rgb(255, 255, 255);
        text-decoration: none;
        text-align: left;
        font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
        font-size: .8rem;
        height: 55px;
      }
      li a:hover {
        background: rgb(56, 56, 56);
        text-decoration: underline;
      }
    }
    .arrow-glyph {
      background-color: transparent;
      position: relative;
      display: inline;
      width: 10px;
      height: 10px;
      vertical-align: text-bottom;
      margin-left: 7px;
      z-index: 999;
    }
  }
  ul li:hover .dropdownMenuButton {
    background-color: rgb(27, 27, 27);
    padding: 1px;
  }
  ul li:hover ul.dropdown-GamePass {
    margin-top: 4vh;
    display: block;
    width: 200px;
    left: 0;
    padding: 0;
  }
  ul li:hover {
    background-color: rgb(27, 27, 27);
  }
  a.dropdownMenuButtonplay{
    width: 40px;
    color: white;
    font-weight: 300;
    font-family: 'SegoePro', Tahoma, Geneva, Verdana, sans-serif;
    font-size: .85rem;
    display: inline;
    margin-left: -10px;
    text-decoration: none;
  }
  a.dropdownMenuButtonplay:hover {
    text-decoration: underline;
    background-color: transparent;
    border: transparent;
  }
}
</style>
