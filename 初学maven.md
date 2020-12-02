# Record

# 2020-12-2 这是学习Maven的第一天  

今天学习的java基本的包管理 以及maven是如何对项目进行接管的

同时了解了maven的以下机制

maven不允许出现同名不同版本的jar包出现

当遇到包冲突时，maven采取就近原则 使用距离项目最近的classpath

包冲突时 可比较依赖版本  选择不冲突的依赖重新在pom文件中配置 
或者在pom文件中配置exclusions 标签  标签作用是告诉maven在依赖嵌套中排除这个依赖
在依赖标签中加入scope标签指定test  test代码中可见 
指定compile 则在生产代码和测试代码中都有效 
指定provided 只在编译期间有效
