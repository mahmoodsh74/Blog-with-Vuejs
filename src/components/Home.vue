<template>
    <div>
        <navbar></navbar>
        <router-view></router-view>
    </div>
</template>
<script>
// import AddPost from './AddBlog';
// import Posts from './Posts';
import navbar from './Navbar';
export default {
    name: 'home',
    components: {
        // 'posts':Posts,
        // 'add-post':AddPost,
        'navbar':navbar
    }
}
</script>
<style >

</style>