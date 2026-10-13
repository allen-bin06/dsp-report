# GROWNSY DSP 报告网站

这是可直接部署到 GitHub Pages 的纯静态网站，**无须安装依赖或构建**。

## 初次发布（建议仓库：`grownsy-dsp-report`）

1. 在 GitHub 创建 **Public** 仓库 `grownsy-dsp-report`（建议不勾选初始化 README）。
2. 下载本网站 ZIP，**解压**。把解压后的所有内容放到该仓库的根目录（`index.html` 必须就在仓库根目录，不要再嵌套一层文件夹）。可用 GitHub Desktop 提交推送，或 GitHub 网页上传文件。
3. 到仓库 **Settings → Pages → Build and deployment**，选择 **Source: Deploy from a branch**、**Branch: main**、**Folder: /(root)**，点击 **Save**。
4. 访问 `https://<你的GitHub用户名>.github.io/grownsy-dsp-report/`。

### 固定网页地址

- 首页（版本中心）：`https://<用户名>.github.io/grownsy-dsp-report/`
- 始终最新：`https://<用户名>.github.io/grownsy-dsp-report/latest/`
- 历史版本：`https://<用户名>.github.io/grownsy-dsp-report/versions/v1.html` 等

## 以后新增 V6 的流程

1. 将当前待发布的**新 HTML 报告**保存为 `versions/v6.html`，不要覆盖 `versions/v5.html`。
2. 同样内容覆盖 `latest/index.html`。
3. 更新 `versions.js`：在数组顶部新增 `v6` 记录，路径 `versions/v6.html`，`current:true`；将原 `v5` 的 `current:true` 删除。
4. 在 `CHANGELOG.md` 记录修改摘要。
5. 提交（Commit）并推送（Push）至 GitHub `main` 分支；Pages 自动更新。

网站首页通过 `versions.js` 显示可切换的版本；直接打开 `latest/` 始终是最新版。

## 当前版本

- V1 2026-10-08：DSP 分析基础版
- V2 2026-10-10：AMC 前后对比版
- V3 2026-10-12：品牌搜索对照框架
- V4 2026-10-12：Google Trends 官方联网嵌入
- V5 2026-10-12：每日 ACOS 图内标注（最新）

## 公开发布须知

**GitHub Pages 公开可访问**。报告包含真实广告花费、销售额、账户或商品信息时，请先确认有权公开。删除网页源码中的敏感数据后再上传；对 GitHub 的历史提交也要谨慎处理，已公开的旧版本可能被缓存或复制。此示例未做脱敏处理。

本仓库仅有静态 HTML；`Google Trends` 依赖联网与对应服务可访问，`Amazon SQP` 不会因上传网页而获得 Seller Central 数据权限。请勿在静态 HTML 中写入 SP-API token、密码或任何私密密钥。