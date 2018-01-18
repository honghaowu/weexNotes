# weex开发
## 1.weex开发环境配置
## 1.1 weex开发环境安装
* [node安装 （LTS推荐）](https://nodejs.org/en/download/)
* [安装java环境](http://www.java.com/zh_CN/)
* [Git](https://git-scm.com)
* weex-toolkit安装 (npm install weex-toolkit -g)  
  weex -v 检查安装版本
* webpack 安装 (npm install webpack -g)
* [android-studio安装，预览开发视图](http://www.android-studio.org/)  
  *Configure->SDKManager->SDK Tools->勾选show Package Details ->勾选23.0.2*

## 1.2 新建weex目录
 * weex create weexDemo
   *会自动安装weekpage*
 * cd weexDemo  
 * npm install  
 * 添加android平台支持 (weex platform add android)
## 1.3 运行android studio
   * 1.选择Open an existing Android Studio project ->weexDemo -> platforms -> android
   * 2.虚拟机配置：菜单栏里的Tools->Android->AVD Manager->Create Virtual Device
    *vt-x报错，HP笔记本是F10进入bios,然后，设置Intel Virtual Technology > Enabled*
    *如果是openfile失败，设置如下*
```
   android.applicationVariants.all { variant ->
        variant.outputs.all {//这里是all，下面是根据自己的情况来定制
            def date = new Date()
            def formattedDate = date.format('yyyyMMdd')
            def fileName
            if (variant.buildType.name == "release") {
                // 输出apk名称为app_100_release.apk
                fileName = "xxx_V${defaultConfig.versionName}.apk"
            } else if (variant.buildType.name == "debug") {
                // 输出apk名称为app_100_debug.apk
                fileName = "xxx_debug_V${defaultConfig.versionName}_${formattedDate}.apk"
            } else {
                // 输出apk名称为app_v1.0.0_2017-12-11_101_beta.apk
                fileName = "xxx_Beta_V${defaultConfig.versionName}.apk"
            }
            //outputFileName = "HuaxiaSign_${defaultConfig.versionName}_${formattedDate}.apk"
            //很多博客只是写了上面这句话，没有具体赋值，自己来选择赋值给outputFileName
            outputFileName = fileName
        }
    }
```
    * 3 把dist下的index.js复制到android studio中的app->assets->index.js ,然后run，即可预览
    
## 1.4 注意事项
    - 之前在安装过程中，出现报错：  
    index.web.js from UglifyJs<br>Unexpected token: punc ()) [index.web.js:752,18]，
    按照官网重新走了一遍，这次用npm,之前用的是cnpm，没有报错。
    http://weex.apache.org/cn/guide/set-up-env.html
## 1.5 weex init 搭建开发环境
    - weex init myweex
    - cd myweex
    - npm install 
    - npm run dev
    - npm run serve
## 1.6 weex组建
    - css布局：
        1.flex,不支持float和百分比  
        2.不支持background的复合写法，包括border,margin,padding的复合写法，需要分开写border-left-style,border-left-color,border-left-width
        3.单位px,不支持rem,em,pt，但是这里的px会根据屏幕适应，类似小程序中的rpx

