# 视杏短视频渲染 java sdk

基于引擎提供 jni 接口


# 使用说明

+ lib 中是已经编译好的　jni 动态库


# 运行方法

+ 运行的时候需要指定　-Djava.library.path 到　jni 的目录：

+ "edit Configuraions" 增加　junit 的运行配置，在　VM Options 增加　-Djava.library.path=./lib　即可