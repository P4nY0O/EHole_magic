# EHole_magic
在进行web打点时，信息收集中对目标进行指纹识别是必不可少的一个环节，使用EHole识别出来的重点资产还要用其他漏洞利用工具去检测，非常的不方便，在原本的基础上加了个漏洞检测功能。提打点的效率。（不影响原版功能的使用）



# 运行流程
对资产进行指纹识别-->重点资产进行漏洞检测-->如：http://www.xxx.com存在通达OA--> 对通达OA漏洞进行扫描
<img width="676" alt="image" src="https://github.com/lemonlove7/EHole_magic/assets/56328995/97b5c907-ca20-465e-bd04-4043b16d1f7e">


# 使用
默认不开启，在poc.ini中将poc=no改为poc=yes开启


### fofa识别
注意：从FOFA识别需要配置FOFA 密钥以及邮箱，在config.ini内配置好密钥以及邮箱即可使用。

```
ehole finger -s domain="baidu.com"  // 支持所有fofa语法
```
### hunter识别
注意：从hunter识别需要配置hunter 密钥，在config.ini内配置好密钥即可使用。

```
ehole finger -b ip="180.140.20.182"  // 支持所有hunter语法
```

### 本地识别

```
ehole finger -l 1.txt  // 从文件中加载url扫描
```

### 单个目标识别
```
ehole finger -u http://www.baidu.com // 单个url检测
```

# 使用截图
<img width="930" alt="image" src="https://github.com/lemonlove7/EHole_magic/assets/56328995/e4064f38-6458-4778-a2f5-b7db2de54b1d">

# 更新日志

### 2023年7月5日

1、修复mac版报错segmentation fault


2、增加从hunter提取资产，进行指纹识别

<img width="892" alt="image" src="https://github.com/lemonlove7/EHole_magic/assets/56328995/f2c733d8-6bf6-4d56-b31b-61015421fd7c">
<img width="807" alt="image" src="https://github.com/lemonlove7/EHole_magic/assets/56328995/dfb7b200-4938-41b1-88c3-9756c6970ebc">


## 参考优秀项目
POC-bomber：https://github.com/tr0uble-mAker/POC-bomber

peiqi文库：https://peiqi.wgpsec.org

EHole：https://github.com/EdgeSecurityTeam/EHole




