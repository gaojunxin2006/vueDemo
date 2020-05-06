<template>

  <div>
    <img class="logo" src="./assets/logo.png" alt="图标">
    <HelloWorld></HelloWorld>
  </div>

</template>




<script>
  import HelloWorld from "./components/HelloWorld";

  export default {
    //映射组件标签
    components:{
      HelloWorld
    }



  }


</script>



<style>
  .logo{
    width: 200px;
    height: 200px;

  }



</style>
