### VE 视频引擎渲染基础文档

## 名词概念解释

1. VE视频模板(Template)

  VE视频模板是指设计师在After Effects中制作，利用VE设计师工具(VE Exporter)编辑导出的可以用于用户修改并渲染生视频文件
  或者实时在屏幕上预览修改效果的视频素材和动画数据文件包。  

  一个模板文件包通常由以下几个部分组成：

  *	assets文件夹		  -->包含模板渲染所使用的所有素材文件

  *	datas文件夹		      --> 包含所有动画数据文件

  *	ui文件夹			  -->包含编辑界面需要的一些素材文件，不参与渲染

  *	config.json文件	      -->模板主配置文件，这里包含了模板的渲染结构和素材列表  

2.	素材(Asset)  

	素材是指设计师在设计模板时使用的，或者用户修改模板时提供的图片、视频和文字图片文件

  

3.	图层(Layer)  

	图层就是用来显示一个用户素材及其附加的动画、特效数据的层。用户可以控制图层所使用的素材文件和是否显示灯状态。  



4.	合成(Composition，简称Comp)  

	合成是After Effects中用来制作一段视频的基本框架容器。VE视频引擎SDK里也建立了完整的合成对象模型。
	每个合成里有其自己的时间轴和多个用户显示素材和动画的图层。典型合成包括代表诸如音视频素材图层、
	动画文本静止图像之类的组件的多个图层。然后在合成内为各个图层添加变换动画和特效插件，
	并使用透明度混合等颜色混合模式来对各个图层的内容进行混合形成最终画面  



5.	素材源合成(Source Composition，简称SourceComp)  

	素材源合成是合成的一个子类，在动态模板中，用户提供的素材会被包含到一个特殊的合成中，这个合成会自动对用户提供的图片素材
	进行调整以填充合成的宽高。  



6.	片段合成(Segment Composition，简称Segment)  

	在动态模板中，用户的提供的素材会被存放到SourceComp中，然后SourceComp会被添加到片段合成中添加动画效果以及和其他素材的混合。
	一个片段合成可以包含1到多个SourceComp来同时进行动画  



7.	AV素材(AVSource)  

	用户的素材被称为Asset，当用户的素材被某个图层使用来显示绘制的时候，Asset对象会被转化为AVSource对象。
	AVSource对象是一个更加底层的用于管理素材像素内容的对象。  



8.	UI标记(UI Key)	  

	为了方便开发者对模板进行自定义修改，VE设计师工具允许设计师在对模板进行导出到时候对素材(Asset)和图层(Layer)添加字符串类型的UI标记，
	开发者可以调用相应的接口通过提前设置的UI标记获取被标记的素材或图层  



9.	附加数据(Extra Data)  

	客户在对素材和图层添加自定义的UI标记的同时也可以添加自定义的附加数据。附加数据也是字符串的形式。
	SDK提供接口获取指定素材和图层的附加数据
	
	
	
