<template>

  <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <h1>请发表对Vue的评论</h1>
          </div>
        </div>
      </div>
    </header>
    <div class="container">
      <Add :addAppCom2="addAppCom2"/>
      <List :com2="com2" :deleteAppCom2="deleteAppCom2"/>
    </div>
  </div>

</template>


<script>
  import Add from "./components/Add";
  import List from "./components/List";
    export default {

      data(){
        return {
          com2:[
            {
              name:'周杰伦',
              content:'我是歌手',
            },
            {
              name:'谢霆锋',
              content:'我是厨师',
            },
            {
              name:'黄渤',
              content:'我是演员',
            }
          ]

        }

      },

      components:{
        Add,
        List


      },
      methods:{
        //添加评论
        addAppCom2(com2){
          alert("这是app.vue中的方法");
          this.com2.unshift(com2);
        },

        //删除评论，根据下标
        deleteAppCom2(index){
          this.com2.splice(index);
        }

      }


    }


</script>


<style>
  .handle {
    width: 40px;
    border: 1px solid #ccc;
    background: #fff;
    position: absolute;
    right: 10px;
    top: 1px;
    text-align: center;
  }

  .handle a {
    display: block;
    text-decoration: none;
  }

  .list-group-item .centence {
    padding: 0px 50px;
  }

  .user {
    font-size: 22px;
  }


</style>
