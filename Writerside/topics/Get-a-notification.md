# Get a notification

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/{user_id}/notification/{notification_id}" method="get">

<response type="200">

<sample>
{
    "code" : 0,
    "info" : "Success",
    "notification_id" : 1,
    "sender_id" : 1,
    "content" : "{\"type\": \"user.friend.request\",\"status\": \"make request\",\"user_id\": 1,\"is_approved\": True,}",
    "create_time" : 1712025307.24112,
    "is_read" : false
}
</sample>

</response>

</api-endpoint>