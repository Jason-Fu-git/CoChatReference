# Post a message

> 注意：即使传的是文件，也必须有`msg_text`字段！
> 
{style="warning"}

> 消息类型为'group_notice'时，发送群公告。仅群主、群管理员可发送
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/message/send" method="POST">

<response type="200">

<sample>
{
    "code" : 0,
    "info" : "Success",
    "msg_id" : 1,
    "create_time" : 1710836514,
}
</sample>

</response>

</api-endpoint>