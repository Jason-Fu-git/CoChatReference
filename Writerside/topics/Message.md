# Message

消息相关

## 后端 -> 前端

### 内容

> 撤回消息后，该消息即被销毁，`msg_id` 随即无效！
> 
{style="warning"}

<tabs>
<tab title="发送消息">
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"chat.message"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <p>"send message"</p>
    </def>
    <def title="user_id">
        <emphasis>required</emphasis>  integer
        <p>发送者的user_id</p>
    </def>
    <def title="chat_id">
        <emphasis>required</emphasis>  integer
        <p>所属聊天id</p>
    </def>
    <def title="msg_id">
        <emphasis>required</emphasis>  integer
        <p>所发消息的id</p>
    </def>
    <def title="update_time">
        <emphasis>required</emphasis>  float
        <p>所发消息的更新时间</p>
    </def>
</deflist>
样例

<code-block lang="json">
{
     'type': 'chat.message',
     'status': 'send message',
     'user_id': 1,
     'chat_id': 1,
     'msg_id': 1,
     'update_time': 1713844846.08072
}
</code-block>
</tab>

<tab title="撤回消息">
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"chat.message"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <p>"withdraw message"</p>
    </def>
    <def title="user_id">
        <emphasis>required</emphasis>  integer
        <p>撤回者的user_id</p>
    </def>
    <def title="chat_id">
        <emphasis>required</emphasis>  integer
        <p>所属聊天id</p>
    </def>
    <def title="msg_id">
        <emphasis>required</emphasis>  integer
        <p>所撤回消息的id</p>
    </def>
    <def title="update_time">
        <emphasis>required</emphasis>  float
        <p>所撤回消息的撤回时间</p>
    </def>
</deflist>
样例

<code-block lang="json">
{
     'type': 'chat.message',
     'status': 'withdraw message',
     'user_id': 1,
     'chat_id': 1,
     'msg_id': 1,
     'update_time': 1713844846.08072
}
</code-block>
</tab>
<tab title="消息已读">
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"chat.message"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <p>"read message"</p>
    </def>
    <def title="user_id">
        <emphasis>required</emphasis>  integer
        <p>已读者的user_id</p>
    </def>
    <def title="chat_id">
        <emphasis>required</emphasis>  integer
        <p>所属聊天id</p>
    </def>
    <def title="msg_id">
        <emphasis>required</emphasis>  integer
        <p>所标记消息的id</p>
    </def>
    <def title="update_time">
        <emphasis>required</emphasis>  float
        <p>所标记消息的更新时间</p>
    </def>
</deflist>
样例

<code-block lang="json">
{
     'type': 'chat.message',
     'status': 'read message',
     'user_id': 1,
     'chat_id': 1,
     'msg_id': 1,
     'update_time': 1713844846.08072
}
</code-block>
</tab>
</tabs>

