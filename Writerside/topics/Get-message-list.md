# Get message list

> 对于文件类消息，不会返回源文件，需要针对对应message的id利用get方法获取
> 
{style="note"}

> **关于历史记录搜索** 
>
> Query string 可以任意组合、任意顺序添加过滤器字段，返回所有过滤器过滤结果的交集
> 
> - 样例1
>   - url : `/api/chat/{chatid}/messages?user_id={userid}`
>   - 返回该聊天中的所有消息
> - 样例2
>   - url : `/api/chat/{chatid}/messages?user_id={userid}&filter_user=2&filter_text='tsinghua'`
>   - 返回该聊天中`user_id=2`的成员所发消息中包含'tsinghua'(大小写敏感)的所有消息
> - 样例3
>   - url : `/api/chat/{chatid}/messages?user_id={userid}&filter_before=3000&filter_after=1000`
>   - 返回该聊天中所有时间介于[1000,3000]之间发的消息.
> 
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/messages" method="GET">

<response type="200">

<sample>
{
    "code" : 0,
    "info" : "Success",
    "messages" : [
        {
            "info" : Success,
            "msg_id" : 1,
            "sender_id" : 1,
            "chat_id" : 1,
            "msg_text" : "I published the Republic",
            "msg_type" : "text",
            "create_time" : 1710836514,
            "update_time" : 2308102839,
            "read_users" : [
                            1,
                            2,
                            ...
                        ],
            "reply_to" : -1,
            "is_system" : false,
            "msg_file_url" : "/api/message/files/2"
        },
        ...
    ]
}
</sample>

</response>

</api-endpoint>