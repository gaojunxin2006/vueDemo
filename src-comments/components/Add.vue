<template>

  <div class="col-md-4">
    <form class="form-horizontal">
      <div class="form-group">
        <label>用户名</label>
        <input type="text" class="form-control" placeholder="用户名" v-model="name">
      </div>
      <div class="form-group">
        <label>评论内容</label>
        <textarea class="form-control" rows="6" placeholder="评论内容" v-model="content"></textarea>
      </div>
      <div class="form-group">
        <div class="col-sm-offset-2 col-sm-10">
          <button type="button" class="btn btn-default pull-right" @click="add">提交</button>
        </div>
      </div>
    </form>
  </div>

</template>


<script>
    export default {

      props:{
        addAppCom2:{
          type:Function,
          required:true,
        }

      },

      data(){
        return {
          name:'',
          content:'',
        }
      },

      //绑定事件监听
      methods:{
        add(){
          alert("add.vue中的方法 ，你点击了提交！");

          //1.检查输入合法性
          const name=this.name.trim();
          const content=this.content.trim();

          if (!name||!content){
            alert("add.vue 你输入的姓名内容不能为空");
            return
          }

          //2.根据输入的数据封装成一个com2对象
          const com2={
            name,
            content,
          }

          //3.添加到com2中
          this.addAppCom2(com2);


          //4.清除输入内容
          this.name='';
          this.content='';

        }


      }



    }


</script>


<style>


</style>
