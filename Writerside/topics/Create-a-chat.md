# Create a chat

> 关于群聊/私聊：
> 
> - 私聊唯一性：私聊只能有一个，且名称只能为好友的昵称
> - 群名唯一性：聊天名不能重复
> - 确认问题：群聊发出邀请后，对方需确认才能加入
>
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/" method="post">

<response type="200">

<sample>
{
    "code" : 0,
    "info" : "Success",
    "chat_id" : 1,
    "create_time" : 1710836514,
}
</sample>

</response>

</api-endpoint>