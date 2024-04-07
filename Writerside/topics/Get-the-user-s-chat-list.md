# Get the user&apos;s chat list

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}/chats" method="GET">

<response type="200">
<sample>
{
    "code" : 0,
    "info" : "Success",
    "chats": [
        {
            "chat_id" : 1,
            "chat_name" : "Athens",
            "create_time" : 1712025307.24112,
            "is_private" : true,
        },
        {...},
        ...
    ]
}
</sample>
</response>

</api-endpoint>