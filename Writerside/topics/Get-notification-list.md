# Get notification list

> url 示例
>  `/api/user/private/{user_id}/notifications?only_unread={bool}&later_than={number}`
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}/notifications" method="GET">

<response type="200">

<sample>
{
    "code" : 0,
    "info" : "Success",
    "notifications" : [
        {
            "notification_id" : 1,
            "sender_id" : 1,
            "content" : "{\"type\": \"user.friend.request\",\"status\": \"make request\",\"user_id\": 1,\"is_approved\": True,}",
            "create_time" : 1712025307.24112,
            "is_read" : false
        },
        ...
    ]
}
</sample>

</response>

</api-endpoint>