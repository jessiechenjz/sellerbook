### 获取申报分类（xlobo.catalogue.get）

---
### 系统参数

* 接口调用参数


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |


*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| categorys | JSON Object |  |  |  |
| version | String | N | 版本号（yyyy-MM-dd HH：mm：ss） |


*  类型描述（CategoryInfo） 

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| category_id | String | N | 分类Id |
| category_cn_name | String | N | 分类中文名 |
| category_en_name | String | N | 分类英文名 |
| category_level | Int | N | 分类级别 |
| category_parent_id | Int | N | 分类父ID |

### 返回结果的格式

#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=1iFUMvKfOOxPpDsYsZ&method=xlobo.catalogue.get
* 请求报文:    
<br  />


```
{
	"app_id" : "1iFUMvKfOOxPpDsYsZ",
	"method" : "xlobo.catalogue.get",
	"sign_method" : "MD5",
	"auth_code" : "idQZDeKTAlqlXnbMlzF1hszexlhQqRVJ",
	"timestamp" : "2017-06-22 17:15:20",
	"sign" : "A1CB7B1190B4DD3E9E3D9C1BA4A5E821",
	"nonce_str" : "2901431669163333446162957056584"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"categorys" : [{
				"category_level" : 1,
				"category_id" : "1",
				"category_en_name" : "Cosmetics/Skin Care",
				"category_cn_name" : "彩妆护理",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "2",
				"category_en_name" : "Vehicle Equipments/Travel/Outdoor",
				"category_cn_name" : "车载/旅游/户外",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "3",
				"category_en_name" : "Pet/Home Supplies",
				"category_cn_name" : "宠物用品/居家用品",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "4",
				"category_en_name" : "Kitchen supplies",
				"category_cn_name" : "厨房用品",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "5",
				"category_en_name" : "Clothing/Home Textiles",
				"category_cn_name" : "服饰家纺",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "6",
				"category_en_name" : "Household/Small Electrical Appliances",
				"category_cn_name" : "家用护理品/小电器",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "7",
				"category_en_name" : "Maternal and Baby products",
				"category_cn_name" : "母婴用品",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "8",
				"category_en_name" : "Cleaning & Skin Care Products",
				"category_cn_name" : "清洁护理",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "9",
				"category_en_name" : "Watch/Glasses/Accessories",
				"category_cn_name" : "手表/眼镜/配饰",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "10",
				"category_en_name" : "Digital Audio Products",
				"category_cn_name" : "数码影音",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "11",
				"category_en_name" : "Luggage,Bag/Shoes",
				"category_cn_name" : "箱包/鞋靴",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "12",
				"category_en_name" : "Tabacco/Alcohol/Tea/Beverage",
				"category_cn_name" : "烟酒茶饮",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "13",
				"category_en_name" : "Nutrition, Health Care & Groceries",
				"category_cn_name" : "营养保健/食品",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "14",
				"category_en_name" : "Sports/Education",
				"category_cn_name" : "运动/教育",
				"category_parent_id" : 0
			}, {
				"category_level" : 2,
				"category_id" : "15",
				"category_en_name" : "Key Cellphone",
				"category_cn_name" : "按键手机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "16",
				"category_en_name" : "Touch Screen Cellphone",
				"category_cn_name" : "触屏手机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "17",
				"category_en_name" : "Phone Accessories",
				"category_cn_name" : "手机配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "18",
				"category_en_name" : "Mac",
				"category_cn_name" : "Mac",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "19",
				"category_en_name" : "iPhone",
				"category_cn_name" : "iPhone",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "20",
				"category_en_name" : "iPad",
				"category_cn_name" : "iPad",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "21",
				"category_en_name" : "iPod",
				"category_cn_name" : "iPod",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "22",
				"category_en_name" : "Iphone Accessories",
				"category_cn_name" : "iPhone配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "23",
				"category_en_name" : "Ipad Accessories",
				"category_cn_name" : "iPad配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "24",
				"category_en_name" : "Digital Camera",
				"category_cn_name" : "数码相机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "25",
				"category_en_name" : "Single Camera/Single Lens Reflex Camera",
				"category_cn_name" : "单电/微单相机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "26",
				"category_en_name" : "SLR Camera",
				"category_cn_name" : "单反相机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "27",
				"category_en_name" : "Camcorder",
				"category_cn_name" : "便携摄像机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "28",
				"category_en_name" : "SLR Lens",
				"category_cn_name" : "单反镜头",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "29",
				"category_en_name" : "Other Camera Lens",
				"category_cn_name" : "其他相机镜头",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "30",
				"category_en_name" : "Filter",
				"category_cn_name" : "滤镜",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "31",
				"category_en_name" : "Flash",
				"category_cn_name" : "闪光灯",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "32",
				"category_en_name" : "Camera Bracket",
				"category_cn_name" : "支架",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "33",
				"category_en_name" : "SLR Accessories",
				"category_cn_name" : "单反配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "34",
				"category_en_name" : "Digital Accessories",
				"category_cn_name" : "数码配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "35",
				"category_en_name" : "MP3 Player",
				"category_cn_name" : "MP3",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "36",
				"category_en_name" : "MP4 Player",
				"category_cn_name" : "MP4",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "37",
				"category_en_name" : "Earphones/Headset/Bluetooth Earphone",
				"category_cn_name" : "耳机/耳麦/蓝牙耳机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "38",
				"category_en_name" : "Computer/Mobile Speakers",
				"category_cn_name" : "电脑/手机外设音箱",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "39",
				"category_en_name" : "VCD/DVD Player",
				"category_cn_name" : "VCD/DVD播放机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "40",
				"category_en_name" : "Amplifier",
				"category_cn_name" : "功放",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "41",
				"category_en_name" : "E-book",
				"category_cn_name" : "电子书",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "42",
				"category_en_name" : "Digital Voice Recorder",
				"category_cn_name" : "录音笔",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "43",
				"category_en_name" : "Microphone",
				"category_cn_name" : "麦克风",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "44",
				"category_en_name" : "Digital Photo Frame",
				"category_cn_name" : "数码相框",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "45",
				"category_en_name" : "Compact Disk",
				"category_cn_name" : "唱片光盘",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "46",
				"category_en_name" : "Laptop",
				"category_cn_name" : "笔记本",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "47",
				"category_en_name" : "Tablet",
				"category_cn_name" : "平板电脑",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "48",
				"category_en_name" : "Tablet Accessories",
				"category_cn_name" : "平板电脑配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "49",
				"category_en_name" : "Desktop Computer ",
				"category_cn_name" : "台式机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "50",
				"category_en_name" : "Computer Components ",
				"category_cn_name" : "电脑配件",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "51",
				"category_en_name" : "Computer Peripherals",
				"category_cn_name" : "电脑外设",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "52",
				"category_en_name" : "Router",
				"category_cn_name" : "路由器",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "53",
				"category_en_name" : "Portable Hard Drive",
				"category_cn_name" : "移动硬盘",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "54",
				"category_en_name" : "U Disk",
				"category_cn_name" : "U盘",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "55",
				"category_en_name" : "Game/Software Discs",
				"category_cn_name" : "游戏/软件光盘",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "56",
				"category_en_name" : "Game Console",
				"category_cn_name" : "游戏机",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "57",
				"category_en_name" : "Gamepad",
				"category_cn_name" : "游戏机手柄",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "58",
				"category_en_name" : "Sound Box",
				"category_cn_name" : "音箱",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "59",
				"category_en_name" : "Other Digital Products",
				"category_cn_name" : "其他数码产品",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "60",
				"category_en_name" : "Air Freshener",
				"category_cn_name" : "家用空气清新器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "61",
				"category_en_name" : "Household Sweeper",
				"category_cn_name" : "家用扫地机",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "62",
				"category_en_name" : "Electric Shaver/Shaving Device/Depilator ",
				"category_cn_name" : "电动剃须刀",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "63",
				"category_en_name" : "Hair Dryer",
				"category_cn_name" : "电吹风",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "64",
				"category_en_name" : "Electric Toothbrush",
				"category_cn_name" : "电动牙刷",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "65",
				"category_en_name" : "Beauty Appliance",
				"category_cn_name" : "美容器具",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "66",
				"category_en_name" : "Barber",
				"category_cn_name" : "理发器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "67",
				"category_en_name" : "Hair Waver",
				"category_cn_name" : "美发器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "68",
				"category_en_name" : "Face Cleaning Brush",
				"category_cn_name" : "洗脸刷",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "69",
				"category_en_name" : "Nose Hair Trimmer",
				"category_cn_name" : "鼻毛修剪器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "70",
				"category_en_name" : "Electric Nose Washing Apparatus",
				"category_cn_name" : "电动洗鼻器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "71",
				"category_en_name" : "Electric Tooth Cleaner",
				"category_cn_name" : "电动洗牙器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "72",
				"category_en_name" : "Massager",
				"category_cn_name" : "按摩器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "73",
				"category_en_name" : "Hemomanometer",
				"category_cn_name" : "血压计",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "74",
				"category_en_name" : "Blood Glucose Meter",
				"category_cn_name" : "血糖仪",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "75",
				"category_en_name" : "Blood Glucose Test Strips",
				"category_cn_name" : "血糖试纸",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "76",
				"category_en_name" : "Thermometer/Ear Thermometer",
				"category_cn_name" : "体温计/耳温计",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "77",
				"category_en_name" : "Uv Disinfection Stick",
				"category_cn_name" : "紫外线消毒棒",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "78",
				"category_en_name" : "Pedometer/Fat Detector",
				"category_cn_name" : "计步器/脂肪检测仪",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "79",
				"category_en_name" : "Other Small Household Appliance",
				"category_cn_name" : "其他家用小电器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "80",
				"category_en_name" : "Cooking Shovel and Spoon",
				"category_cn_name" : "烹饪铲勺",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "81",
				"category_en_name" : "Cookware",
				"category_cn_name" : "烹饪锅具",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "82",
				"category_en_name" : "Bowl/Plate/Saucer/Knives and Forks",
				"category_cn_name" : "碗/盆/碟/刀叉",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "83",
				"category_en_name" : "Knives/Scissors/Knife Sharpener",
				"category_cn_name" : "刀具/剪刀/磨刀器",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "84",
				"category_en_name" : "Tableware/Baby Tableware",
				"category_cn_name" : "家用餐具/宝宝餐具",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "85",
				"category_en_name" : "Seasoning Box",
				"category_cn_name" : "调味盒",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "86",
				"category_en_name" : "Bottle Opener/Vegetable Peeler",
				"category_cn_name" : "开瓶器/削皮器",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "87",
				"category_en_name" : "Ice Grid/Popsicle Grid",
				"category_cn_name" : "制冰格/冰棒模",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "88",
				"category_en_name" : "Eggbeater/Egg Molds",
				"category_cn_name" : "打蛋器/蛋模",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "89",
				"category_en_name" : "Filter Purifier",
				"category_cn_name" : "净水器（含过滤芯）",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "90",
				"category_en_name" : "Filter Element",
				"category_cn_name" : "净水器过滤芯",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "91",
				"category_en_name" : "Electric Ice Cream Makers",
				"category_cn_name" : "冰淇淋机（插电）",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "92",
				"category_en_name" : "Ice Cream Mold",
				"category_cn_name" : "雪糕机（不插电）",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "93",
				"category_en_name" : "Household Electric Cooker",
				"category_cn_name" : "家用电饭煲",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "94",
				"category_en_name" : "Household Microwave Oven",
				"category_cn_name" : "家用微波炉",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "95",
				"category_en_name" : "Household Electromagnetic Oven",
				"category_cn_name" : "家用电磁炉",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "96",
				"category_en_name" : "Household Smoke Exhaust Ventilator",
				"category_cn_name" : "家用抽油烟机",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "97",
				"category_en_name" : "Household Dish Washers",
				"category_cn_name" : "家用洗碗机",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "98",
				"category_en_name" : "Household Juicer ",
				"category_cn_name" : "家用电动榨汁机",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "99",
				"category_en_name" : "Household Coffee Maker",
				"category_cn_name" : "家用咖啡机",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "100",
				"category_en_name" : "Coat",
				"category_cn_name" : "上衣",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "101",
				"category_en_name" : "Suit",
				"category_cn_name" : "西装",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "102",
				"category_en_name" : "Waistcoat",
				"category_cn_name" : "马甲",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "103",
				"category_en_name" : "Wraps/Mantle",
				"category_cn_name" : "披肩/披风",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "104",
				"category_en_name" : "Down Jacket",
				"category_cn_name" : "羽绒服",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "105",
				"category_en_name" : "Trousers",
				"category_cn_name" : "外裤",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "106",
				"category_en_name" : "T-Shirt/Polo Shirt",
				"category_cn_name" : "T恤/Polo",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "107",
				"category_en_name" : "Hoodie",
				"category_cn_name" : "卫衣",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "108",
				"category_en_name" : "Sweat Pants",
				"category_cn_name" : "卫裤",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "109",
				"category_en_name" : "Shirt/T-shirt",
				"category_cn_name" : "衬衫/T恤衫",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "110",
				"category_en_name" : "Sweater/Knitwear",
				"category_cn_name" : "毛衣/针织衫",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "111",
				"category_en_name" : "Braces Skirt",
				"category_cn_name" : "吊带衫",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "112",
				"category_en_name" : "Dress",
				"category_cn_name" : "裙子",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "113",
				"category_en_name" : "Shorts",
				"category_cn_name" : "短裤",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "114",
				"category_en_name" : "Bra/Underclothes",
				"category_cn_name" : "文胸/内衣裤",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "115",
				"category_en_name" : "Pajamas/Pyjama Trousers/Night Skirt",
				"category_cn_name" : "睡衣/睡裤/睡裙",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "116",
				"category_en_name" : "Maternity Dress",
				"category_cn_name" : "孕妇装",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "117",
				"category_en_name" : "Baby/Kid's Clothes",
				"category_cn_name" : "婴儿服饰/童装",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "118",
				"category_en_name" : "Sock/Stocking",
				"category_cn_name" : "袜子",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "119",
				"category_en_name" : "Belt(Leather)",
				"category_cn_name" : "皮带（真皮）",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "120",
				"category_en_name" : "Belt(Non-Leather)",
				"category_cn_name" : "腰带（非皮质）",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "121",
				"category_en_name" : "Headgear",
				"category_cn_name" : "帽子",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "122",
				"category_en_name" : "Scarf/Kerchief",
				"category_cn_name" : "围巾/头巾",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "123",
				"category_en_name" : "Glove",
				"category_cn_name" : "手套",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "124",
				"category_en_name" : "Tie",
				"category_cn_name" : "领带",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "125",
				"category_en_name" : "Sleeve Button",
				"category_cn_name" : "袖扣",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "126",
				"category_en_name" : "Blanket/Quilt/sleeping bag",
				"category_cn_name" : "毛毯、被子、睡袋",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "127",
				"category_en_name" : "Pillow/Towel",
				"category_cn_name" : "枕头、毛巾被",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "128",
				"category_en_name" : "Textile Beddings",
				"category_cn_name" : "床上纺织用品",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "129",
				"category_en_name" : "Face Cream",
				"category_cn_name" : "面霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "130",
				"category_en_name" : "Eye Cream",
				"category_cn_name" : "眼霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "131",
				"category_en_name" : "Sun Cream",
				"category_cn_name" : "防晒/隔离霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "132",
				"category_en_name" : "Facial Cleanser",
				"category_cn_name" : "洗面奶/洁面霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "133",
				"category_en_name" : "Body Lotion",
				"category_cn_name" : "身体乳",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "134",
				"category_en_name" : "Essence",
				"category_cn_name" : "精华液",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "135",
				"category_en_name" : "Hand Lotion",
				"category_cn_name" : "护手霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "136",
				"category_en_name" : "Foundation Make-Up/Concealer",
				"category_cn_name" : "粉底/遮瑕膏",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "137",
				"category_en_name" : "Perfume",
				"category_cn_name" : "香水",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "138",
				"category_en_name" : "Toner",
				"category_cn_name" : "爽肤水",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "139",
				"category_en_name" : "Nail Polish",
				"category_cn_name" : "指甲油",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "140",
				"category_en_name" : "Lip Balm",
				"category_cn_name" : "润唇膏（保湿）",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "141",
				"category_en_name" : "Lip Gloss",
				"category_cn_name" : "唇膏唇彩（着色）",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "142",
				"category_en_name" : "Mask",
				"category_cn_name" : "面膜（以“张/片”计算）",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "143",
				"category_en_name" : "Cheek Powder",
				"category_cn_name" : "腮红",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "144",
				"category_en_name" : "Eyeliner",
				"category_cn_name" : "眼影/眼线",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "145",
				"category_en_name" : "Eyebrow Pencil",
				"category_cn_name" : "眉笔",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "146",
				"category_en_name" : "Mascara",
				"category_cn_name" : "睫毛膏",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "147",
				"category_en_name" : "Cleansing Water/Oil",
				"category_cn_name" : "卸妆水/卸妆油",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "148",
				"category_en_name" : "Hair Dyes/Wax",
				"category_cn_name" : "染发/造型",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "149",
				"category_en_name" : "Massage Oil",
				"category_cn_name" : "按摩精油",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "150",
				"category_en_name" : "Slimming Cream",
				"category_cn_name" : "纤体露",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "151",
				"category_en_name" : "Depilatory Cream",
				"category_cn_name" : "脱毛膏",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "152",
				"category_en_name" : "Cosmetic Kit",
				"category_cn_name" : "化妆品套装",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "153",
				"category_en_name" : "Cosmetic Brush/Powder Puff/Cleansing Cotton",
				"category_cn_name" : "化妆刷/面扑/卸妆棉",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "154",
				"category_en_name" : "Shampoo",
				"category_cn_name" : "洗发露",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "155",
				"category_en_name" : "Hair Conditioner",
				"category_cn_name" : "护发素",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "156",
				"category_en_name" : "Body Wash",
				"category_cn_name" : "沐浴乳",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "157",
				"category_en_name" : "Shaving Cream",
				"category_cn_name" : "剃须泡",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "158",
				"category_en_name" : "Scrub Cream/ Bath Salt",
				"category_cn_name" : "磨砂/浴盐",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "159",
				"category_en_name" : "Soap",
				"category_cn_name" : "香皂",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "160",
				"category_en_name" : "Depilatory Cream",
				"category_cn_name" : "脱毛膏",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "161",
				"category_en_name" : "Tooth Paste/Powder",
				"category_cn_name" : "牙膏/牙粉",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "162",
				"category_en_name" : "Tooth Brush",
				"category_cn_name" : "牙刷",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "163",
				"category_en_name" : "Dental Floss",
				"category_cn_name" : "牙线",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "164",
				"category_en_name" : "Mouthwash",
				"category_cn_name" : "漱口水",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "165",
				"category_en_name" : "Tampons",
				"category_cn_name" : "卫生护垫",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "166",
				"category_en_name" : "Feminine Hygiene Wash",
				"category_cn_name" : "女性护理液",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "167",
				"category_en_name" : "Pregnancy Test Kit",
				"category_cn_name" : "验孕试纸/验孕棒",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "168",
				"category_en_name" : "Skin Care Kit",
				"category_cn_name" : "护理套装",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "169",
				"category_en_name" : "Repellent Liquid/Cream",
				"category_cn_name" : "驱蚊膏/驱蚊液",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "170",
				"category_en_name" : "Sanitizer/Disinfectant",
				"category_cn_name" : "洗手液/消毒液",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "171",
				"category_en_name" : "Essential Oil",
				"category_cn_name" : "香薰精油",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "172",
				"category_en_name" : "Respirator",
				"category_cn_name" : "口罩",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "173",
				"category_en_name" : "Wallet/Purse/Zero Wallet",
				"category_cn_name" : "钱包/卡包/零钱包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "174",
				"category_en_name" : "Clutch",
				"category_cn_name" : "手拿包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "175",
				"category_en_name" : "Single-shoulder Bag",
				"category_cn_name" : "单肩包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "176",
				"category_en_name" : "Backpack",
				"category_cn_name" : "双肩包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "177",
				"category_en_name" : "Hand Bag",
				"category_cn_name" : "手提包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "178",
				"category_en_name" : "Laptop Bag",
				"category_cn_name" : "电脑数码包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "179",
				"category_en_name" : "Luggage",
				"category_cn_name" : "拉杆箱",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "180",
				"category_en_name" : "Waist Bag",
				"category_cn_name" : "腰包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "181",
				"category_en_name" : "Schoolbag",
				"category_cn_name" : "儿童书包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "182",
				"category_en_name" : "Cosmetic Bag",
				"category_cn_name" : "化妆包",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "183",
				"category_en_name" : "Casual Shoes",
				"category_cn_name" : "休闲鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "184",
				"category_en_name" : "Sneaker",
				"category_cn_name" : "运动鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "185",
				"category_en_name" : "Canvas Shoes",
				"category_cn_name" : "单鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "186",
				"category_en_name" : "Leather Shoes",
				"category_cn_name" : "真皮皮鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "187",
				"category_en_name" : "Sandal/Slippers",
				"category_cn_name" : "凉鞋/拖鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "188",
				"category_en_name" : "Boots",
				"category_cn_name" : "靴子",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "189",
				"category_en_name" : "Kid's Shoes",
				"category_cn_name" : "童鞋",
				"category_parent_id" : 11
			}, {
				"category_level" : 2,
				"category_id" : "190",
				"category_en_name" : "Quartz Watch",
				"category_cn_name" : "石英表",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "191",
				"category_en_name" : "Electronic Watch",
				"category_cn_name" : "电子表",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "192",
				"category_en_name" : "Mechanical Watch",
				"category_cn_name" : "机械表",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "193",
				"category_en_name" : "Luxury Watch(Values Over RMB 10,000)",
				"category_cn_name" : "高档手表(10000元以上)",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "194",
				"category_en_name" : "Kid's Swatch",
				"category_cn_name" : "儿童手表",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "195",
				"category_en_name" : "Alarm Clock",
				"category_cn_name" : "闹钟",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "196",
				"category_en_name" : "Sunglasses",
				"category_cn_name" : "太阳镜",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "197",
				"category_en_name" : "Glasses Frame",
				"category_cn_name" : "眼镜框",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "198",
				"category_en_name" : "Swimming Goggles",
				"category_cn_name" : "游泳眼镜",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "199",
				"category_en_name" : "Necklace",
				"category_cn_name" : "项链",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "200",
				"category_en_name" : "Pendant",
				"category_cn_name" : "吊坠",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "201",
				"category_en_name" : "Bracelets/Bangles",
				"category_cn_name" : "手链/手镯",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "202",
				"category_en_name" : "Ring",
				"category_cn_name" : "戒指",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "203",
				"category_en_name" : "Hair Accessory",
				"category_cn_name" : "发饰",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "204",
				"category_en_name" : "Ear Drop/Ring",
				"category_cn_name" : "耳环/耳钉",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "205",
				"category_en_name" : "Key Chain",
				"category_cn_name" : "钥匙扣",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "206",
				"category_en_name" : "Vitamin",
				"category_cn_name" : "维生素",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "207",
				"category_en_name" : "Albumen Powder",
				"category_cn_name" : "蛋白粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "208",
				"category_en_name" : "Fish Oil",
				"category_cn_name" : "鱼油",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "209",
				"category_en_name" : "Diet Health Product",
				"category_cn_name" : "减肥保健品",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "210",
				"category_en_name" : "Propolis",
				"category_cn_name" : "蜂胶",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "211",
				"category_en_name" : "Natural Health Food",
				"category_cn_name" : "天然保健品",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "212",
				"category_en_name" : "Coenzyme",
				"category_cn_name" : "辅酶",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "213",
				"category_en_name" : "Milk Powder",
				"category_cn_name" : "奶粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "214",
				"category_en_name" : "Rice Powder",
				"category_cn_name" : "米粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "215",
				"category_en_name" : "Puree",
				"category_cn_name" : "果泥/菜泥",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "216",
				"category_en_name" : "Biscuits/Puff",
				"category_cn_name" : "饼干/泡芙",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "217",
				"category_en_name" : "Solid Food",
				"category_cn_name" : "辅食",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "218",
				"category_en_name" : "Biscuits/Pastry",
				"category_cn_name" : "饼干糕点",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "219",
				"category_en_name" : "Cereal",
				"category_cn_name" : "麦片",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "220",
				"category_en_name" : "Dried Fruit/Preserved Fruit",
				"category_cn_name" : "干果/蜜饯",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "221",
				"category_en_name" : "Candy/Chocolate",
				"category_cn_name" : "糖果/巧克力",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "222",
				"category_en_name" : "Snack Food",
				"category_cn_name" : "零食",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "223",
				"category_en_name" : "Seasoning",
				"category_cn_name" : "调味品",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "224",
				"category_en_name" : "Honey",
				"category_cn_name" : "蜂蜜",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "225",
				"category_en_name" : "American Ginseng(slice/piece)",
				"category_cn_name" : "西洋参（片）",
				"category_parent_id" : 13
			}, {
				"category_level" : 3,
				"category_id" : "226",
				"category_en_name" : "American Ginseng Powder Product",
				"category_cn_name" : "西洋参（粉末）保健品",
				"category_parent_id" : 225
			}, {
				"category_level" : 2,
				"category_id" : "227",
				"category_en_name" : "Coffee/Drink Powder ",
				"category_cn_name" : "咖啡/冲调",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "228",
				"category_en_name" : "Tea",
				"category_cn_name" : "茶叶",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "229",
				"category_en_name" : "Wine",
				"category_cn_name" : "葡萄酒",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "230",
				"category_en_name" : "Brandy",
				"category_cn_name" : "白兰地",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "231",
				"category_en_name" : "Whiskey",
				"category_cn_name" : "威士忌",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "232",
				"category_en_name" : "Vodka",
				"category_cn_name" : "伏特加",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "233",
				"category_en_name" : "White Wine",
				"category_cn_name" : "白酒",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "234",
				"category_en_name" : "Beverage",
				"category_cn_name" : "饮料",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "235",
				"category_en_name" : "Cigarette",
				"category_cn_name" : "卷烟",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "236",
				"category_en_name" : "Cigar",
				"category_cn_name" : "雪茄",
				"category_parent_id" : 12
			}, {
				"category_level" : 2,
				"category_id" : "237",
				"category_en_name" : "Milk Bottle/Pacifier",
				"category_cn_name" : "奶瓶/奶嘴",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "238",
				"category_en_name" : "Feeding Bowl and Spoon for Baby",
				"category_cn_name" : "婴儿喂食碗勺",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "239",
				"category_en_name" : "Milk Storage Bag",
				"category_cn_name" : "婴儿辅食碾磨器",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "240",
				"category_en_name" : "Spill Prevention Breast Pad/",
				"category_cn_name" : "溢乳垫/储奶袋",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "241",
				"category_en_name" : "Breast Pump",
				"category_cn_name" : "吸奶器",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "242",
				"category_en_name" : "Baby Teether",
				"category_cn_name" : "婴儿牙胶",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "243",
				"category_en_name" : "Baby Diaper",
				"category_cn_name" : "纸尿裤",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "244",
				"category_en_name" : "Baby Shampoo",
				"category_cn_name" : "婴儿洗发沐浴露",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "245",
				"category_en_name" : "Eczema Ointment",
				"category_cn_name" : "湿疹药膏",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "246",
				"category_en_name" : "Nipple Cream",
				"category_cn_name" : "乳头霜",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "247",
				"category_en_name" : "Stretch Marks Massage Cream",
				"category_cn_name" : "妊娠纹按摩膏",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "248",
				"category_en_name" : "Maternal and Child Disinfection Supplies",
				"category_cn_name" : "母婴消毒用品",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "249",
				"category_en_name" : "Baby Clothes",
				"category_cn_name" : "婴儿服饰",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "250",
				"category_en_name" : "Baby Stroller/Bassinet",
				"category_cn_name" : "婴儿推车/童车",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "251",
				"category_en_name" : "Baby Straps",
				"category_cn_name" : "婴儿背带",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "252",
				"category_en_name" : "Child Safety Seat",
				"category_cn_name" : "儿童安全座椅",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "253",
				"category_en_name" : "Infanette/Cradle",
				"category_cn_name" : "婴儿床/摇篮",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "254",
				"category_en_name" : "Baby Toy",
				"category_cn_name" : "婴儿玩具",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "255",
				"category_en_name" : "Toy for Children",
				"category_cn_name" : "儿童玩具",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "256",
				"category_en_name" : "Medical Care",
				"category_cn_name" : "医药护理品",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "257",
				"category_en_name" : "Pregnant Women Underwear",
				"category_cn_name" : "孕妇内衣",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "258",
				"category_en_name" : "Radiation-proof Clothes",
				"category_cn_name" : "防辐射服",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "259",
				"category_en_name" : "Corset",
				"category_cn_name" : "塑身衣",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "260",
				"category_en_name" : "Scar Plaster",
				"category_cn_name" : "疤痕贴",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "261",
				"category_en_name" : "Antipruritic Ointment",
				"category_cn_name" : "止痒药膏",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "262",
				"category_en_name" : "Scar Ointment",
				"category_cn_name" : "祛疤药膏",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "263",
				"category_en_name" : "Res-Q Ointment",
				"category_cn_name" : "紫草膏",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "264",
				"category_en_name" : "All Better Balm(Ointment)",
				"category_cn_name" : "万用软膏（药膏）",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "265",
				"category_en_name" : "Talcum Powder",
				"category_cn_name" : "爽身粉",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "266",
				"category_en_name" : "Child Safety Seat",
				"category_cn_name" : "儿童安全座椅",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "267",
				"category_en_name" : "Car Telephone",
				"category_cn_name" : "车载电话",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "268",
				"category_en_name" : "Navigator",
				"category_cn_name" : "导航仪",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "269",
				"category_en_name" : "Vehicle Escape Hammer",
				"category_cn_name" : "车载逃生锤",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "270",
				"category_en_name" : "Other Vehicle Supplies",
				"category_cn_name" : "其他车载用品",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "271",
				"category_en_name" : "Car Maintenance Tools",
				"category_cn_name" : "车载维修工具",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "272",
				"category_en_name" : "Car Wax",
				"category_cn_name" : "车蜡",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "273",
				"category_en_name" : "Water-proof Coats",
				"category_cn_name" : "冲锋衣",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "274",
				"category_en_name" : "Water-proof Trousers",
				"category_cn_name" : "冲锋裤",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "275",
				"category_en_name" : "Outdoor Footwear",
				"category_cn_name" : "户外鞋靴",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "276",
				"category_en_name" : "Tent",
				"category_cn_name" : "帐篷",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "277",
				"category_en_name" : "Sleeping Bag",
				"category_cn_name" : "睡袋",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "278",
				"category_en_name" : "Moisture-proof Pad",
				"category_cn_name" : "防潮垫",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "279",
				"category_en_name" : "Telescope",
				"category_cn_name" : "望远镜",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "280",
				"category_en_name" : "Outdoor Tools",
				"category_cn_name" : "户外工具",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "281",
				"category_en_name" : "Swiss Army Knife",
				"category_cn_name" : "瑞士军刀",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "282",
				"category_en_name" : "Outdoor Instrument",
				"category_cn_name" : "户外仪表",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "283",
				"category_en_name" : "Outdoor Lighting Equipment",
				"category_cn_name" : "户外照明",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "284",
				"category_en_name" : "ZIPPO Lighter(Oil Free)",
				"category_cn_name" : "ZIPPO打火机（无油）",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "285",
				"category_en_name" : "Picnic Cookware",
				"category_cn_name" : "野餐炊具",
				"category_parent_id" : 2
			}, {
				"category_level" : 2,
				"category_id" : "286",
				"category_en_name" : "Swimming Glasses",
				"category_cn_name" : "游泳眼镜",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "287",
				"category_en_name" : "Fishing Rod/Gear",
				"category_cn_name" : "鱼竿/渔具",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "288",
				"category_en_name" : "Swimming Suit",
				"category_cn_name" : "泳衣",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "289",
				"category_en_name" : "Ski",
				"category_cn_name" : "滑雪板",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "290",
				"category_en_name" : "Ice Skates",
				"category_cn_name" : "滑冰鞋",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "291",
				"category_en_name" : "Fitness Equipment",
				"category_cn_name" : "健身器械",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "292",
				"category_en_name" : "Bicycle",
				"category_cn_name" : "自行车",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "293",
				"category_en_name" : "Bicycle Parts",
				"category_cn_name" : "自行车配件",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "294",
				"category_en_name" : "Helmet",
				"category_cn_name" : "头盔",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "295",
				"category_en_name" : "Pedometer/Heart Rate Monitor",
				"category_cn_name" : "计步器/心率器",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "296",
				"category_en_name" : "Sports Wristband",
				"category_cn_name" : "运动腕带",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "297",
				"category_en_name" : "Kneecap/Elbow Pad",
				"category_cn_name" : "护膝/护肘",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "298",
				"category_en_name" : "Brassie",
				"category_cn_name" : "高尔夫球杆",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "299",
				"category_en_name" : "Other Sports Instrument",
				"category_cn_name" : "其他运动器具",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "300",
				"category_en_name" : "Musical Instrument",
				"category_cn_name" : "乐器",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "301",
				"category_en_name" : "Reference Book/Text Book",
				"category_cn_name" : "教科书籍",
				"category_parent_id" : 14
			}, {
				"category_level" : 3,
				"category_id" : "302",
				"category_en_name" : "Educational Videotape",
				"category_cn_name" : "教育用录像带",
				"category_parent_id" : 301
			}, {
				"category_level" : 2,
				"category_id" : "303",
				"category_en_name" : "Educational Movie",
				"category_cn_name" : "教育用电影片",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "304",
				"category_en_name" : "Educational Slide",
				"category_cn_name" : "教育用幻灯片",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "305",
				"category_en_name" : "Pen",
				"category_cn_name" : "笔",
				"category_parent_id" : 14
			}, {
				"category_level" : 2,
				"category_id" : "306",
				"category_en_name" : "Storage Products",
				"category_cn_name" : "收纳用品",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "307",
				"category_en_name" : "Umbrella and Rain Gear",
				"category_cn_name" : "雨伞雨具",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "308",
				"category_en_name" : "Leather Cleaner",
				"category_cn_name" : "皮革清洁剂",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "309",
				"category_en_name" : "Bathroom Hardware",
				"category_cn_name" : "卫浴五金",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "310",
				"category_en_name" : "Adult Products",
				"category_cn_name" : "成人用品",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "311",
				"category_en_name" : "Home Soft Decoration",
				"category_cn_name" : "家装软饰",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "312",
				"category_en_name" : "Teether",
				"category_cn_name" : "磨牙棒",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "313",
				"category_en_name" : "Oral Medicine Syringe",
				"category_cn_name" : "喂药器",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "314",
				"category_en_name" : "Ear Cleaning Powder",
				"category_cn_name" : "洗耳粉",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "315",
				"category_en_name" : "Pet Shampoo/Body Wash",
				"category_cn_name" : "宠物沐浴露",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "316",
				"category_en_name" : "Pet Solid Food",
				"category_cn_name" : "宠物辅食",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "317",
				"category_en_name" : "Pet Grooming Products",
				"category_cn_name" : "宠物美容用品",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "318",
				"category_en_name" : "Pet Clothing",
				"category_cn_name" : "宠物服饰",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "319",
				"category_en_name" : "Pet Collars, Tags & Leashes",
				"category_cn_name" : "宠物牵引绳/训练绳",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "320",
				"category_en_name" : "Calcium Tablets",
				"category_cn_name" : "钙片",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "321",
				"category_en_name" : "Colostrum",
				"category_cn_name" : "牛初乳",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "322",
				"category_en_name" : "Docosahexaenoic Acid/Omega 3",
				"category_cn_name" : "DHA",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "323",
				"category_en_name" : "Other clothes",
				"category_cn_name" : "其他衣着",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "324",
				"category_en_name" : "Other items",
				"category_cn_name" : "其他物品",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "348",
				"category_en_name" : "Acne treatment cream",
				"category_cn_name" : "祛疤膏/祛疤笔",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "346",
				"category_en_name" : "Blemish Balm",
				"category_cn_name" : "BB霜",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "325",
				"category_en_name" : "Manual Shaving Device",
				"category_cn_name" : "手动剃毛器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "347",
				"category_en_name" : "Bright liquid / high gloss paste",
				"category_cn_name" : "提亮液/高光膏",
				"category_parent_id" : 1
			}, {
				"category_level" : 2,
				"category_id" : "338",
				"category_en_name" : "Coffee Bean",
				"category_cn_name" : "咖啡豆",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "339",
				"category_en_name" : "Cocoa Powder",
				"category_cn_name" : "可可粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "340",
				"category_en_name" : "Band Aid",
				"category_cn_name" : "创可贴",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "341",
				"category_en_name" : "Vegetable Washing Powder",
				"category_cn_name" : "洗菜粉",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "342",
				"category_en_name" : "Eye Patch",
				"category_cn_name" : "眼罩",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "343",
				"category_en_name" : "Manual Razor",
				"category_cn_name" : "手动剃须刀",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "344",
				"category_en_name" : "Detergent",
				"category_cn_name" : "洗洁精",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "345",
				"category_en_name" : "Washing Powder/Laundry Detergent",
				"category_cn_name" : "洗衣粉/洗衣液",
				"category_parent_id" : 3
			}, {
				"category_level" : 2,
				"category_id" : "334",
				"category_en_name" : "infant milk powder",
				"category_cn_name" : "婴儿奶粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "335",
				"category_en_name" : "adult milk powder",
				"category_cn_name" : "成人奶粉",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "349",
				"category_en_name" : "",
				"category_cn_name" : "其他饰品",
				"category_parent_id" : 9
			}, {
				"category_level" : 2,
				"category_id" : "350",
				"category_en_name" : "",
				"category_cn_name" : "牛奶",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "351",
				"category_en_name" : "",
				"category_cn_name" : "核桃油/橄榄油",
				"category_parent_id" : 13
			}, {
				"category_level" : 2,
				"category_id" : "326",
				"category_en_name" : "Electric Hair Removal Device",
				"category_cn_name" : "电动脱毛器",
				"category_parent_id" : 6
			}, {
				"category_level" : 2,
				"category_id" : "327",
				"category_en_name" : "Kettle/Cup",
				"category_cn_name" : "水壶/水杯",
				"category_parent_id" : 4
			}, {
				"category_level" : 2,
				"category_id" : "328",
				"category_en_name" : "Girdle",
				"category_cn_name" : "托腹带",
				"category_parent_id" : 7
			}, {
				"category_level" : 2,
				"category_id" : "329",
				"category_en_name" : "Portable Bluetooth Stereo",
				"category_cn_name" : "便携蓝牙音响(IHOME)",
				"category_parent_id" : 10
			}, {
				"category_level" : 2,
				"category_id" : "330",
				"category_en_name" : "Leather Jacket",
				"category_cn_name" : "皮上衣",
				"category_parent_id" : 5
			}, {
				"category_level" : 2,
				"category_id" : "331",
				"category_en_name" : "Eye Drops",
				"category_cn_name" : "眼药水",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "332",
				"category_en_name" : "Foot Patch",
				"category_cn_name" : "足贴",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "333",
				"category_en_name" : "Shoulder Patch",
				"category_cn_name" : "肩贴",
				"category_parent_id" : 8
			}, {
				"category_level" : 2,
				"category_id" : "352",
				"category_en_name" : "",
				"category_cn_name" : "面膜（以“毫升/克”计算）",
				"category_parent_id" : 1
			}
		],
		"version" : "1.0"
	}
}
```