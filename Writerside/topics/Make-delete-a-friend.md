# Make / Delete a friend

> 此接口有三种调用时机：
> - A 向 B 发出添加好友的申请
> - B 收到了 A 的申请，并做出回应，此时`approve`字段起作用
> - A 和 B 已经是朋友，但是 B 想把 A 删掉，此时`approve`字段必须为`false`
> 
{style="note"}

<api-endpoint openapi-path="../cochat.yaml" endpoint="/api/user/{userid}/friends" method="PUT">
</api-endpoint>