# 灰度对接二


```
curl --location --request POST 'https://epark.zhenyi.tech/flw/api/v1/unionpay/callback/pay' \
--header 'User-Agent: Apifox/1.0.0 (https://apifox.com)' \
--header 'Content-Type: application/json' \
--header 'Accept: */*' \
--header 'Host: epark.zhenyi.tech' \
--header 'Connection: keep-alive' \
--data-raw '{
    "car":"MN3770",
    "new":0,
    "fee":3
}'
```

## 接口地址 `POST`

`https://epark.zhenyi.tech/flw/api/v1/unionpay/callback/pay`

## body
```
{
    "car":"MN3770",
    "new":0,
    "fee":3
}
```

> `fee`:金额是整数,3为3元
> `new`默认保持`0`
> `car`:车牌号码


# ~~易泊车灰度对接~~

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


