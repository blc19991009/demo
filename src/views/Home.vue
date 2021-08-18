<template>
	<div class="home">
		<el-button :plain="true" @click="open2">你好</el-button>
		<el-button :plain="true" @click="open3">乱杀</el-button>
		<el-button :plain="true" @click="open1">8层箱子的伤害</el-button>
		<el-button :plain="true" @click="open4">夹子</el-button>
		<div v-for="(item,index) in dataList" :key="index">
			<p>{{item.name}}</p>
			<p>{{item.sushe}}</p>
			<p>{{item.age}}</p>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		props: ['dataList'],
		created() {
			console.log(this.dataList)
		},
		methods: {
			open2() {
				this.$message('hello哇');
			},
			open3() {
				this.$message({
					message:'可恶让你装到了',
					type:'success'
				});
			},
			open1() {
				this.$message({
					message:'对吧，钢铁',
					type:'warning'
				});
			},
			open4() {
				this.$message.error('小风车，大西几，啊吧啊吧啊巴巴');
			}

		}
	}
</script>
<style scoped="scoped">
	.home {
		width: 220px;
		height: 220px;
		background-color: blue;
	}
</style>
