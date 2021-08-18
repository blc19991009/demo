<template>
	<div id="app">
		<div class="nihao" style="width: 100px; height: 100px; border: 1px solid black;" v-for="(item,index) in dataList" :key="item">
			<div v-loading="item.status">
				{{item.name}}{{index}}
			</div>
		</div>
	</div>
</template>

<script>

	export default {
		watch:{
			
		},
		data() {
			return {
				update: true,
				flag: false,
				dataList: [{
					name: '王耀',
					sushe: '601',
					age: '22',
					status:true
				}, {
					name: '马路辰',
					sushe: '601',
					age: '22',
					status:false
				}],
				urls: [
					'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
					'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
					'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
					'https://fuss10.elemecdn.com/9/bb/e27858e973f5d7d3904835f46abbdjpeg.jpeg',
					'https://fuss10.elemecdn.com/d/e6/c4d93a3805b3ce3f323f7974e6f78jpeg.jpeg',
					'https://fuss10.elemecdn.com/3/28/bbf893f792f03a54408b3b7a7ebf0jpeg.jpeg',
					'https://fuss10.elemecdn.com/2/11/6535bcfb26e4c79b48ddde44f4b6fjpeg.jpeg'
				]
			}
		},
		methods: {
			reload() {
				// 移除组件
				this.update = false
				// 在组件移除后，重新渲染组件
				// this.$nextTick可实现在DOM 状态更新后，执行传入的方法。
				this.flag = true
				this.$nextTick(() => {
					this.update = true

					this.flag = false


				})
			}
		}
	}
</script>

<style>

</style>

<!-- <template>
   <div>
     <h4>测试computed</h4>
     <div>
       <input type="text" v-model="message" />
       <span>{{defdata}}</span>
     </div>
     <div>setter</div>
 
   </div>
 
 </template>
 
 <script>
    export default {
     data () {
        return {
          message: 'hello'
        }
      },
     computed: {
        // def () {
        //   return 'dfd'
        // },
        defdata () {
          console.log(this.message) // message被改变的时候，这里会被执行；并重新赋值defdata变量
          return 'dfd' +this.message
        }
      }
   }
 </script> -->
