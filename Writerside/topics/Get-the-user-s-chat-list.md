# Get the user&apos;s chat list

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/{userid}/chats" method="GET">

<response type="200">
<sample>
{
    "code" : 0,
    "info" : "Success",
    "chats": [
        {
            "chat_id" : 1,
            "chat_name" : "Athens",
            "is_private" : true,
        },
        {...},
        ...
    ]
}
</sample>
</response>

</api-endpoint>