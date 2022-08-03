<!-- 首页，新建简历和已创建简历目录 -->

<template>
  <div class="home">
		<button class="new">New</button>
		<Main></Main>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  components: {

  },

}

</script>

<style scoped>

.home{
	display: flex;
	justify-content: center;
}
.new {
	height: 50px;
	width: 200px;
	background-color: rgb(255, 102, 68);
	color: #fff;
	border-radius: 5px;
	border: none;
}
</style>
