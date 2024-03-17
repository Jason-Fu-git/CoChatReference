# Update user

<!-- Use multiple <sample> elements inside <request> to provide samples for various programming languages. 
They will be placed in tabs.Developers can use these samples as templates when making requests to this endpoint. -->

<api-endpoint openapi-path="./../cochat.yaml" endpoint="/api/user/{username}" method="post">

<request>
<sample>
    {
        "token" : "***.***.***"
        "user_name" : "Plato",
        "password" : "123456",
        "user_email" : "Plato@163.com",
        "avatar" : "{FILE BINARY}"
    }
</sample>

</request>

<response type="200">

<sample>
    {
        "code" : 0,
        "info" : "Success",
        "token" : "***.***.***"
        "user_name" : "Plato",
        "password" : "123456",
        "user_email" : "Plato@163.com",
        "avatar" : "{FILE BINARY}"
    }
</sample>

</response>
</api-endpoint>
