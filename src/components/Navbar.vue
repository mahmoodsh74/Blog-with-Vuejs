<template>
    <nav class="navbar navbar-default">
        <div class="container-fluid">
            <div class="navbar-header">
                <a class="navbar-brand" href="#">Vue js</a>
            </div>
            <ul class="nav navbar-nav">
                <li><router-link :to="{name:'posts'}" exact>صفحه اصلی</router-link></li>
                <li><router-link :to="{name:'insert'}" exact>افزودن نوشته</router-link></li>
            </ul>
        </div>
    </nav>
</template>
<script>
export default {
    name:'navbar'
}
</script>
<style>
.router-link-active{
color:#555;
background-color: #e7e7e7;
}
</style>