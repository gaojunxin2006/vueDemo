<template>

  <div class="col-md-8">
    <h3 class="reply">评论回复：</h3>
    <h2 v-show="com2.length==0">暂无评论，点击左侧添加评论！！！</h2>
    <ul class="list-group">
     <Item v-for="(com3,index) in com2" :key="index" :com3="com3" :deleteAppCom2="deleteAppCom2" :index="index"/>
    </ul>
  </div>

</template>


<script>
  import Item from "./Item";

    export default {

      //声明接收属性  这个属性就会成为组件对象的属性，可以在模板当中读取
      props:['com2','deleteAppCom2'],
      components:{
        Item
      }




    }


</script>


<style>
  .reply {
    margin-top: 0px;
  }



</style>
