# GitHub Pages 免费资源订阅中心

本模板适用于公开托管你拥有权利或已经获得传播授权的直播列表、视频配置以及小说书源配置。**不包含可播放频道、影视站点或小说采集规则。**

## 1. 创建仓库

1. 打开 https://github.com/new
2. 仓库名称使用 `my-media-sources`，选择 `Public`，创建仓库。
3. 将本模板 ZIP 解压，将**解压后的文件**（不是 ZIP 文件）放到仓库根目录。GitHub 仓库页面选择 `Add file` → `Upload files`，提交至 `main` 分支。
4. `Settings` → `Pages` → `Build and deployment` → `Source: Deploy from a branch` → `Branch: main` → `Folder: /(root)` → `Save`。
5. 访问 `https://你的GitHub用户名.github.io/my-media-sources/`。

## 2. 必需修改

编辑 `tvbox.json`，将其中 `USERNAME` 替换成你的 GitHub 用户名。如果仓库不叫 `my-media-sources`，同时修改 URL 的仓库名称部分。

## 3. 入口地址

- 首页：`https://你的用户名.github.io/my-media-sources/`
- 直播 M3U：`https://你的用户名.github.io/my-media-sources/live.m3u`
- TVBox：`https://你的用户名.github.io/my-media-sources/tvbox.json`
- 视频索引：`https://你的用户名.github.io/my-media-sources/videos.json`
- 小说索引：`https://你的用户名.github.io/my-media-sources/books.json`
- 阅读书源：`https://你的用户名.github.io/my-media-sources/bookSource.json`

## 4. 格式说明

- `live.m3u`：初始为空，仅保留 M3U 标头。请将注释示例改为获得合法授权的可用流地址，并在播放器中测试。
- `tvbox.json`：TVBox 风格配置，`sites` 为空。不同 TVBox 衍生客户端的 `lives` 对 M3U 的解析可能不同，请实际测试。
- `videos.json`：自定义 JSON 清单，不等同于 TVBox 可识别的影视采集源。
- `books.json`：自定义小说索引，不等同于「阅读」App 的书源。
- `bookSource.json`：「阅读」App 格式的空数组。有效书源需要完整的 `bookSourceUrl`、`bookSourceName` 和搜索、详情、目录及正文规则；这些规则依具体合法内容站点而定。

## 5. 限制与注意事项

- GitHub Pages 只能托管静态文件，不会运行 Python/Node.js 后台抓取器、数据库、转码器或实时推流服务器。
- GitHub Pages 是公共访问地址，不要将 Cookie、账号密码、API Key、私人数据写入公开仓库。
- 已有直播流若本身存在跨域、鉴权、防盗链、地域限制或 HTTPS 混合内容限制，Pages 无法自动消除。
- GitHub Pages 官方公布站点最大 1 GB、每月约 100 GB 软带宽限制，并可能进行速率限制。

官方文档：
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
