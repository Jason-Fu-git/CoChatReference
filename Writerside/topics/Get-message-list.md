# Get message list

> 对于文件类消息，不会返回源文件，需要针对对应message的id利用get方法获取
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
            "msg_id" : 1,
            "sender_id" : 1,
            "msg_text" : "I published the Republic",
            "msg_type" : "text",
            "create_time" : 1710836514,
            "read_users" : [
                1,
                2,
                ...
            ]
        },
        ...
    ]
}
</sample>

</response>

</api-endpoint>