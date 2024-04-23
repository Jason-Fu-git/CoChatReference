# Withdraw / Delete a message

> 撤回消息后将自动创建系统通知 `{USER_NAME} withdrawn a message`
> 
> 并通过`websocket`通知聊天中的所有用户
> 
{style="note"}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/message/{messageid}/management" method="DELETE">

</api-endpoint>