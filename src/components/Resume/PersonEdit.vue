<template>
	<div class='person-edit'>
		<h1 style="text-align: center">个人信息</h1>
		<span>姓名：</span>
		<input type="text" class="college" v-model="info.name"><br>
		<span>电话：</span>
		<input type="text" class="major" v-model="info.phone"><br>
		<span>邮箱：</span>
		<input type="text" class="degree" v-model="info.mail"><br>
		<span>意向岗位：</span>
		<input type="text" class="start" v-model="info.job"><br>
	</div>
</template>

<script>
import bus from "@/utils/bus.js";
export default {
	name: 'PersonEdit',
	components: {

	},
	data() {
		return {
			info: {
				name: '',
				phone: '',
				mail: '',
				job: '',
			}
		}
	},
	created() {
		bus.$on('bus-info', data => {
			// console.log(typeof data, '114');
			this.info = data;
		});
	},
	beforeDestroy() {
		bus.$off('bus-info');
	},
}
</script>

<style scoped>
</style>