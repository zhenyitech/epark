# 易泊车灰度对接

### 请求地址

`http://ctm.zhen-yee.com/flw/test/epark/push`


### 请求参数

|参数|名称|备注|
|-----|-----|-----
|plate|车牌号码|`MN3770`|
|fee|金额(单位分)|如6元,传入`600`|
|uid|用户id|目前可空| 


# 请求示例


> 车牌号`MN3770`
>
> 金额6元

`http://ctm.zhen-yee.com/flw/test/epark/push?plate=MN3770&fee=600`
