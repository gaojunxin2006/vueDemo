<template>


      <li class="list-group-item">
        <div class="handle">
          <a href="javascript:;" @click="deletecom2">删除</a>
        </div>
        <p class="user"><span >{{com3.name}}</span><span>说:</span></p>
        <p class="centence">{{com3.content}}</p>
      </li>



</template>


<script>
    export default {
      props:{
        com3:Object,
        deleteAppCom2:Function,
        index:Number,
      },
      methods:{

        deletecom2(){
          alert("item.vue 你点了删除评论");
          var {com3,index,deleteAppCom2} =this;
          if (window.confirm('你确定删除'+com3.name+'下标'+index)){
            deleteAppCom2(index);
          }

        }


      }
    }


</script>


<style>
  li {
    transition: .5s;
    overflow: hidden;
  }

  .user {
    font-size: 22px;
  }

</style>
