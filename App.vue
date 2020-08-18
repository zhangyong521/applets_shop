<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@font-face {font-family: "iconfont";
	  src: url('~@/static/font/iconfont.eot?t=1597709126323'); /* IE9 */
	  src: url('~@/static/font/iconfont.eot?t=1597709126323#iefix') format('embedded-opentype'), /* IE6-IE8 */
	  url('data:application/x-font-woff2;charset=utf-8;base64,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') format('woff2'),
	  url('~@/static/font/iconfont.woff?t=1597709126323') format('woff'),
	  url('~@/static/font/iconfont.ttf?t=1597709126323') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
	  url('~@/static/font/iconfont.svg?t=1597709126323#iconfont') format('svg'); /* iOS 4.1- */
	}
	
	.iconfont {
	  font-family: "iconfont" !important;
	  font-size: 16px;
	  font-style: normal;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	}
	
	.icon-shouye:before {
	  content: "\e601";
	}
	
	.icon-dingdan:before {
	  content: "\e602";
	}
	
	.icon-weibiaoti-1:before {
	  content: "\e603";
	}
	
	.icon-bianji:before {
	  content: "\e605";
	}
	
	.icon-tianjiadingdan:before {
	  content: "\e606";
	}
	
	.icon-dingdanguanli:before {
	  content: "\e607";
	}
	
	.icon-fenlei:before {
	  content: "\e608";
	}
	
	.icon-weibiaoti-6:before {
	  content: "\e609";
	}
	
	.icon-shanchu:before {
	  content: "\e60a";
	}
	
	.icon-dingdanguanli1:before {
	  content: "\e60b";
	}
	
	.icon-tuangou:before {
	  content: "\e60c";
	}
	
	.icon-gerenzhongxin:before {
	  content: "\e60d";
	}
	
	.icon-gengduo:before {
	  content: "\e60e";
	}
	
	.icon-fasongtongzhi:before {
	  content: "\e610";
	}
	
	.icon-dingwei:before {
	  content: "\e615";
	}
	
	.icon-huiyuanguanli:before {
	  content: "\e616";
	}
	
	.icon-shangpinguanli:before {
	  content: "\e617";
	}
	
	.icon-mendianguanli:before {
	  content: "\e618";
	}
	
	.icon-daishouhuo:before {
	  content: "\e61a";
	}
	
	.icon-shouhou:before {
	  content: "\e61c";
	}
</style>
