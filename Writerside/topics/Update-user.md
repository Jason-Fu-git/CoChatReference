# Update user

> Security Warning
> 
> 修改密码的时候不安全，后续开发时添加密码验证或2FA
> 
{style="warning"}

<!-- Use multiple <sample> elements inside <request> to provide samples for various programming languages. 
They will be placed in tabs.Developers can use these samples as templates when making requests to this endpoint. -->

<api-endpoint openapi-path="./../cotalk.yaml" endpoint="/api/user/{userid}" method="put">

<request>
<sample>
    {
        "user_name" : "Plato",
        "password" : "123456",
        "user_email" : "Plato@163.com",
        "avatar" : "{FILE BINARY}"
    }
</sample>

</request>

</api-endpoint>
