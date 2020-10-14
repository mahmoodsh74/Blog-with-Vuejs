<template>
  <div>
      <h1>{{post.title}}</h1>
      <h4>{{post.body}}</h4>
      <hr>
      <router-link :to="{name:'posts'}">بازگشت به عقب</router-link>
  </div>
</template>
<script>
import Http from 'axios'
export default {
    name:'post',
    data(){
        return{
            postid:this.$route.params.post_id,
            post:{}
        }
    },
    created(){
        this.getPost();
    },
    methods:{
        getPost() {
             Http.get('https://blog-35c3c.firebaseio.com/posts/'+ this.postid + '.json')
            .then(response => {
                this.post = response.data;
            })
            .catch(error =>{
                console.log(error.response.data)
            })
        }
    }
}
</script>
<style >

</style>