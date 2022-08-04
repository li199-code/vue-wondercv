<template>
	<div class='person' @click="busFun">
		<div class="name">{{ info.name }}</div>
		<span class="phone">{{ info.phone }}| </span>
		<span class="email">{{ info.mail }}| </span>
		<span class="job">{{ info.job }}</span>
	</div>
</template>

<script>
import bus from "@/utils/bus.js";
export default {
	name: 'Person',
	components: {

	},
	data() {
		return {
			info: {
				name: '李丰耀',
				phone: '18168039401',
				mail: 'lifengyao1510@163.com',
				job: 'web前端'
			},
		}
	},
	methods: {
		busFun() {
			// 通过 $emit 来触发方法，参数1 是定义方法名，参数2 是你要发送的数据
			bus.$emit('bus-info', this.info)
		},
	}
}
</script>

<style scoped>
.person {
	text-align: center;
	padding: 20px 0;
}

.name {
	padding-bottom: 10px;
	font-size: 20px;

}

.person:hover {
	background-color: #eee;
}
</style>