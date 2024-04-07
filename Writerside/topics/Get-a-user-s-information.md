# Get a user&apos;s information

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}" method="GET">

<response type="200">
<sample>
{   
    "user_id" : 1,
    "user_name" : "Plato",
    "user_email" : "Plato@Athens.com",
    "description" : "A great philosopher",
    "register_time" : 1712025307.24112,
    "avatar" : {FILE_BINARY}
}
</sample>

</response>

</api-endpoint>