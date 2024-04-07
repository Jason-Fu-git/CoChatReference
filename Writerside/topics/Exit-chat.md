# Exit chat

> 私聊不能退出，除非终止好友关系，此时自动删除私聊
> 
{style="warning"}

> 如果该成员退出聊天后，聊天中一个人都没有，则该聊天自动删除。
>
> 群主退出后，群主权交给管理员/成员
>
{style='warning'}

<api-endpoint openapi-path="../cotalk.yaml" endpoint="/api/user/private/{user_id}/chats" method="DELETE"></api-endpoint>