# token信息

* ## 接口

/send/api/mobile

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | token |  |
| srid | 服务ID | 默认-1 |
| platform | 平台类型 | 默认Android |
| **content** |  |  |
| account | 唯一标识码 |  |
| agent | agentId |  |

* ## 样例

`[{`

`	"header":{`

`		"tid":"JsVkXHdqTG1878285484",`

`		"appid":"TZbafrPAmp1880722139",`

`		"pt":"dataToken",`

`		"srid":"-1",`

`		"platform":"Android"`

`	},`

`	"content":[`

`		{`

`			"accountId":0,`

`			"agentId":0`

`		}`

`	]`

`}]`

