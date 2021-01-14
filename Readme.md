
## 前言
简介：上传图片通用组件，固定一定数量的上传几张图的场景，有一张图的img是空的表示没上传，直接引用

## 有疑问
微信搜索“慢慢向好”小程序，找客服反馈，相应问题。
				  

## 素材
[图片资源](https://pixabay.com)
 
## 开始使用
下载源码解压，复制`/components` 下的组件至项目根目录的 `/components` 文件夹下


`index.vue`的`script`加入如下部分：
```
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
```


`index.vue`的`template`加入如下部分：
```
<view >
		<imgUpload :themeColor="themeColor" :list="uploadTipList" @imgAdd="imgAddFun" ></imgUpload>
		
	</view>

```

## 参考插件
[参考插件](https://ext.dcloud.net.cn/plugin?id=2922)
[参考插件](https://ext.dcloud.net.cn/plugin?id=594)


 