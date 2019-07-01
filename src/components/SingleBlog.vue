<template>
	<div id="single-blog">
		<h1>{{blog.title}}</h1>
		<article>body：{{blog.body}}</article>
		<article>作者：{{blog.author}}</article>
		<p>内容：{{blog.content}}</p>
		<p>分类：</p>
		<ul>
          <li v-for="category in blog.categories" :key="category">{{category}}</li>
        </ul>
        <button @click="deleteSingleBlog()">删除</button>
        <router-link :to="'/edit/'+id">编辑</router-link>
	</div>
</template>

<script>
	export default{
		name:"single-blog",
		data(){
			return{
				id:this.$route.params.id,
				blog:{}
			}
		},
		created(){
			this.$http.get("http://localhost:3000/posts/"+this.id)
			.then(function(data){
				//console.log(data);
				this.blog=data.body;
			})
		},
		methods:{
			deleteSingleBlog(){
				this.$http.delete("http://localhost:3000/posts/"+this.id)
				.then(response=>{
					this.$router.push({path:'/'})
				})
			}
		}
	}
</script>

<style>
#single-blog{
	max-width: 960px;
	margin: 0 auto;
	padding: 20px;
	background: #eee;
	border:1px dotted #aaa;
}
#show-blogs{
	max-width: 800px;
	margin: 0 auto;
}
</style>











