# Log user into the system

<api-endpoint openapi-path="./../cotalk.yaml" endpoint="/api/user/login" method="post">
<response type="200">

<sample>
    {
        "code" : 0,
        "info" : "Success",
        "token" : "***.***.***",
        "user_id" : 1,
        "user_name" : "Plato",
        "user_email" : "Plato@163.com",
        "user_phone" : "2830923",
        "description": "A great philosopher",
        "register_time" : 1712025307.24112,
        "avatar" : "{FILE BINARY}"
    }
</sample>

</response>
</api-endpoint>
