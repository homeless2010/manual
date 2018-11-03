## 安装配置
* [下载maven](http://maven.apache.org/download.cgi)
>maven3.3+需要jdk1.7或更高版本

* 配置环境变量
 1. maven环境变量    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/m2_home.png)
 2. 添加path    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/path.png)    
 3. 在cmd命令窗口中执行mvn -v    
  如图则安装成功    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/mvn.png)    
* 配置镜像与仓库地址    
  1. Repository（仓库）
  ![](https://cdn.www.sojson.com/file/17-12-20-22-34-47/doc/8469051458)    
  2. Mirror    
  mirror相当于一个拦截器，它会拦截maven对remote repository的相关请求，把请求里的remote repository地址，重定向到mirror里配置的地址。    
  --------------------------------------------
  *一般公司都有自己的私服，可以在你的maven安装目录conf下或者本地仓库下的settings.xml配置Repository，重复配置用户配置会覆盖全局配置*    
## maven项目开发调试
1. 新建maven项目    
![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/sample.png)    
2. 配置maven build     
  - 项目右键Run as 找到 Run Configurations...
  - 在左侧找到Maven Build 点击右键新建    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/debug1.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/debug2.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/debug3.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/debug4.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/debug5.png)    
  **此时就可以点击Run As 找到你配置好的命令，执行就可运行项目了**
3. 运行
  - 启动报错找不到jetty插件需要在pom中配置或者在setting.xml中配置    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/jetty6.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/jetty7.png)   
  再次启动    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/success.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/success2.png)
4. 调试
  - 方式一    
  点击Debug As 找到上面步骤2配置的Run Configuration的命令，执行即可
  - 方式二    
  ***利用远程调试来调试本地代码***    
  项目右键Run as 找到 Debug Configurations...    
  **首先需要在上面步骤二中加入调试相关虚拟机参数**   
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/remote4.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/remote1.png)    
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/remote2.png)     
  ![](http://www.cuichaojiang.xin/wp-content/uploads/2018/11/remote3.png)    
  ***调试时先启动run configuration它会额外启动一个调试端口，然后待端口启动后启动上面配置好的debug configuration***    
 -----------------------------------------------------
 *仅供参考 如有疑问欢迎提交issue*  
