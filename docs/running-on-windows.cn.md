Running Appium on Windows
在windows上运行appium
=======================

# Limitations
#限制

If you are running Appium on Windows, you cannot use the prebuilt '.app', which is built for OS X only. Additionally, you will not be able to test iOS apps because Appium relies on OS X-only libraries to support iOS testing.
如果你在windows上安装appium，你没法使用预编译专用于OS X的.app文件，你也将不能测试IOS apps，因为appium依赖OS X专用的库来支持IOS测试。这意味着你只能通过在mac上来运行IOS的app测试。这点限制挺大。


# Setup
#启动

To get started:

1. Install [node.js](http://nodejs.org/download/) (v.0.8 or greater). Use the installer from nodejs.org.
1. 安装nodejs(http://nodejs.org/download/)(0.8版本及以上)，通过官方的安装程序来安装。

2. Install the [Android SDK](http://developer.android.com/sdk/index.html). You will need to run the 'android' tool (included in the SDK) and make sure you have an API Level 17 or greater API installed. Set `ANDROID_HOME` to be your Android SDK path and add the tools and platform-tools folders to your PATH variable.
2. 安装android的sdk包，(http://developer.android.com/sdk/index.html)，运行依赖sdk中的'android'工具。并确保你安装了Level17或以上的版本api。设置'ANDROID_HOME'系统变量为你的Android SDK路径，并把tools platform-tools两个目录加入到系统的Path路径里。因为这里面包含有一些执行命令

3. Install the Java JDK and set `JAVA_HOME` to your JDK folder.
3. 安装java的JDK，并设置'JAVA_HOME'变量为你的JDK目录。

4. Install [Apache Ant](http://ant.apache.org/bindownload.cgi) or use the one that comes with the Android Windows SDK in the eclipse\plugins folder. Be sure to add the folder containing ant to your PATH variable.
4. 安装[Apache Ant](http://ant.apache.org/bindownload.cgi)。
或者直接使用Android Windows SDK自带的ant，地址在eclipse\plugins目录，你需要把这个目录加到你的系统PATH变量中

5. Install [Apache Maven](http://maven.apache.org/download.cgi) and set the M2HOME and M2 environment variables. Add the M2 environment variable to your PATH variable.
5. 安装[Apache Maven](http://maven.apache.org/download.cgi)，并且设置M2HOME和M2环境变量，把M2环境变量添加到你的系统PATH变量中。

6. Install [Git](http://git-scm.com/download/win) Be sure to install Git for windows to run in the regular command prompt.
6. 安装[Git](http://git-scm.com/download/win)，确保你安装了windows下的Git，以便可以运行常用的命令

Now that you've downloaded everything, run:
现在，你已经下载安装了所有的依赖，开始运行
reset.bat

    reset.bat

# Running Appium
# 运行Appium

To run tests on Windows, you will need to have the Android Emulator booted or an Android Device connected that is running an AVD with API Level 17 or greater. Then run Appium on the command line using node.js:

    node .

See the [server documentation](https://github.com/appium/appium/blob/master/docs/server-args.md) for all the command line arguments.
要在windows上运行测试用例，你需要先启动Android模拟器或者连接上一个API Level17以上的android真机。
然后在命令行运行appium 
    node .


# Notes
* you must supply the --no-reset and --full-reset flags currently for android to work on Windows.
* There exists a hardware accelerated emulator for android, it has it's own
  limitations. For more information you can check out this
  [page](https://github.com/appium/appium/blob/master/docs/android-hax-emulator.md).
* Make sure that `hw.battery=yes` in your AVD's `config.ini`.

# 备注
* 你必须带上--no-reset和--full-reset标记，以用于windows上的android
* 有一个硬件加速模拟器用于android，但是它有自己的一些限制，如果你想了解更多，请参考[页面](https://github.com/appium/appium/blob/master/docs/android-hax-emulator.md)
* 确保在你的AVD的'config.ini'中有一个配置项为`hw.battery=yes` 



出于对官方文档的尊重，我按照原文翻译，如下介绍我的安装心得。官方提到的一些工具，其实并不需要安装。

# 安装appium的最简单方式


1. 安装node
2、使用npm安装appium，npm install appium

# 运行appium
启动appium，直接运行appium 即可。appiun会启动2个端口，一个是4723，用于webdriver协议，一个是4724，是用于和android交互使用的

