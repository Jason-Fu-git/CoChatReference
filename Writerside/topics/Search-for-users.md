# Search for users

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user" method="GET">

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
            "avatar" : "{FILE BINARY}",
        },
        {...},
        ...
    ]
}
</sample>
</response>

</api-endpoint>