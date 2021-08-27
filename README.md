

## 快速集成

__Gradle 编译环境（Android Studio）__

(1）在 <font color=red size=4 >  **project**  </font>级别的 build.gradle 文件中添加 android-gradle-plugin 依赖：

```android
buildscript {
    repositories {
        jcenter()
        //添加 Sendata Analytics maven 库地址
        maven { url 'https://jitpack.io' }
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.2.0'
        //添加 android-gradle-plugin 依赖
        classpath 'com.github.haibin80s:sa-sdk-android-plugin:1.0.0'
    }
}

allprojects {
    repositories {
        jcenter()
        //添加 Sendata Analytics maven 库地址
        maven { url 'https://jitpack.io' }
    }
}
```

（2）在 <font color=red size=4 > **主 module** </font>的 build.gradle 文件中添加 com.sendata.analytics.android 插件、Sendata Analytics SDK 依赖：

```android
apply plugin: 'com.android.application'
//添加 com.sendata.analytics.android 插件
apply plugin: 'com.sendata.analytics.android'

dependencies {
   //添加 Sendata Analytics SDK 依赖
   compile 'com.sendata.analytics.android:SendataAnalyticsSDK:1.0.0'
}
```


