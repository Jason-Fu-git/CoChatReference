# Get a message

> 文件怎么传还没想好，先空着
> 
{style="warning"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/message/{messageid}/management" method="GET">

<response type="200">
<sample>
{
    "code" : 0,
    "info" : Success,
    "msg_id" : 1,
    "sender_id" : 1,
    "chat_id" : 1,
    "msg_text" : "I published the Republic",
    "msg_type" : "T",
    "create_time" : 1710836514,
    "update_time" : 2308102839,
    "read_users" : [
                        1,
                        2,
                        ...
                    ],
    "unable_to_see_users" : [
                                1,
                                2,
                                ...
                            ],
    "reply_to" : -1,
    "is_system" : false,
    "msg_file_url" : "/api/message/files/2"
}
</sample>
</response>

</api-endpoint>