# Friend request

前端到后端（或后端到前端）的friend request通知发送

## 前端 -> 后端

> 此接口有三种调用时机：
> - A 向 B 发出添加好友的申请
> - B 收到了 A 的申请，并做出回应，此时`approve`字段起作用
> - A 和 B 已经是朋友，但是 B 想把 A 删掉，此时`approve`字段必须为`false`
>
{style="note"}

考虑到此任务与后端HTTP请求高度绑定，通知部分由后端接管，前端只需关心接收工作。


## 后端 -> 前端

### 内容

属性
<deflist collapsible="false">
    <def title="type">
        <emphasis>required</emphasis> string
        <p>"user.friend.request"</p>
    </def>
    <def title="status">
        <emphasis>required</emphasis> string
        <p>"received"</p>
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
{
     'type': 'user.friend.request',
     'status': 'received',
     'user_id': 1,
     'is_approved': True,
}
</code-block>