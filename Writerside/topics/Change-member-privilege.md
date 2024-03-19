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


<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/chat/{chatid}/management" method="PUT">


</api-endpoint>