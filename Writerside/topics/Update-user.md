# Update user

> 支持的头像扩展名包括：`.png`, `.jpg`, `.jpeg`
>
{style="note"}

> 修改密码时需要2FA，请求体必填`password`和`code`两个字段。
> 
> 修改用户其他信息时，不需要验证。
> 
{style="note"}

不必传入所有字段，按需传入即可。

<!-- Use multiple <sample> elements inside <request> to provide samples for various programming languages. 
They will be placed in tabs.Developers can use these samples as templates when making requests to this endpoint. -->

<api-endpoint openapi-path="./../cotalk.yaml" endpoint="/api/user/private/{user_id}" method="post">

</api-endpoint>
