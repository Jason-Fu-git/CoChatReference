# Chat management

聊天管理

## 后端 -> 前端

### 内容

属性
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"chat.management"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <list>
        <li>
        "kicked out" - 用户被踢出
        </li>
        <li>
        "change to {NEW PRIVILEGE}" - 用户权限被更改，其中`NEW PRIVILEGE`的取值有`member`,`admin`,`owner`
        </li>
        <li>
        "make invitation" - 加入群聊的邀请
        </li>
        </list>
    </def>
    <def title="user_id">
        <emphasis>required</emphasis>  integer
        <p>对方的user_id</p>
    </def>
    <def title="chat_id">
        <emphasis>required</emphasis>  integer
        <p>所属群聊id</p>
    </def>
    <def title="is_approved">
        <emphasis>required</emphasis>  boolean | string
        <p>是否同意请求</p>
    </def>
</deflist>
样例

<code-block lang="json">
{
     'type': 'chat.management',
     'status': 'change to admin',
     'user_id': 1,
     'chat_id': 1,
     'is_approved': True,
}
</code-block>