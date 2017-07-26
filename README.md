# CompressHelper
压缩，图片压缩，压缩Bitmap，Compress,CompressImage,CompressFile,CompressBitmap<br><br>

主要通过尺寸压缩和质量压缩，以达到清晰度最优，该项目参考了[https://github.com/zetbaitsu/Compressor](https://github.com/zetbaitsu/Compressor) 的部分代码，且在基础上修正了部分bug
## 效果图<br>
![](https://github.com/Canglangweiwei/CompressHelper/blob/CompressHelper-master/111.png)

#### ⊙开源不易，希望给个star或者fork奖励
#### ⊙拥抱开源：https://github.com/Canglangweiwei/


## 特点
  1、支持压缩单张图片和多张图片<br>
## 使用方法
#### 1、添加依赖<br>
##### Step 1. Add it in your root build.gradle at the end of repositories:
```java
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
##### Step 2. Add the dependency
```java
dependencies {
	        compile 'com.github.nanchen2251:CompressHelper:1.0.5'
	}
```
#### 2、在Activity里面使用<br>
```java
   File newFile = CompressHelper.getDefault(this).compressToFile(oldFile);
```
#### 3、你也可以自定义属性
```java
   File newFile = new CompressHelper.Builder(this)
                    .setMaxWidth(720)  // 默认最大宽度为720
                    .setMaxHeight(960) // 默认最大高度为960
                    .setQuality(80)    // 默认压缩质量为80
		    .setFileName(yourFileName) // 设置你需要修改的文件名
                    .setCompressFormat(CompressFormat.JPEG) // 设置默认压缩为jpg格式
                    .setDestinationDirectoryPath(Environment.getExternalStoragePublicDirectory(
                            Environment.DIRECTORY_PICTURES).getAbsolutePath())
                    .build()
                    .compressToFile(oldFile);
```
该项目参考了：

* [https://github.com/zetbaitsu/Compressor](https://github.com/zetbaitsu/Compressor) 
* [https://github.com/Curzibn/Luban](https://github.com/Curzibn/Luban)

#### 有码走遍天下 无码寸步难行（引自网络）

> 梦想，永不止步!  
爱编程 不爱Bug  
爱加班 不爱黑眼圈  
固执 但不偏执  
疯狂 但不疯癫  
生活里的菜鸟  
工作中的大神  
身怀宝藏，一心憧憬星辰大海  
追求极致，目标始于高山之巅  
一群怀揣好奇，梦想改变世界的孩子  
一群追日逐浪，正在改变世界的极客  
你们用最美的语言，诠释着科技的力量  
你们用极速的创新，引领着时代的变迁  
  
------至所有正在努力奋斗的程序猿们！加油！！  
