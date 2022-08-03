<template>
	<div class='education'>
		<div class="item-head">
			<span style="font-weight: bold">教育经历</span>
			<div style="border-bottom: 2px solid #000; padding-top: 4px;"></div>
		</div>
		<div class="content">
			<div class="item">
				<span class="item-left">
					<span class="college" style="font-weight: bold">南京邮电大学</span>
					<span> - </span>
					<span class="major">控制科学与工程</span>
					<span>&nbsp</span>
					<span class="degree">硕士</span>
				</span>
				<span class="item-right">
					<span class="start">2020.09</span>
					<span> - </span>
					<span class="end">2023.06</span>
				</span>
			</div>
			
		</div>
	</div>
</template>

<script>

export default {
 name: 'Education',
 components: {

 }
}
</script>

<style scoped>
.education {
	padding: 20px 0;
}
.item {
	display: flex;
	justify-content: space-between;
	padding: 5px 0;
}
</style>