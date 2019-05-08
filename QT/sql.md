环境监测系统数据库设计
===

### 总体设计

1.防疫信息
2.饲喂信息
3.产量信息

4.奶山羊信息

5.羊舍信息

6.设备信息

### 防疫信息

防疫信息表(antiepidemicData)

| 编号 | 奶山羊编号 | 疫苗编号  | 防疫时间 |        备注        |
| :--: | :--------: | :-------: | :------: | :----------------: |
|  id  |   goatId   | vaccineId |  inTime  | antiepidemicRemark |

疫苗信息表(vacineInfo)

| 疫苗编号 |  疫苗名称  |  疫病种类  |  免疫时间  |  免疫剂量  |  注射部位  |     备注     |
| :------: | :--------: | :--------: | :--------: | :--------: | :--------: | :----------: |
| vacineId | vacineName | vacineType | vacineTime | vacineDose | vacinePart | vacineRemark |



### 饲喂信息

饲喂信息表(feedingData)

| 编号 | 奶山羊编号 | 饲料编号 |  饲喂量   | 饲喂时间 |     备注      |
| :--: | :--------: | :------: | :-------: | :------: | :-----------: |
|  id  |   goatId   |  feedId  | feedLevel |  inTime  | feedingRemark |

饲料信息表(feedInfo)

| 饲料编号 |   名称   | 适用范围  | 用法用量  |    备注    |
| :------: | :------: | :-------: | :-------: | :--------: |
|  feedId  | feedName | feedRange | feedUsage | feedRemark |

###  产量信息

产量信息表（yieldData)

| 编号 | 奶山羊编号 | 产品编号  | 产量  | 产出时间 |    备注     |
| :--: | :--------: | :-------: | :---: | :------: | :---------: |
|  id  |   goatId   | productId | yield | outTime  | yieldRemark |

产品信息表(productInfo)

| 产品编号  |  产品名称   |     备注      |
| :-------: | :---------: | :-----------: |
| productId | productName | productRemark |

### dataForm
| 奶山羊编号 | 产品名称 |   舍号   | 时间 |  备注  |
| :--------: | :------: | :------: | :--: | :----: |
| goatId     | productId | houseId | time | remark |



### 4.奶山羊信息

奶山羊信息表(goatInfo)

| 编号 | 奶山羊编号 |  舍号   |  体重  | 入圈时间 | 出圈时间 |
| :--: | :--------: | :-----: | :----: | :------: | :------: |
|  id  |   goatId   | houseId | weight |  inTime  | outTime  |

#### 5.羊舍信息

羊舍信息表(houseInfo)

| 羊舍编号(舍号) |
| -------------- |
| houseId        |

羊舍环境数据表(houseData)

| 编号 |  舍号   | 记录时间  | 温度  | 湿度  | 二氧化碳 | 氨气 |   光照    | PM2.5 | PM10  | 烟雾  |
| :--: | :-----: | :-------: | :---: | :---: | :------: | :--: | :-------: | :---: | :---: | :---: |
|  id  | houseId | datatimem | wendu | shidu |  eryang  | anqi | guangzhao | pmer  | pmshi | yanwu |



#### 6.设备信息

设备信息表(deviceInfo)

| 编号 | 设备编号 |  设备状态   | 购入时间 |
| :--: | :------: | :---------: | :------: |
|  id  | deviceId | deviceState |  inTime  |

绑定信息表(bindingInfo)

| 绑定编号  | 设备编号 | 奶山羊编号/羊舍编号 |
| --------- | -------- | ------------------- |
| bindingId | deviceId | goatId/houseId      |

