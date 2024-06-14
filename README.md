# 收费系统配置清单

## 配置管理后台

1. 系統管理->停車場管理->亞馬喇前地停車場->閘機

1. 添加车位余量信息:**设置出入方向**

1. 设置电单车车道:**设置出入方向**

1. 设置私家车车道

1. 添加岗亭管理员

## 闸机信息

| 名称        | 操作     | 备注                                |
|-----------|--------|-----------------------------------|
| 閘機名       | **必填** |                                   |
| 地址        | **必填** | 闸机位置,任意填写                         |
| 攝像頭IO     | **必填** |                                   | 
| IO板IO     | **必填** |                                   | 
| apikey    | **必填** | 一般數字開頭，用於閘機設置頁的登錄名,亞麻喇正式入口為6，出口為7 | 
| apisecret | **必填** | 默認輸入：`123456`，用於閘機設置頁的登錄密碼        | 
| 閘機方向      | **必填** |                                   | 

> **如打开闸机程序弹出：缺少`msvcp140.dll`，请安装`VC_redist.x64.exe`**
## 出口工控机

| COM口 | 功能            | 备注 |
|------|---------------|----|
| COM1 | 澳门通           |    |
| COM2 | 时租票打印机(POS80) |    |
| COM3 |               |    |
| COM4 |               |    |
| COM5 | BOC/银联闪付      |    |

## 岗亭

| COM口 | 功能               | 备注 |
|------|------------------|----|
| COM1 | 澳门通              |    |
| COM2 | 补票打印机(硬票)(POS80) |    |
| COM3 | 金额显示(USB转换)      |    |
| USB  | 打印机(软票)          |    |

配置打印机:`/data/flutter_asset/setting/config.json`

## 配置摄像头

| 名称     | 操作                | 备注               |
|--------|-------------------|------------------|
| 攝像頭地址  |                   | 例:`192.168.1.24` |
| 设置网络参数 | 網絡參數->FTP->點擊啓用FTP | **必须勾选**         |
| FTP地址  | 例`192.168.1.207`  | **根据不同停车场调整**    |
| 用戶名    | zhenyi            |                  |
| 密碼     |zhenyi|                  |
| 心跳周期   |                   |                  |
| 保存路徑   | `/<ip>`| 直接复制,**带符号**     |
| 勾选上传   | 勾選文件名包含車牌號，上傳XML文件| **必须勾选**         |
| 验证配置   |點擊驗證，彈出綠色彈框                   |                  |
| 保存配置   |點擊確定保存數據||

## 工控机配置

| 名称                    | 操作                     | 备注         |
|-----------------------|------------------------|------------|
| 閘機設置                  | `ctrl+shift+alt+s`     |            |
| 登錄名稱                  | 	後臺相應閘口的`apikey`	      | 默认`zhenyi` |
| 登錄密碼                  | 	後臺相應閘口的`apisecret`	   |默认`zhenyi` |
| 服務器地址（HTTP）           | `http://192.168.1.207` | 据不同停车场调整   |
| 服務器地址（WebSocket）      | `http://192.168.1.207` | 根据不同停车场调整  |
| O板地址                  | 後臺相應的主板地址	             |`192.168.0.162`|
| IO板端口                 | `1025`	                |
| 打印機名稱                 | 系統打印機的名稱	              |`POS80`|
| 澳门通COM口               | `COM1`	                  |
| 澳门通扣值命令               | `F4`                     |
| BOC通信端口                | `COM5`	                  |
| 日志是否打印                | `是`                      |
| 调试模式                  | `关闭`	                    |
| 混合车道                  |                        | |
| 日志文件夹| 出口在根目录创建log文件夹		       |
| 安装DLL                 |                        |
| 64位WIN7               |                        |

## 支付信息

| a | 2 | 3 | 4 |
|---|---|---|---|
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |

## 接线方式

### 出口

| a | 2 | 3 | 4 |
|---|---|---|---|
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |
| a | 2 | 3 | 4 |

### 入口

#### 入口私家车工控机

| 接口   | 描述 | 备注 |
|------|----|----|
| COM1 |    |    |

#### 入口电单车工控机

| 接口   | 描述 | 备注 |
|------|----|----|
| COM1 |    |    |

#### 入口IO板

| 接口  | 描述 | 备注 |
|-----|----|----|
| DO0 |||
| DO1 |||
| DO2 |||
| DO3 |开闸||
| DO4 |||
| DO5 |开闸||
| DI0 |充电车按钮|    |
| DI1 |伤残车按钮|    |
| DI2 |时租票按钮|    |
| DI3 |电单车地感|    |
| DI4 |私家车地感|    |
| DI5 |    |    |
| DI6 |    |    |
| DI7 |    |    | 
| DI8 |票据打印按钮|    | 
| DI9 |    |    | 
| DI10 |    |    |
| DI11 |    |    |  

#### 出口IO板

| 接口  | 描述 | 备注 |
|-----|----|----|
| DO0 |    |    |
| DO1 |    |    |
| DO2 |    |    |
| DO3 |    |    |
| DO4 |    |    |
| DO5 |    |    |
| DI0 |    |    |
| DI1 |    |    |
| DI2 |    |    |
| DI3 |    |    |
| DI4 |    |    |
| DI5 |    |    |
| DI6 |    |    |
| DI7 |    |    |   
| DI8 ||    | 
| DI9 |    |    | 
| DI10 |    |    |
| DI11 |    |    |  

#### 出口私家车工控机

| 接口   | 描述 | 备注 |
|------|----|----|
| COM1 |    |    |

#### 出口电单车工控机

| 接口   | 描述 | 备注 |
|------|----|----|
| COM1 |    |    |
