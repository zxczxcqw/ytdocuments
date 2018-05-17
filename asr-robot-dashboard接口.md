# ytdocuments
asr-robot-dashboard接口文档

```json
{
    "info":
    {
        "UsedAICount":"7", //使用的AI数量
        "CompanyAICount":"10", //公司总共AI数量
        "AvailueAICount":3, //可用机器人数量
        "AICallMaxRate":"1", //备用标识（数据库是这么备注的）
        "AsrCallMaxLine":3, //外呼并发数最大值
        "callIdList":[          //外线号码
            {"Num": "66660011"},
            {"Num": "66660010"},
            {"Num": "66660009"},
            {"Num": "66660008"},
            {"Num": "66660007"},
            {"Num": "66660006"},
            {"Num": "66660005"},
            {"Num": "66660004"},
            {"Num": "66660003"},
            {"Num": "66660002"},
            {"Num": "66660001"},
            {"Num": "88851554227"},
            {"Num": "32432423"}
        ],
        "alias":"32432423", //语音线路
        "ExtList":[   //分机号列表
            {"id": "3", "type": "friend", "name": "1003"},
            {"id": "4", "type": "friend", "name": "1004"},
            {"id": "5", "type": "friend", "name": "1005"},
            {"id": "6", "type": "friend", "name": "1006"},
            {"id": "7", "type": "friend", "name": "1007"},
            {"id": "8", "type": "friend", "name": "1008"},
            {"id": "9", "type": "friend", "name": "1009"},
            {"id": "10", "type": "friend", "name": "1010"}
        ],
        "StaffId":[  //公司坐席号id
            {"StaffId": "1003"},
            {"StaffId": "1004"},
            {"StaffId": "1005"},
            {"StaffId": "1006"},
            {"StaffId": "1007"},
            {"StaffId": "1008"},
            {"StaffId": "1009"},
            {"StaffId": "1010"}
        ]
    }
}


```
