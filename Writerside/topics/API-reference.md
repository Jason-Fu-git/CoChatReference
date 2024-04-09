# API Reference

> 文件/头像怎么传还没想好，先空着
>
{style="warning"}

后端服务器的API Reference

## 用户

- [创建用户](Create-user.md)
- [登录用户](Logs-user-into-the-system.md)
- [更新用户信息](Update-user.md)
- [删除用户](Delete-user.md)
- [获取用户详细信息](Get-a-user-s-information.md)
- [获取用户头像](Get-a-user-s-avatar.md)


- [好友列表](Get-the-user-s-friends-list.md)
- [用户搜索](Search-for-users.md)
- [添加/删除好友](Make-delete-a-friend.md)


- [聊天列表](Get-the-user-s-chat-list.md)
- [退出群聊](Exit-chat.md)


- [获取通知列表](Get-notification-list.md)
- [获取单个通知内容](Get-a-notification.md)
- [删除通知](Delete-a-notification.md)
- [通知标为已读](Mark-as-read.md)


## 聊天

- [创建聊天](Create-a-chat.md)
- [获取聊天内消息](Get-message-list.md)
- [获取聊天成员列表](Get-member-list.md)
- [修改成员权限](Change-member-privilege.md)
- [邀请加入/踢出](Invite-kick-a-member.md)

## 消息

- [获取某消息的详细信息](Get-a-message.md)
- [撤回消息](Delete-a-message.md)
- [发送消息](Post-a-message.md)
- [标记已读](Read-a-message.md)

## Websocket

- [Websocket](Websocket.md)

## Security

使用`jwt token`，其`payload`为 `user_id`

<!-- Use the <api-doc> element to generate the documentation for a few specific endpoints and methods with the same tag 
or <api-endpoint> element to generate the documentation for a specific endpoint and method.
See the subsections here for specific examples. -->