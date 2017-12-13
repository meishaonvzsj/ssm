使用Maven的好处：
    一：可以将每个工程中的jar提取出来放到本地仓库中，这样工程中只包含源代码,工程中只是引用本地仓库中的jar包，
        好处：可以实现jar包的集中管理与维护
    二：可以实现对jar包的精确管理，即需要使用什么jar包就在pom文件中进行配置
    三：可以实现对jar包所依赖的jar包的自动管理
    四：方便工程的打包处理


Maven的使用步骤：
    一：创建本地仓库(拷贝已经仓库)
    二：从maven插件包中解压出settings.xml，和本地仓库放在一块，
       修改settings.xml文件中的<localRepository>D:/Maven/Reponsitory</localRepository>(用来指定本地仓库的路径)
    三：修改开发工具中的maven配置参数(为maven插件指定settings.xml文件的路径)
    四：在开发工具中创建maven工程


pom:project object model

modelVersion:所使用的object model版本
groupId:项目创建团体或组织的唯一标识符，通常是域名倒写
artifactId:项目artifact唯一的基地址名(可以理解成项目名/工程名)
package:打包方式
version:artifact的版本
name:表示项目的展示名(通常和artifactId相同)，在maven生成的文档中使用
url:项目的发布地址，在maven生成的文档中使用
description:项目的描述，在maven生成的文档中使用
dependencies:表示依赖，在子节点dependency中添加具体依赖的groupId artifactId 和version
build:表示build配置
finalName:打包时的最终名称