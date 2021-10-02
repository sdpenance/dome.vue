<template>
     <div>
   <Header></Header>
    <div class="container">
    <Left :addComment='addComment'></Left>
    <List :coms='comments'></List>
     
    </div>
  </div>
</template>
<script>
import Header from '@/components/Header.vue'
import Left from '@/components/Left.vue'
import List from '@/components/List.vue'
export default {
    name:'',
    components:{
        Header,
        Left,
        List
    },
    data() {
        return {
            comments:[
                {id:1,content:'vue牛逼',username:"颜伟"},
                {id:2,content:'vue好用',username:"赵丽颖"},
                {id:3,content:'vue可以',username:"杨幂"},
            ]
        }
    },
   methods:{
     addComment(comment){
       this.comments.unshift(comment)
     }
   }
}
</script>