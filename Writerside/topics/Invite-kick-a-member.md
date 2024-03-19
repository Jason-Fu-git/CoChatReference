# Invite / Kick a member

> 此接口有三种调用时机
> - A 邀请 B 加入群聊 C
> - B 收到了 A 的邀请，并回复，此时`approve`接口起作用
> - A 把 B 踢出群聊 C，此时 `approve`必须为`false`
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/management" method="put">

</api-endpoint>