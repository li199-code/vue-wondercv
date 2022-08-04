<template>
	<div class='education'>
		<div class="item-head">
			<div class="item-head-left">
				<span style="font-weight: bold">教育经历</span>
			</div>
			<div class="item-head-right">
				<button class="add" @click="add">+</button>
			</div>
		</div>
		<div class="split-line"></div>
		<div class="content">
			<div class="item" v-for="(item, index) in lists" @click="busFun(item)">
				<span class="item-left">
					<span class="college" style="font-weight: bold">{{ item.college }}</span>
					<span> - </span>
					<span class="major">{{ item.major }}</span>
					<span>&nbsp</span>
					<span class="degree">{{ item.degree }}</span>
				</span>
				<span class="item-right">
					<span class="start">{{ item.start }}</span>
					<span> - </span>
					<span class="end">{{ item.end }}</span>

				</span>
				<button class="remove" @click="remove(index)">-</button>
			</div>
		</div>
	</div>
</template>

<script>
import bus from "@/utils/bus.js";
export default {

	name: 'Education',
	components: {

	},
	data() {
		return {
			lists: [
				{
					college: '南京邮电大学',
					major: '控制科学与工程',
					degree: '硕士',
					start: '2020-09',
					end: '2023-06',
				},
			],
		}
	},
	methods: {
		busFun(item) {
			// 通过 $emit 来触发方法，参数1 是定义方法名，参数2 是你要发送的数据
			bus.$emit('bus-item', item)
		},
		newItem: function () {
			this.college = 'xxx';
			this.major = 'xxx';
			this.degree = 'xx';
			this.start = '20xx-xx';
			this.end = '20xx-xx';
		},
		add() {
			this.lists.push(new this.newItem());
		},
		remove(index) {
			this.lists.splice(index, 1)
		}
	}

}
</script>

<style scoped>
.education {
	padding: 20px 0;
}

.education:hover {
	background-color: #eee;
}

.item {
	display: flex;
	justify-content: space-between;
	padding-top: 10px;
}

.item-head {
	display: flex;
	justify-content: space-between;
}

.split-line {
	border-bottom: 2px solid #000;
	padding-top: 4px;
}

.education .add {
	display: none;
	font-size: 20px;
	font-weight: bold;
}

.education:hover .add {
	display: block;
}

.remove {
	display: none;
}

.item:hover .remove {
	display: block;
}
</style>