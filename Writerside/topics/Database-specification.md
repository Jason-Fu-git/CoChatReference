# Database specification

数据库规范

## `User`

| 字段名             | 字段类型              | 描述    | 备注                                  |
|-----------------|-------------------|-------|-------------------------------------|
| `user_id`       | `BigAutoField`    |       | 主键                                  |
| `user_name`     | `CharField`       |       | `maxLength=50`, `unique=True`       |
| `password`      | `CharField`       | 加密后的密码 | `maxLength=50`                      |
| `register_time` | `FloatField`      |       | 时间戳                                 |
| `login_time`    | `FloatField`      |       | 时间戳                                 |
| `user_email`    | `CharField`       | 邮箱    | `maxLength=100`, `blank=True`（允许为空） |
| `user_icon`     | `ImageField`      | 头像    | `.png`文件, `blank=True`              |
|                 |                |              |                                           |

### 成员方法

- `get_memberships`
- `get_friends`
- `get_chats`



## `Message`

| 字段名           | 字段类型           | 描述                                                      | 备注                                       |
|---------------|----------------|---------------------------------------------------------| ------------------------------------------ |
| `msg_id`      | `BigAutoField` |                                                         | 主键                                       |
| `sender`      | `ForeignKey` | 消息发送者                                                   | `on_delete=models.CASCADE` |
| `chat`        | `ForeignKey` | 消息所属聊天                                                  | `on_delete=models.CASCADE`                 |
| `msg_text`    | `CharField`    | `message_type`  = “text” 时，为消息文字；其余情况，为文件名（文件未加载成功时显示）。 | `maxLength=1000`                           |
| `msg_file`    | `FileField`    | 文件（可为空）                                                 | `blank=True`                               |
| `msg_type`    | `CharField`    | “text” \| “image” \| “audio” \| “video” \| “others”     | `maxLength=10`                             |
| `create_time` | `FloatField`   |                                                         | 时间戳                                     |
| `update_time` | `FloatField` | 该消息的已读/未读列表更新时间 | 时间戳 |
| `read_users`  | `ManyToManyField` | 已读该消息的用户列表 |  |





## `Chat`

| 字段名        | 字段类型       | 描述       | 备注           |
| ------------- | -------------- | ---------- | -------------- |
| `chat_id`     | `BigAutoField` |            | 主键           |
| `chat_name`   | `CharField`    | 群聊名称   | `maxLength=50` |
| `create_time` | `FloatField`   | 创建时间   | 时间戳         |
| `is_private`  | `BooleanField` | 是否为私聊 |                |

### 成员方法

- `get_memberships`
- `get_members`
- `get_owner`
- `get_admins`



## `Friendship`

| 字段名        | 字段类型     | 描述 | 备注                                                         |
| ------------- | ------------ | ---- | ------------------------------------------------------------ |
| `user`        | `ForeignKey` |      | `on_delete=models.CASCADE`<br />`related_name='user_friendship'` |
| `friend`      | `ForeignKey` |      | `on_delete=models.CASCADE`<br />`related_name='friend_friendship'` |
| `update_time` | `FloatFeild` |      | 时间戳                                                       |
|               |              |      |                                                              |

注：每一个好友关系对应数据库中两条数据，即（A, B）,(B, A)



## `Membership`

| 字段名        | 字段类型     | 描述 | 备注                                                         |
| ------------- | ------------ | ---- | ------------------------------------------------------------ |
| `user`        | `ForeignKey` |      | `on_delete=models.CASCADE`<br />`related_name='user_membership'` |
| `chat`        | `ForeignKey` |      | `on_delete=models.CASCADE`<br />`related_name='user_membership'` |
| `privilege`   | `CharField`  |      | 成员权限，包括群主(owner)、成员(member)、管理员(admin) 三选一 |
| `update_time` | `FloatField` |      | 时间戳                                                       |