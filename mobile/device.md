# device信息

* ## 接口

/send/api/mobile

* ## 属性说明

| **名称** | **含义** | **注释** |
| :--- | :--- | :--- |
| **header** |  |  |
| tid | 租户码 |  |
| appid | 应用ID |  |
| pt | device |  |
| srid | 服务ID | 默认-1 |
| platform | 平台类型 | 默认Android |
| **content** |  |  |
| osname | 操作系统名称 |  |
| osversion | 操作系统版本 |  |
| model | 编译打包模型 |  |
| agentname | 友云音agent名称 |  |
| agentver | 友云音agent版本 |  |
| deviceid | 设备id |  |
| country | 国家编码 |  |
| region | 地区编码 |  |
| manufacturer |  |  |
| hostip | ip地址 |  |
| province | 省份 |  |
| city | 城市 |  |
| misc | 镜像说明 |  |
| platver | 镜像版本 |  |
| platform | 平台类型 |  |

* ## 样例

\[{

	"header":{

		"tid":"JsVkXHdqTG1878285484",

		"appid":"TZbafrPAmp1880722139",

		"pt":"device",

		"srid":"-1",

		"platform":"Android"

	},

	"content":\[

		{

			"agentname": "AndroidAgent",

			"agentver": "1.0.0",

			"country": "",

			"deviceid": "cde336a7-6921-4d07-9a92-d37f8d915dd7",

			"manufacturer": "HUAWEI",

			"misc": {

				"platform": "Native",

				"platver": "1.0.0",

				"size": "normal"

			},

			"model": "KNT-AL20",

			"osname": "Android",

			"osversion": "7.0",

			"region": "",

			"hostip":"10.6.225.112",

			"province":"北京",

			"city":"北京"

		}

	\]

}\]

