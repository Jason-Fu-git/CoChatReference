# Changes

<!-- Maintain a changelog or release notes section
to inform users about updates, changes, and new features in different API versions -->

## March 16, 2024

api文档初始化，编写了[Git规范](Git-specification.md)和[数据库规范](Database-specification.md).

## March 17, 2024

api reference的 [User部分](Create-user.md) 的创建、登录、更新数据、删除编写完毕

## March 19, 2024

- api reference User部分的 Chat，Friend管理完成，Chat, Message主要api接口编写完成
- 修改了数据库规范，删除了Inbox，将已读列表追加到message表中

## March 30, 2024

新建websocket建立规范、好友请求规范

## April 1, 2024

新建`/api/user/<user_id>`url下对`GET`方法的处理，可通过用户ID获取用户详细信息。

## April 2, 2024

新建`Notification`数据库即`Notification`配套HTTP请求规范。

## April 6, 2024

修改了部分`Chat` 接口规范

## April 9, 2024

实现头像传输

- 用户注册/信息更新的请求体格式改为`multipart/form-data`
- 获取头像参见[这里](Get-a-user-s-avatar.md)

GET 方法 API 规范更改

- [搜索用户](Search-for-users.md)
- [通知列表获取](Get-notification-list.md)
- [消息列表获取](Get-message-list.md)
- [聊天成员获取](Get-message-list.md)

Chat 部分 Websocket 和 Notification 规范

## April 16, 2024

- 将通知的各项操作整合到url `/api/user/private/{user_id}/notification/{notification_id}`
- 新建获取[chat detail](Get-chat-detail.md)的接口
- 修改Message相关接口

## April 23, 2024

- 新建 Websocket 接口 [Message](Message.md)
- 新增好友分组功能，参见
    - [Get the user's friend list](Get-the-user-s-friends-list.md)
    - [Make / Delete a friend](Make-delete-a-friend.md)

## May 2, 2024

- 新增[聊天历史记录搜索](Get-message-list.md)功能

## May 3, 2024

- 新增群公告功能，修改以下原有接口
  - [发送消息](Post-a-message.md)
  - [获取历史消息](Get-message-list.md)

## May 7, 2024

- 新增验证码功能
  - [发送验证码](Send-verification-code.md)
  - [更新用户信息](Update-user.md)

## May 14, 2024

- 更新数据库设计文档。
- 新增字段`user_phone`
- 修改[用户信息更新规则](Update-user.md)