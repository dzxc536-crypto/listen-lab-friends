# 听练 · 好友分享版

免费、非商业的个人英语听力练习工具。识别、对齐和英译中在使用者浏览器中运行；没有收费推理 API，不上传个人音频。

网站地址：https://dzxc536-crypto.github.io/listen-lab-friends/

## 使用

打开网站，按首次使用提示保存模型（完整资源约 300 MB）。可先试合成演示，再导入自己的英语音频。材料和进度保存在本设备浏览器中，请定期导出 `.listen` 备份。

保留句末暂停、0.1–2.5 倍保调、字幕遮挡、双语字幕、字幕字号与紧凑度、音频管理、批量 ZIP 导出功能。手机布局经过桌面浏览器视口检查，手机实际识别性能及后台行为仍需实机验证。

## 部署和复现

`source-bundle.zip` 内的 `site/` 保存可编辑网页源文件；解压即可修改。`scripts/restore-resources.py` 从 `resources.json` 指定的原始来源恢复固定版本资源，并对全部站点文件核对 SHA-256。GitHub Pages 的免费公开仓库构建发布完整站点，用户从本站下载模型，运行时不依赖模型来源网站。

先解压 `source-bundle.zip`，然后本地恢复：`python scripts/restore-resources.py`。预览：`python -m http.server 8080 --bind 127.0.0.1 --directory site`，然后打开 `http://localhost:8080`。

采用 GitHub Pages 免费公开仓库和标准托管 runner，不使用付费 runner、服务器、域名、推理 API 或数据库。Pages 当前有站点容量与带宽限制，不承诺无限流量或永久免费；遵守其非商业用途要求。

模型、运行库的原始来源和许可证见 `site/THIRD_PARTY.md`、`resources.json` 和相关随附许可。本仓库的公开可见性不改变第三方资源的许可。
