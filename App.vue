<script>
	export default {
		onLaunch: function() {
			console.log('App Launch');
			if (!wx.cloud) {
				console.error('请使用 2.3.0 或以上的基础库以使用云能力');
			} else {
				wx.cloud.init({
					// env 参数说明：
					//   env 参数决定接下来小程序发起的云开发调用（wx.cloud.xxx）会默认请求到哪个云环境的资源
					//   此处请填入环境 ID, 环境 ID 可打开云控制台查看
					//   如不填则使用默认环境（第一个创建的环境）
					// env: 'yuangezhizao-yuangezhizao',
					traceUser: true
				});
			}
		},
		onShow: function() {
			console.log('App Show');
			// uni.setKeepScreenOn({
			// 	keepScreenOn: true
			// });
		},
		onHide: function() {
			console.log('App Hide');
		}
	};
</script>

<style>
/* 解决头条小程序组件内引入字体不生效的问题 */
/* #ifdef MP-TOUTIAO */
@font-face {
	font-family: uniicons;
	src: url('/static/uni.ttf');
}
/* #endif */
</style>
