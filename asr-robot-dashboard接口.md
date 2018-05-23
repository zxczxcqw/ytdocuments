# ytdocuments
asr-robot-dashboard接口文档

```json
//接口功能添加修改初始化数据
//接口地址/api_backend.php?r=asroperate/asrinit，修改初始化需传参数AsrId
{
   "info":
    {
        "used_ai_count":"7", //使用的AI数量
        "company_ai_count":"10", //公司总共AI数量
        "availue_ai_count":3, //可用机器人数量
        "aicall_max_rate":"1", //备用标识（数据库是这么备注的）
        "asrcall_max_line":3, //外呼并发数最大值
        "callid_list":[ //外线号码 和 语音线路
             {"num": "66660011","alias": "上海言通"}
         ],
        "ext_list":[ //分机号列表
            {"id": "1","type": "friend", "name": "1001"},
            {"id": "10", "type": "friend", "name": "1010"}
        ],
        "staff_id":[ //分机号列表
            {"staff_id": "1002","staff_name": "1010"},
        ],
        "asr_info":
          {   "id":"7",  //机器人id
              "company_id":"3", //公司id
              "staff_id":"1008", //所属客服id
              "status":"0",   //群呼状态：0 关闭 1 启动
              "caller_id":"610099255", //外呼显示号码
              "concurrent_line":"1",  //并发线
              "asr_number":"7900001",  //语音识别线路
              "batchid_str":"",     //逗号分割的批次ID字符串
              "exten_num":"mobile13880615750",   //转接的分机号（不是工号）
              "name":"四川话测试",   //群呼名称
              "sms_switch":"0",     //短信开关：0 关 1 开
              "sms_fee" :"0.08",     //短信费用：默认8分
              "start_time":"08:00:00",  //群呼开始时间
              "end_time":"21:00:00",    //群呼结束时间
              "auth_time":"2019-03-23 13:09:29", //授权到期时间
              "creater":null,  //创建者
              "create_time":"2018-03-23 13:09:29",  //创建时间
              "ai_count":"4",    //机器人数量
              "enable_daemon_call":"0",  //启用后台呼叫标志，1启用，0关闭
              "man_machine_interaction":"转手机:13880615750", //人机交互
              "extnum_list":[] //分机号列表
        } //添加时为空(修改时传参数 AsrId 获取)
    }
}


//获取所有机器人信息，或获取单个机器人信息
//接口地址 /api_backend.php?r=asroperate/asrinfo，可传参数AsrId 获取单个机器人信息
{
 "info":
          {   "id":"7",  //机器人id
              "company_id":"3", //公司id
              "staff_id":"1008", //所属客服id
              "status":"0",   //群呼状态：0 关闭 1 启动
              "caller_id":"610099255", //外呼显示号码
              "concurrent_line":"1",  //并发线
              "asr_number":"7900001",  //语音识别线路
              "batchid_str":"",     //逗号分割的批次ID字符串
              "exten_num":"mobile13880615750",   //转接的分机号（不是工号）
              "name":"四川话测试",   //群呼名称
              "sms_switch":"0",     //短信开关：0 关 1 开
              "sms_fee" :"0.08",     //短信费用：默认8分
              "start_time":"08:00:00",  //群呼开始时间
              "end_time":"21:00:00",    //群呼结束时间
              "auth_time":"2019-03-23 13:09:29", //授权到期时间
              "creater":null,  //创建者
              "create_time":"2018-03-23 13:09:29",  //创建时间
              "ai_count":"4",    //机器人数量
              "enable_daemon_call":"0",  //启用后台呼叫标志，1启用，0关闭
              "man_machine_interaction":"转手机:13880615750", //人机交互
              "extnum_list":[] //分机号列表
        } //添加时为空(修改时传参数 AsrId 获取)
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
    "caller_id": "610099255",    //外呼显示号码
    "concurrent_line": "1",      //并发线
    "asr_number": "7900002",     //语音识别线路
    "batchid_str": "15,20,30",   //逗号分割的批次ID字符串
    "name": "四川话测试",    //群呼名称
    "sms_switch": "0",  //短信开关：0 关 1 开
    "start_time": "08:00:00", //群呼开始时间
    "end_time": "21:00:00",      //群呼结束时间
    "ai_count": "4", //机器人数量
    "agent_or_queue": "1"//交互方式 1转手机，2转分机，3队列
    "exten_num":  //分机号（转分机） 
    "asr_to_mobile": //手机号（转手机）
    "asr_queue": //队列（队列）
    "enable_daemon_call": "0", //启用后台呼叫标志，1启用，0关闭
}

```
