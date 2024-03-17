# Create user

<!--Specify request and response samples manually. 
You can add the sample inside the <sample> element or include it from a file using the 'src' attribute.-->

<api-endpoint openapi-path="./../cochat.yaml" endpoint="/api/user/register" method="post">

<request>

<sample>
    {
        "user_name" : "Plato",
        "password" : "123456",
        "user_email" : "Plato@163.com",
        "avatar" : "{FILE BINARY}"
    }
</sample>

</request>

<response type="200">

<sample>
    {
        "code" : 0,
        "info" : "Success",
        "token" : "***.***.***"
        "user_name" : "Plato",
        "password" : "123456",
        "user_email" : "Plato@163.com",
        "avatar" : "{FILE BINARY}"
    }
</sample>

</response>

</api-endpoint>
