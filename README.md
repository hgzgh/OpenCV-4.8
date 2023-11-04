# OpenCV-4.8+opencv-contrib-4.8+CUDA-11.4
此仓库主要演示OpenCV-4.8及扩展库的编译，以及开启GPU,CUDA可以安装自己电脑
需要的版本


我的编译环境：
windows10、VS2019、Cmake-3.28、CUDA(此安装流程需要网上自己找)

注意：我使用的VS2022编译出了很多错误，也不知道为什么，建议还是使用VS2019

1.首先下载Opencv-4.8，点击此[链接](https://github.com/opencv/opencv/releases)进入，找到下图的版本，然后下载Source.code
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699082347997-4899536f-fe8b-4d70-b9fb-68ee2071fd74.png#averageHue=%23fefdfc&clientId=u63a1a90a-4366-4&from=paste&height=685&id=u44bd7b27&originHeight=856&originWidth=1350&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=95134&status=done&style=none&taskId=ue07f51d8-c0a5-4963-be7f-8a5cfe94f17&title=&width=1080)

2.下载对应的OpenCV-Contrib，点击此[链接](https://github.com/opencv/opencv_contrib/tags)，版本一定要和OpenCV一样，下载Source.code
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699082541420-ceb9c8c1-b624-4ede-94f2-cca946d0add4.png#averageHue=%23fefdfd&clientId=u63a1a90a-4366-4&from=paste&height=353&id=u550b6f5c&originHeight=441&originWidth=1310&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=31974&status=done&style=none&taskId=ud9da6e01-6fa9-4eec-bfb8-1fb5124c275&title=&width=1048)

3.下载Cmake3.28(可以不用此版本，3.0以上版本都可以)，点击此[下载](https://cmake.org/download/)，安装步骤网上查询
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699082686883-e8612881-a20f-444d-b2da-e2277ffcd124.png#averageHue=%23f5f4f3&clientId=u63a1a90a-4366-4&from=paste&height=422&id=u10eabc3e&originHeight=527&originWidth=1272&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=88153&status=done&style=none&taskId=u2bd4059d-952d-4288-b775-e57bc31913c&title=&width=1017.6)

4.提前下载.cache，防止cmake过程中自动下载失败，[链接](https://github.com/hgzgh/OpenCV-4.8)

5.解压前面下面的所有zip，然后将解压后的.cache复制到OpenCV-4.8文件夹，然后创建一个一个build文件夹
我的目录结构是这样的
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699083599635-285e3e63-4d83-4537-96c1-e05d9ba68b9a.png#averageHue=%23fcf9f9&clientId=u63a1a90a-4366-4&from=paste&height=259&id=u04774902&originHeight=324&originWidth=920&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=24495&status=done&style=none&taskId=u85d190b3-9c52-470d-9988-eb82cade68e&title=&width=736)

![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699083747671-06572c41-ef01-498b-a179-19441a96bde8.png#averageHue=%23faf8f7&clientId=u63a1a90a-4366-4&from=paste&height=293&id=u6f7c4cb4&originHeight=366&originWidth=874&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=45161&status=done&style=none&taskId=u16904739-d603-4390-af44-e0e4886677a&title=&width=699.2)

6.打开cmake-gui界面，操作如下
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085621807-12f1a1d0-a2b5-4d50-8718-8580dd25569b.png#averageHue=%23f7f7f7&clientId=u63a1a90a-4366-4&from=paste&height=731&id=ud60be65f&originHeight=914&originWidth=1460&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=31790&status=done&style=none&taskId=uee823216-ca5a-4b8a-9e5b-33c4f78cfa2&title=&width=1168)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085654150-2c7d36ee-b09c-491a-a0fc-3fb7f5fe4d1a.png#averageHue=%23f6f6f6&clientId=u63a1a90a-4366-4&from=paste&height=731&id=u1c5681bb&originHeight=914&originWidth=1460&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=38717&status=done&style=none&taskId=ub9bf93b9-b13a-43d1-9604-7abf2fe80c4&title=&width=1168)
当出现下面的界面才可以继续操作，否则请重新按照上面的步骤重来
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699084612081-24f6f4ba-05b8-444d-becc-b049d9b7ef74.png#averageHue=%23f5bcbc&clientId=u63a1a90a-4366-4&from=paste&height=731&id=u7718138a&originHeight=914&originWidth=1460&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=56671&status=done&style=none&taskId=u0393f8ef-ada3-4abf-b12b-a73220c63e7&title=&width=1168)
搜索cuda，全部打勾
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699084687568-b924e279-5bf0-4ca7-ae95-8c6daa0405b1.png#averageHue=%23f9b3b3&clientId=u63a1a90a-4366-4&from=paste&height=185&id=ubcd73bcd&originHeight=231&originWidth=1466&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=15572&status=done&style=none&taskId=u47eab2fd-71fa-4b58-8747-e042b431fab&title=&width=1172.8)
搜索extra，然后选择opencv-contrib中的modules文件夹，一定要选modules文件夹
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699084757359-ea37222f-f8ca-4093-805a-c33f617c1ac4.png#averageHue=%23f7d3d2&clientId=u63a1a90a-4366-4&from=paste&height=130&id=ud35154d8&originHeight=162&originWidth=1437&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=10333&status=done&style=none&taskId=ub316e3b0-8607-41f0-b105-f827f376d00&title=&width=1149.6)
搜索non，打勾
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699084815669-ae470a18-390d-4351-bb62-a50e79fb7542.png#averageHue=%23f7e1e0&clientId=u63a1a90a-4366-4&from=paste&height=126&id=u745ff205&originHeight=157&originWidth=1459&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=9503&status=done&style=none&taskId=u7ec64775-6f1b-4954-a464-d6408672ff8&title=&width=1167.2)
搜索world，打勾
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699084835588-888c392e-414e-4e1f-886b-ea0d882fed23.png#averageHue=%23f7e2e1&clientId=u63a1a90a-4366-4&from=paste&height=129&id=u17c9bb00&originHeight=161&originWidth=1445&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=7292&status=done&style=none&taskId=uf32ecdfd-a9bf-40f2-9de1-ba1b97a9192&title=&width=1156)

然后继续点击configure
直到出现一下页面
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085012545-e0f64b61-03a1-4b88-8ac0-ed17e922af54.png#averageHue=%23f4d6d6&clientId=u63a1a90a-4366-4&from=paste&height=731&id=ufc218c33&originHeight=914&originWidth=1460&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=51904&status=done&style=none&taskId=u09c3ea8a-dbdf-4e44-a673-b3ea9496549&title=&width=1168)

搜索FAST，打勾
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085051488-2a273d53-b079-4c81-820d-2b01c74f10e6.png#averageHue=%23f5d6d5&clientId=u63a1a90a-4366-4&from=paste&height=94&id=u6a5c770f&originHeight=117&originWidth=1469&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=10565&status=done&style=none&taskId=uf5bf1d9d-caa8-4334-95c2-6b34de14c3c&title=&width=1175.2)

然后点击configure，继续等待出现下面页面
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085106363-c155ad87-c2ab-41b1-97cd-8eb737fc7229.png#averageHue=%23f3f1f0&clientId=u63a1a90a-4366-4&from=paste&height=731&id=uf4ea6a09&originHeight=914&originWidth=1460&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=52240&status=done&style=none&taskId=u6dcf287f-5d66-433f-81cd-e5d5d6e7fe9&title=&width=1168)

然后点击Gengeate，完成之后点击Open Project
进入之后按照如下图操作，点击
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085280802-ffe37fd5-24f6-427c-861a-9db25e19fc13.png#averageHue=%23222326&clientId=u63a1a90a-4366-4&from=paste&height=233&id=ubadb35a4&originHeight=291&originWidth=436&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=20808&status=done&style=none&taskId=u982b56e6-b8fa-4ff1-a4d2-3fba8ed6c68&title=&width=348.8)

勾选ALL_BUILD（Release和Debug自行选择，也可以全部选择），下拉菜单继续勾选INSTALL，最后点击生成，等待时间有点久，我个人电脑等待了6个多小时，配置较差
![image.png](https://cdn.nlark.com/yuque/0/2023/png/26064701/1699085343355-b31aaf78-9e4b-4b41-ab76-16a2e565c6a5.png#averageHue=%23f0efee&clientId=u63a1a90a-4366-4&from=paste&height=427&id=uf6aab598&originHeight=534&originWidth=895&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=66203&status=done&style=none&taskId=u90d22bd6-c762-4ac9-8728-6c895a0d585&title=&width=716)
