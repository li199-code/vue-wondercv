<!-- 在这里编辑简历及预览、输出 -->

<template>
	<div class="edit">
		<ResumeEdit></ResumeEdit>
		<Resume></Resume>
	</div>
</template>

<script>
import Resume from '@/components/Resume/Resume.vue'
import ResumeEdit from '@/components/Resume/ResumeEdit.vue'
export default {
	name: 'EditView',
	components: {
		Resume,
		ResumeEdit
	},
	beforeCreate() {
		document.querySelector('body').setAttribute('style', 'background:rgb(53, 57, 68)')
	},
	// 在销毁前，将body的style属性删除
	beforeDestroy() {
		document.querySelector('body').removeAttribute('style')
	},
}
</script>

<style scoped>
.edit {
	display: flex;
	justify-content: center;
}
</style>
