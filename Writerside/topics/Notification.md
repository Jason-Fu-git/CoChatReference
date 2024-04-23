# Notification

用户离线时，系统向该用户所发的通知。

## 1. Friend request

将本应发给用户Websocket的内容存到notification中。格式为`JSON`字符串。

属性
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"user.friend.request"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <list>
        <li>
        "make request" - B收到了A发出的好友请求
        </li>
        <li>
        "accept request" - A收到了B的同意通知
        </li>
        <li>
        "reject request" - A收到了B的拒绝通知
        </li>
        <li>
        "delete" - A和B已经是朋友，A决定删掉B，B收到该通知
        </li>
        </list>
    </def>
    <def title="user_id">
        <emphasis>required</emphasis>  integer
        <p>对方的user_id</p>
    </def>
    <def title="is_approved">
        <emphasis>required</emphasis>  boolean | string
        <p>是否同意请求</p>
    </def>
</deflist>
样例

<code-block lang="json">
"{
     \"type\": \"user.friend.request\",
     \"status\": \"make request\",
     \"user_id\": 1,
     \"is_approved\": True,
}"
</code-block>


## 2. Chat management

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