# Create user

<!--Specify request and response samples manually. 
You can add the sample inside the <sample> element or include it from a file using the 'src' attribute.-->

<api-endpoint openapi-path="./../cotalk.yaml" endpoint="/api/user/register" method="post">



<response type="200">

<sample>
    {
        "code" : 0,
        "info" : "Success",
        "token" : "***.***.***",
        "user_id" : 1,
        "user_name" : "Plato",
        "user_email" : "Plato@163.com",
        "description": "A great philosopher",
        "register_time" : 1712025307.24112,
        "avatar" : "{FILE BINARY}"
    }
</sample>

</response>

</api-endpoint>
