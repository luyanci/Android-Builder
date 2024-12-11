<div align="center"> 
  
# Android-Builder
 Automaticcaly build android kernel by github actions.


[原版仓库](https://github.com/DogdayAndroid/Android-Builder/)  [原版readme](https://github.com/luyanci/Android-Builder/blob/main/README_vanlia.md) 
  
 [![Build kernels](https://github.com/luyanci/Android-Builder/actions/workflows/build.yml/badge.svg)](https://github.com/luyanci/Android-Builder/actions/workflows/build.yml)  
  
</div> 
  
 ## 介绍 
 使用github Action构建安卓系统内核 支持kernelSU和LXC docker构建

## KernelSU
从v20241211.88起，将使用[rissu版kernelsu](https://github.com/rsuntk/KernelSU)的构建补丁，以继续支持non-gki内核构建，请注意之后的构建需要从提供的链接下载管理器

 ## 刷入方法 
 1.进入recovery（关机状态下电源+音量加） 
  
 2.备份boot分区 (Redmi K30 /Redmi 8需额外备份dtbo分区)
  
 3.下载[内核](https://github.com/luyanci/Android-Builder/releases/latest) 
  
 4.刷入（或者在sideload模式下用'adb sideload xxx.zip'刷入） 
  
 ## 目前已有内核构建 
 ### Redmi K30 / PocoF2 (phoenix/phoenixin)
 **PixelExperience(Android 11/Android 12)** 
  
 **redcliff**(Android13类原 可自行测试) 
  
 **Pure**([这个非官方的PE13](https://github.com/SimpleJony/device_xiaomi_phoenix/releases/tag/PEPlus)似乎用了这个内核)[From](https://github.com/PixelExperience/official_devices/issues/3155) 

 ### Redmi K40 (alioth)
**Realking**

 ### Redmi K60 / Poco F5 Pro (mondrian)
 **baalam**

 **EvolutionX** [Not Work]

 ### Redmi 8(olive)
 **LOLZ**

 共6个内核构建(主要是针对类原的构建) 
  
 ## 构建周期 
 每周日的早11点(UTC)会自动编译一次内核，每个月会清理一次构建历史 
  
 如果有非周日的releases，那可能是我给仓库更新了点什么并构建测试了
 ~~(也有可能是ksu有新的稳定releases发布了)~~

 (别想了，ksu已经放弃支持非gki内核了，只能锁死在v0.9.5了)
  
 ## 使用的内核源码仓库链接
 ## Redmi K30 / PocoF2 (phoenix/phoenixin)
 [MIUI&Redcliff(来自于ksu的wiki)](https://github.com/SlackerState/android_kernel_xiaomi_sm6150) 
  
 [PixelExperience](https://github.com/PixelExperience-Devices/kernel_xiaomi_phoenix) 
  
 [Pure](https://github.com/Pzqqt/android_kernel_xiaomi_sm6150-1)

 ## Redmi K40 (alioth)
[Realking](https://github.com/Rohail33/Realking_kernel_sm8250)

 ## Redmi K60 / Poco F5 Pro (mondrian)
 [Baalam](https://github.com/LowTension/android_kernel_xiaomi_sm8475)
 [EvolutionX](https://github.com/Evolution-X-Devices/kernel_xiaomi_sm8475)

 ## Redmi 8(olive)
[LOLZ](https://github.com/Jprimero15/lolz_kernel_redmi8)