<template>
  <div>
  <Header></Header>
    <div class="container">
    <Add :addComment='addComment'></Add>
    <List :comments='comments' :deleComment='deleComment'></List>
    </div>
  </div>
</template>
<script>
import Header from '@/components/Header.vue'
import Add from '@/components/Add.vue'
import List from '@/components/List.vue'
export default {
  name:'',
  components:{
    Header,
    Add,
    List
  },
  data() {
    return {
      comments:[
        {id:1,content:'真是我的评论',username:'送悟空'},
        {id:2,content:'你真好呀',username:'猪八戒'},
        {id:3,content:'师徒四人',username:'沙僧'},
        {id:4,content:'北国风光',username:'唐僧'},
      ]
    }
  },
  methods:{
    addComment(comment){
      this.comments.unshift(comment)
    },
    deleComment(index){
      this.comments.splice(index,1)
    }
  }
}
</script>
<style scoped>

</style>