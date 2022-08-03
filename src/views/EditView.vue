<!-- 在这里编辑简历及预览、输出 -->

<template>
  <div class="edit">
		<Resume></Resume>
  </div>
</template>

<script>
import Resume from '@/components/Resume/Resume.vue'
export default {
	name:'EditView',
	components:{
    Resume
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

</style>
