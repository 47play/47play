#### Android Studio接入

##### （1）将sdk47-release.aar至拷贝至libs文件夹

##### （2）修改build.gradle文件

![](/Users/wukangjian/bitbucket/public/others/1.jpg)



```java
repositories {
    flatDir {
        dirs 'libs'
    }
}
   
implementation (name:"sdk47-release",ext:'aar')
```