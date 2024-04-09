# Invite / Kick a member

> 此接口有三种调用时机
> - A 邀请 B 加入群聊 C
>   - A 向 B 发送 Notification 或 websocket， 详情参见[Chat management](Chat-management.md)
> - B 收到了 A 的邀请，并回复，此时`approve`字段起作用, `member_id`与`user_id`相等
>   -  在这种情况下，如果 B 同意邀请，则添加系统消息："B joined the chat." 此消息全体聊天参与者可见。
>   - 注：不管B作何反应，不会添加任何 Notification
> - A 把 B 踢出群聊 C，此时 `approve`必须为`false`
>   - 添加系统消息： "A kicked B out of the chat." 此消息全体聊天参与者可见
>   - A 向 B 发送 Notification 或 websocket， 详情参见[Chat management](Chat-management.md)
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