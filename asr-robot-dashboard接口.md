# ytdocuments
asr-robot-dashboard接口文档

```json
//接口功能添加修改初始化数据
//接口地址/api_backend.php?r=asroperate/asrinit，修改初始化需传参数AsrId
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
        ]
        "AliasList":[ //语音线路列表
            {"alias":"66660011"}
        ], 
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
        ]，
        "asrInfo":
        {
             "Id": "7",              //机器人id
            "CompanyId": "3",       //公司id
            "staff_id": "1008",     //所属客服id
            "Status": "0",          //群呼状态：0 关闭 1 启动
            "CallerID": "610099255",    //外呼显示号码
            "ConcurrentLine": "1",      //并发线
            "asrnumber": "7900002",     //语音识别线路
            "BatchIdStr": "15,20,30",   //逗号分割的批次ID字符串
            "ExtenNum": "mobile13880615750", //转接的分机号（不是工号）
            "Name": "四川话测试",    //群呼名称
            "sms_switch": "0",  //短信开关：0 关 1 开
            "sms_fee": "0.08",  //短信费用：默认8分
            "StartTime": "08:00:00", //群呼开始时间
            "EndTime": "21:00:00",      //群呼结束时间
            "AuthTime": "2019-03-24 23:22:22", //授权到期时间
            "Creater": null, //创建者
            "CreateTime": "2018-03-23 13:09:29", //创建时间
            "aicount": "4", //机器人数量
            "EnableDaemonCall": "0", //启用后台呼叫标志，1启用，0关闭
            "ManMachineInteraction": "转手机:13880615750",  //人机交互
            "ExtNumList": [], //分机号列表
        } //添加时为空(修改时传参数 AsrId 获取)
    }
}


//获取所有机器人信息，或获取单个机器人信息
//接口地址 /api_backend.php?r=asroperate/asrinfo，可传参数AsrId 获取单个机器人信息
{
     "info":
     [
         {
            "Id": "7",              //机器人id
            "CompanyId": "3",       //公司id
            "staff_id": "1008",     //所属客服id
            "Status": "0",          //群呼状态：0 关闭 1 启动
            "CallerID": "610099255",    //外呼显示号码
            "ConcurrentLine": "1",      //并发线
            "asrnumber": "7900002",     //语音识别线路
            "BatchIdStr": "15,20,30",   //逗号分割的批次ID字符串
            "ExtenNum": "mobile13880615750", //转接的分机号（不是工号）
            "Name": "四川话测试",    //群呼名称
            "sms_switch": "0",  //短信开关：0 关 1 开
            "sms_fee": "0.08",  //短信费用：默认8分
            "StartTime": "08:00:00", //群呼开始时间
            "EndTime": "21:00:00",      //群呼结束时间
            "AuthTime": "2019-03-24 23:22:22", //授权到期时间
            "Creater": null, //创建者
            "CreateTime": "2018-03-23 13:09:29", //创建时间
            "aicount": "4", //机器人数量
            "EnableDaemonCall": "0", //启用后台呼叫标志，1启用，0关闭
            "ManMachineInteraction": "转手机:13880615750",  //人机交互
            "ExtNumList": [], //分机号列表
         }
    ]
}


//接口获取批次id
//接口地址/api_backend.php?r=asroperate/batchlist，无需参数
{
     "info":
     [
         {   "id": "92",   //批次id
             "name": "exce3" //批次名称
         },
    ]
}


//接口功能添加修改机器人
//接口地址/api_backend.php?r=asroperate/addasr
//参数说明
{
    "CallerID": "610099255",    //外呼显示号码
    "ConcurrentLine": "1",      //并发线
    "asrnumber": "7900002",     //语音识别线路
    "BatchIdStr": "15,20,30",   //逗号分割的批次ID字符串
    "Name": "四川话测试",    //群呼名称
    "sms_switch": "0",  //短信开关：0 关 1 开
    "StartTime": "08:00:00", //群呼开始时间
    "EndTime": "21:00:00",      //群呼结束时间
    "aicount": "4", //机器人数量
    "agentorqueue": "1"//交互方式 1转手机，2转分机，3队列
    "ExtenNum":  //分机号（转分机） 
    "asrtomobile": //手机号（转手机）
    "asrqueue": //队列（队列）
    "EnableDaemonCall": "0", //启用后台呼叫标志，1启用，0关闭
}

```
