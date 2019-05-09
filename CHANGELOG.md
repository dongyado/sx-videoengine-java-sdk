# VE 视频渲染引擎 java sdk
### 1.3.7
+ 修复 ffmpeg stream copy 不能使用 filter_complex 

### 1.3.6 
+ 新增添加水印
+ 新增设置音乐淡出时间
+ 新增设置音乐音量

### 1.3.5
+ 为 VeProcessRenderTask 增加注释
+ 移除不需要的测试代码

### 1.3.4 
+ 为 lib/ 增加文档和脚本
+ 更新引擎包到最新

### 1.3.3 
+ 支持 3d 动画效果
+ 支持按图片尺寸比例缩放,并使用模糊效果填充空白部分

### 1.3.2
+ 增加 setBitrateControl 设置比特率参数


### 1.3.1
+ 修复渲染子进程非正常退出导致进程卡死的问题


### 1.3
+ 更改包名为 com.seeshiontech.vesdk


### 1.2
+ 增加 setDynamicSubFiles 方法,为动态模板设置相关子素材

### 1.1
+ 重构进程渲染接口
    |- 增加 VeProcessRenderTask
    |- 支持设置音乐文件
    |- 替换之前的进程渲染接口
    |- 修复潜在崩溃问题
    
### 1.0

+ 线程渲染接口
+ 进程渲染接口