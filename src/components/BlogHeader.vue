<template>
	<nav>
		<ul>
			<li>
				<router-link to="/" exact>博客</router-link>
				<router-link to="/add" exact>写博客</router-link>
			</li>
		</ul>
	</nav>
</template>


<script>
	export default{
		name:"blog-header"
	}
</script>


<style>

.single-blog{
padding: 20px;
margin: 20px 0;
box-sizing: border-box;
background: #eee;
border-radius: 1px dotted #aaa;
}
</style>

