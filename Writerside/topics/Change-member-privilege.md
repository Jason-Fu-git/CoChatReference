# Change member privilege

> 权限说明：
>
> - 修改对方为“群主”（唯一）：仅群主
> - 修改对方为“管理员”（至多三个）：仅群主
> - 修改对方为“成员”：仅群主
> 
> 若修改对方为“群主”，自己的权限变为“成员”（如果后端成功响应）
>
{style="note"}

成员权限修改后，添加系统消息 "A changed B's privilege to admin" (例)，并利用Notification或Websocket通知对方。

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/management" method="PUT">


</api-endpoint>