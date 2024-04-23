# Get the user&apos;s friend list

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}/friends" method="GET">

<response type="200">
<sample>
{
    "code" : 0,
    "info" : "Success",
    "friends": [
        {
            "user_id" : 1,
            "user_name" : "Plato",
            "user_email" : "Plato@163.com",
            "description" : "A great philosopher",
            "register_time" : 1712025307.24112,
            "group" : "ungrouped"
            "avatar" : "{FILE BINARY}",
        },
        {...},
        ...
    ]
}
</sample>
</response>

</api-endpoint>