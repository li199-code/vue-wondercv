<template>
	<div class='education-edit'>
		<h1 style="text-align: center">教育经历</h1>
		<span>学校：</span>
		<input type="text" class="college" v-model="item.college"><br>
		<span>专业：</span>
		<input type="text" class="major" v-model="item.major"><br>
		<span>学历：</span>
		<input type="text" class="degree" v-model="item.degree"><br>
		<span>入学年月：</span>
		<input type="text" class="start" v-model="item.start"><br>
		<span>毕业年月：</span>
		<input type="text" class="end" v-model="item.end">
	</div>
</template>

<script>
import bus from "../../utils/bus.js";
export default {

	name: 'Education-edit',
	components: {

	},
	data() {
		return {
			item: {
				college: '',
				major: '',
				degree: '',
				start: '',
				end: '',
			}

		}
	},

	created() {
		bus.$on('bus-item', data => {
			this.item = data;
		});
	},
	beforeDestroy() {
		bus.$off('bus-item');
	},

}
</script>

<style scoped>
</style>