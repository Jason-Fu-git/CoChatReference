# Update user

> 支持的头像扩展名包括：`.png`, `.jpg`, `.jpeg`
>
{style="note"}

> 修改密码时需要2FA，请求体必填`password`和`code`两个字段。
> 
> 修改用户其他信息时，不需要验证。
> 
{style="note"}

> - 对除密码外字段的修改，需要在`old_password`字段传入原密码
> - 对密码的修改，需要邮箱验证码
> 
> 因此，建议前端设计两个页面。第一个页面可以更改除密码外的个人信息，但必填原密码。在第一个页面增加“忘记密码”链接，以重置密码。
>
{style="note"}

不必传入所有字段，按需传入即可。

<!-- Use multiple <sample> elements inside <request> to provide samples for various programming languages. 
They will be placed in tabs.Developers can use these samples as templates when making requests to this endpoint. -->

<api-endpoint openapi-path="./../cotalk.yaml" endpoint="/api/user/private/{user_id}" method="post">

</api-endpoint>
