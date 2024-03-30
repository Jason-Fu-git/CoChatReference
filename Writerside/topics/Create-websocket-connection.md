# Create websocket connection

建立与后端websocket的链接

> 当`token`错误或已有同id用户建立链接时，`connect`会被拒绝。
> 
{style="warning"}

### url

`/ws/?Authorization={JWT_TOKEN}&user_id={USER_ID}`