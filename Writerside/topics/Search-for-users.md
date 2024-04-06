# Search for users

> 如欲获取所有用户，请对`/api/user/search` 调用GET方法
>
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/search/{search_text}" method="GET">

<response type="200">
<sample>
{
    "code" : 0,
    "info" : "Success",
    "users": [
        {
            "user_id" : 1,
            "user_name" : "Plato",
            "user_email" : "Plato@163.com",
            "description" : "A great philosopher",
            "register_time" : 1712025307.24112,
            "avatar" : "{FILE BINARY}",
        },
        {...},
        ...
    ]
}
</sample>
</response>

</api-endpoint>