<template>
    <li class="list-group-item">
            <div class="handle">
              <a href="javascript:;" @click="deleC">删除</a>
            </div>
            <p class="user"><span >{{com.content}}</span><span>说:</span></p>
            <p class="centence">{{com.username}}!</p>
          </li>
</template>
<script>
export default {
    name:'',
    props:['com','deleComment','index'],
   methods:{
      deleC(){
      if(confirm('确定要删除吗')){
         this.deleComment(this.index)
      }
     
    }
   }
}
</script>
<style scoped>
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