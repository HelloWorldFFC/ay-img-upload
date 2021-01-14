<template>
	<view >
		<imgUpload :themeColor="themeColor" :list="uploadTipList" @imgAdd="imgAddFun" ></imgUpload>
		
	</view>
</template>

<script>
	import imgUpload from '@/components/ay-img-upload/ay-img-upload.vue';
	export default {
		components: {
			imgUpload,

		},
		data() {
			return {
				themeColor : '#33CCCC',
				uploadTipList : [
					{
						name : '凭证1',
						img :'',
						remove : true ,
					},
					{
						name : '凭证2',
						img :'',
						remove : true ,
					},
					{
						name : '凭证3',
						img :'',
						remove : true ,
					},
				],
			}
		},
		onLoad() {
			let that = this;

		},

		methods: {
			imgAddFun(e) {
				let that = this;
				console.log(e)
				//固定一定数量的上传几张图的场景，有一张图的img是空的表示没上传
				that.uploadTipList = e;
			},
		}
	}
</script>

<style lang="scss">
</style>
