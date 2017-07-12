# app信息

* ## 接口

/send/api/mobile

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | app |  |
| srid | 服务ID | 默认-1 |
| platform | 平台类型 | 默认Android |
| **content** |  |  |
| name | 应用名称 |  |
| packageid | 包路径 |  |
| version | 应用版本 |  |

* ## 样例

```json
[{
	"header":{
		"tid":"JsVkXHdqTG1878285484",
		"appid":"TZbafrPAmp1880722139",
		"pt":"app",
		"srid":"-1",
		"platform":"Android"
	},
	"content":[
		{
			"name": "办公OA",
			"packageid": "com.rock.xinhuapk",
			"version": "1.1.5"
		}
	]
}]
```



