# biubiubiu 管理员任务仓库

在 Gitee 和 GitHub 两个任务仓库的根目录放置 `tasks.json`。

APK 读取顺序：

1. `https://gitee.com/xth_320/biubiubiu/raw/master/tasks.json`
2. `https://gitee.com/xth_320/biubiubiu/raw/main/tasks.json`
3. `https://raw.githubusercontent.com/deerinwild/biubiubiu/main/tasks.json`
4. `https://raw.githubusercontent.com/deerinwild/biubiubiu/master/tasks.json`

字段说明：

- `monitorEndpoint`：Render 上报接口。
- `prelogin.tx`：腾讯视频预登录页面。
- `prelogin.iqy`：爱奇艺预登录页面。
- `tasks[].platform`：统一使用 `tx` 或 `iqy`。
- `tasks[].url`：管理员发布的具体播放页链接。
