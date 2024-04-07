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
    "msg_text" : "I published the Republic",
    "msg_type" : "text",
    "create_time" : 1710836514,
    "read_users" : [
                        1,
                        2,
                        ...
                    ]
    "msg_file" : "{FILE_BINARY}"
}
</sample>
</response>

</api-endpoint>