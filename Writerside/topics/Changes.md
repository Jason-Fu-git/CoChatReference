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