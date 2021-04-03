# api.doc

## 1.牛鼻识别

#### 接口URL
> https://api.aibank.jp/aiserver/v1/oxNose

#### 请求方式
> POST

#### Content-Type
> form-data



#### 请求Header参数

| 参数        | 示例值                                      | 是否必填 | 参数描述         |
| :-------- | :--------------------------------------- | :--- | :----------- |
| accessKey | eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiIzODlmMTZhYzdmODM0MjliIiwiZXhwIjoxNjE3NTMzMzk4LCJpYXQiOjE2MTcxMDEzOTgsInJhbiI6Im83ZnQ4cyJ9.AMZsXN_KO9GjowS7lLyZ9tvUF1VdlWzRUBGPVp6kNVA | 必填   | accessKey 唯一 |

#### 请求Body参数

| 参数   | 示例值                                 | 是否必填 | 参数描述 |
| :--- | :---------------------------------- | :--- | :--- |
| pic1 | D:\dutyCode\aibank\test_api\ox1.png | 必填   | 图片1  |
| pic2 | D:\dutyCode\aibank\test_api\ox2.png | 必填   | 图片2  |

#### 成功响应示例
```javascript
{
	"code": 200,
	"msg": "成功",
	"data": {
		"confidence": 0.168
	}
}
```

| 参数              | 示例值   | 参数描述 |
| :-------------- | :---- | :--- |
| code            | 200   | 响应码  |
| msg             | 成功    | 响应信息 |
| data            | -     | 响应数据 |
| data.confidence | 0.168 | 置信度  |



## 2.人脸交换

#### 接口URL
> https://api.aibank.jp/aiserver/v1/swapFace

#### 请求方式
> POST

#### Content-Type
> form-data



#### 请求Header参数

| 参数        | 示例值                                      | 是否必填 | 参数描述         |
| :-------- | :--------------------------------------- | :--- | :----------- |
| accessKey | eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiIzODlmMTZhYzdmODM0MjliIiwiZXhwIjoxNjE3NTMzMzk4LCJpYXQiOjE2MTcxMDEzOTgsInJhbiI6Im83ZnQ4cyJ9.AMZsXN_KO9GjowS7lLyZ9tvUF1VdlWzRUBGPVp6kNVA | 必填   | accessKey,唯一 |

#### 请求Body参数

| 参数      | 示例值                                    | 是否必填 | 参数描述 |
| :------ | :------------------------------------- | :--- | :--- |
| orgPic  | D:\dutyCode\aibank\test_api\source.png | 必填   | 原图   |
| destPic | D:\dutyCode\aibank\test_api\T2.jpg     | 必填   | 目标图  |

#### 成功响应示例
```javascript
{
	"code": 200,
	"msg": "成功",
	"data": {
		"base64": "9jabdel12lklerekrj..."
	}
}
```

| 参数          | 示例值                   | 参数描述     |
| :---------- | :-------------------- | :------- |
| code        | 200                   | 响应码      |
| msg         | 成功                    | 响应信息     |
| data        | -                     | 响应数据     |
| data.base64 | 9jabdel12lklerekrj... | 结果base64 |

