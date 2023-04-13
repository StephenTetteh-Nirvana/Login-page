<template>
  <div class="container">
    <div class="img">
      <h1>Student's Registry</h1>
      <ButtonComp />
    </div>
  </div>
 
</template>

<script>
import ButtonComp from './components/ButtonComp.vue'
export default {
  name: 'App',
  components:{
    ButtonComp,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Tilt+Prism&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
   -moz-osx-font-smoothing: grayscale;
}
*{
margin:0px;
padding:0px
}
.container{
  width:100%;
  height:100vh;
  overflow:hidden;
}
h1{
  color:#f0ebeb;
  font-family:'Tilt Prism';
  font-size:50px;
  margin-left:25px;
  padding-top:10px;
}
.img{
    background-image:linear-gradient(rgba(48, 47, 47, 0.75),rgba(7, 3, 3, 0.75)),url(../background/wallpaper.jpg);
    background-repeat:no-repeat;
    background-position:center;
    background-size:cover;
    height: 100vh;
    width: 100%;
}
</style>
