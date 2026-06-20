# biubiubiu 后台任务链接部署

把 `tasks.json` 放在仓库根目录即可。

APK 读取顺序：

1. Gitee 主仓库：`https://gitee.com/xth_320/biubiubiu/raw/master/tasks.json`
2. Gitee main 分支兜底：`https://gitee.com/xth_320/biubiubiu/raw/main/tasks.json`
3. GitHub 备用仓库：`https://raw.githubusercontent.com/deerinwild/biubiubiu/main/tasks.json`
4. GitHub master 分支兜底：`https://raw.githubusercontent.com/deerinwild/biubiubiu/master/tasks.json`

建议两个仓库都放同一份 `tasks.json`。Gitee 正常时 APK 不会读取 GitHub；Gitee 出错时才读取 GitHub。

字段说明：

- `version`：配置文件版本。
- `updatedAt`：后台更新时间，显示在 APK 首页。
- `message`：给用户看的提示语。
- `monitorEndpoint`：Render 监控接口地址，格式类似 `https://xxx.onrender.com/api/ping`。
- `tasks`：管理员发布的视频链接列表。
- `platform`：目前只填 `tx` 或 `iqy`。
- `url`：必须尽量使用桌面版视频链接，例如腾讯 `https://v.qq.com/...`，爱奇艺 `https://www.iqiyi.com/...`。
- `enabled`：设置为 `false` 时，APK 不显示该链接。
