<template>
	<div class='project'>
		<div class="item-head">
			<span style="font-weight: bold">项目经历</span>
			<div style="border-bottom: 2px solid #000; padding-top: 4px;"></div>
		</div>
		<div class="content">
			<div class="item">
				<span class="projectname">blog</span>
				<span class="date">2022.7-2022.8</span>
				<div class="describe">
					项目描述：支持求职者搜索和筛选岗位，以及企业发布岗位
					项目设计：
					1.基于Vue3.0+TypeScript实现，页面采用flex布局，单页面应用
					2.使用axios封装网络请求与响应，并使用Mockjs拦截axios请求，根据筛选返回模拟数据，完成前后端交互逻辑
				</div>
			</div>
		</div>

	</div>
</template>

<script>

export default {
	name: 'Project',
	components: {

	}
}
</script>

<style scoped>
.project {
	padding: 20px 0;
}

.item {
	/* display: flex;
	justify-content: space-between; */
	padding-top: 10px;
}

.date {
	float: right;
}
</style>