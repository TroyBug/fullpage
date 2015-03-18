# fullpage
基于jQuery的全屏滚动插件

mh.js是jQuery mousewheel插件，目前只支持纵向滚动

在IE6+、Chrome40、Firefox35下测试通过

使用方法：
先引入jQuery库，然后引用插件，最后调用。
$(container).FullPage({
  section:'.section',	//每一屏的容器样式
	active:'active',	//表示当前屏被激活时所用的样式
	container:'.box',	//最外层容器
	controller:'.controlBtns',	//控制器
	speed: 300,	//动画速度
	delay: 600,	//每次滚动完成后的锁屏时间
  callback:function(i) {
			switch (i) {
				case 0:
					document.title = 1;
					break;
				case 1:
					document.title = 2;
					break;
				case 2:
					document.title = 3;
					break;
				case 3:
					document.title = 4;
					break;
				case 4:
					document.title = 5;
					break;
				default:
					break;
			}
		}
});
