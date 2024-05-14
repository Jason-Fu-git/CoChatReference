# Database specification

数据库规范

## `User`

| 字段名                 | 字段类型           | 描述       | 备注                                                          |
|---------------------|----------------|----------|-------------------------------------------------------------|
| `user_id`           | `BigAutoField` | 用户id     | 主键                                                          |
| `user_name`         | `CharField`    | 用户名      | `maxLength=50`, `unique=True`                               |
| `password`          | `CharField`    | 加密后的密码   | `maxLength=50`                                              |
| `description`       | `CharField`    | 用户描述     | `max_length=MAX_DESCRIPTION_LENGTH, default="这个人很懒，什么都没留下"` |
| `user_icon`         | `ImageField`   | 头像       | `blank=True`，后端自动压缩                                         |
| `register_time`     | `FloatField`   | 用户注册时间   | 时间戳                                                         |
| `login_time`        | `FloatField`   | 用户登录时间   | 时间戳                                                         |
| `modify_time`       | `FloatField`   | 用户信息修改时间 | 时间戳                                                         |
| `user_email`        | `CharField`    | 邮箱       | `maxLength=100`, `blank=True`（允许为空）                         |
| `jwt_token_salt`    | `BinaryField`  | JWT令牌的盐  | 每个用户，每次登录都会创建新的盐                                            |
| `verification_code` | `CharField`    | 六位验证码    | 修改密码时后端随机生成                                                 |

## `Message`

| 字段名                   | 字段类型              | 描述                                                      | 备注                         |
|-----------------------|-------------------|---------------------------------------------------------|----------------------------|
| `msg_id`              | `BigAutoField`    | 消息id                                                    | 主键                         |
| `sender`              | `ForeignKey`      | 消息发送者                                                   | `on_delete=models.CASCADE` |
| `chat`                | `ForeignKey`      | 消息所属聊天                                                  | `on_delete=models.CASCADE` |
| `msg_text`            | `CharField`       | `message_type`  = “text” 时，为消息文字；其余情况，为文件名（文件未加载成功时显示）。 | `maxLength=1000`           |
| `msg_file`            | `FileField`       | 文件（可为空）                                                 | `blank=True`               |
| `msg_type`            | `CharField`       | “text” \| “image” \| “audio” \| “video” \| “others”     | `maxLength=10`             |
| `create_time`         | `FloatField`      | 该消息的发送时间                                                | 时间戳                        |
| `update_time`         | `FloatField`      | 该消息的已读/未读列表更新时间                                         | 时间戳                        |
| `read_users`          | `ManyToManyField` | 已读该消息的用户列表                                              |                            |
| `unable_to_see_users` | `ManyToManyField` | 不可视该消息的用户列表                                             |                            |
| `reply_to`            | `IntegerField`    | 回复某消息（id）                                               | default=-1                 |
| `is_system`           | `BooleanField`    | 是否为系统消息                                                 | default=False              |

## `Chat`

| 字段名           | 字段类型           | 描述    | 备注             |
|---------------|----------------|-------|----------------|
| `chat_id`     | `BigAutoField` | 聊天id  | 主键             |
| `chat_name`   | `CharField`    | 群聊名称  | `maxLength=50` |
| `create_time` | `FloatField`   | 创建时间  | 时间戳            |
| `is_private`  | `BooleanField` | 是否为私聊 |                |

## `Friendship`

| 字段名           | 字段类型           | 描述     | 备注                                                                 |
|---------------|----------------|--------|--------------------------------------------------------------------|
| `user`        | `ForeignKey`   | 用户（自己） | `on_delete=models.CASCADE`<br />`related_name='user_friendship'`   |
| `friend`      | `ForeignKey`   | 用户（好友） | `on_delete=models.CASCADE`<br />`related_name='friend_friendship'` |
| `update_time` | `FloatField`   | 关系更新时间 | 时间戳                                                                |
| `group`       | `CharField`    | 好友分组名称 | `maxLength=50`<br />`default='ungrouped'`                          |
| `is_approved` | `BooleanField` | 是否同意请求 | 只有在双方都同意时，该字段才为true                                                |

注：每一个好友关系对应数据库中两条数据，即（A, B）,(B, A)

## `Membership`

| 字段名           | 字段类型           | 描述       | 备注                                                               |
|---------------|----------------|----------|------------------------------------------------------------------|
| `user`        | `ForeignKey`   | 用户       | `on_delete=models.CASCADE`<br />`related_name='user_membership'` |
| `chat`        | `ForeignKey`   | 聊天       | `on_delete=models.CASCADE`<br />`related_name='user_membership'` |
| `privilege`   | `CharField`    | 权限       | 成员权限，包括群主(owner)、成员(member)、管理员(admin) 三选一                       |
| `update_time` | `FloatField`   | 关系更新时间   | 时间戳                                                              |
| `is_approved` | `BooleanField` | 是否同意加入聊天 | 默认False                                                          |
| `is_system`   | `BooleanField` | 是否为系统通知  | 默认False                                                          |                                                          

## `Notification`

| 字段名               | 字段类型           | 描述     | 备注                                                                 |
|-------------------|----------------|--------|--------------------------------------------------------------------|
| `notification_id` | `BigAutoField` | 通知id   | `primary_key=True`                                                 |
| `receiver`        | `ForeignKey`   | 通知接受者  | ` on_delete=models.CASCADE, related_name='receiver_notifications'` |
| `sender`          | `ForeignKey`   | 通知发送者  | ` on_delete=models.CASCADE, related_name='sender_notifications'`   |
| `content`         | `CharField`    | 通知具体内容 | `max_length=1000`                                                  |
| `create_time`     | `FloatField`   | 通知创建时间 | 时间戳                                                                |
| `is_read`         | `BooleanField` | 是否已读   | `default=False`                                                    |

## `Client`

| 字段名            | 字段类型           | 描述                      | 备注                             |
|----------------|----------------|-------------------------|--------------------------------|
| `channel_name` | `CharField`    | 该channel的channel_name属性 | `max_length=1024, unique=True` |
| `user_id`      | `IntegerField` | 该channel所属user的id       | `unique=True`                  |
| `create_time`  | `FloatField`   | 该channel建立的时间           | `default=get_timestamp`        |