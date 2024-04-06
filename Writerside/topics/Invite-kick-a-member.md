# Invite / Kick a member

> 此接口有三种调用时机
> - A 邀请 B 加入群聊 C
> - B 收到了 A 的邀请，不回复，此时`approve`字段起作用, `member_id`与`user_id`相等
> - A 把 B 踢出群聊 C，此时 `approve`必须为`false`
>
{style="note"}

> 权限说明：
>
> - 邀请成员：任何人均可邀请
> - 删除成员：仅群主/管理员，且群主不能被删除
>
{style="note"}

> 如果该成员退出聊天后，聊天中一个人都没有，则该聊天自动删除。
> 
> 群主退出后，群主权交给管理员/成员
> 
{style='warning'}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/members" method="put">

</api-endpoint>