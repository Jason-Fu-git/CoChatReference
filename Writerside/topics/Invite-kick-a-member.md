# Invite / Kick a member

> 此接口有三种调用时机
> - A 邀请 B 加入群聊 C
> - B 收到了 A 的邀请，并回复，此时`approve`字段起作用
> - A 把 B 踢出群聊 C，此时 `approve`必须为`false`
>
{style="note"}

> 权限说明：
> 
> - 邀请成员：任何人均可邀请
> - 删除成员：仅群主/管理员
>
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/members" method="put">

</api-endpoint>