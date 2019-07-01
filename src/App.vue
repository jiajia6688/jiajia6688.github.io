<template>
  <div id="app">
      <!-- <add-blog></add-blog> -->
      <!-- <show-blog></show-blog> -->
      <blog-header></blog-header>
      <router-view></router-view>

  </div>
</template>

<script>
import AddBlog from './components/AddBlog'
import ShowBlog from './components/ShowBlogs'
import BlogHeader from './components/BlogHeader'

export default {
  name: 'App',
  components: {
    AddBlog,ShowBlog,BlogHeader
  }
}
</script>

<style>
ul{
	list-style: none;
	text-align: center;
	margin: 0;
}
li{
	display: inline-block;
	margin: 0 10px;
}
a{
	color: #fff;
	border-radius: 5px;
	text-decoration: none;
	padding: 12px;
}
nav{
	background: crimson;
	padding: 30px 0;
	margin-bottom: 40px;
}
.router-link-active{
	background: rgba(255,255,255,0.8);
	color: #444;
}


</style>
