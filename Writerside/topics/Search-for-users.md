# Search for users

> 当搜索词为空时，返回所有用户
> 
> 否则，从用户名、用户邮箱、用户描述中寻找匹配项
>
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/search" method="GET">

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
            "user_phone" : "28139021",
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