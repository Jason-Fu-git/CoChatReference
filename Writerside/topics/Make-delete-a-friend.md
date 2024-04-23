# Make / Delete a friend

> 此接口有三种调用时机：
> - A 向 B 发出添加好友的申请
> - B 收到了 A 的申请，并做出回应，此时`approve`字段起作用
> - A 和 B 已经是朋友，但是 B 想把 A 删掉，此时`approve`字段必须为`false`
> 
{style="note"}

> `group` 字段若为空，则默认置为 `ungrouped`. 该字段可在
> 1. 发送好友申请
> 2. 接受好友申请
> 3. 已经建立好友关系，更改好友分组
> 
> 时添加。
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}/friends" method="PUT">
</api-endpoint>