# 维护这份个人主页

这是 `type_云` 的 GitHub Profile README 仓库。GitHub 会把 `main` 分支根目录的 `README.md` 展示在个人账号主页。

## 修改内容

- `README.md`：个人简介、项目导航与精选项目说明。
- `assets/profile-banner.svg`：个人页头图；优先改本地资源，不依赖会过期的第三方横幅服务。
- 只写已经公开、可核实的信息；不要加入未经确认的联系方式、经历或社交账号。
- 精选项目固定为 `Doodle`、`conchbase`、`pagurus`，并与个人页 Pinned repositories 保持一致。
- 项目链接优先指向本账号下的公开仓库；动态状态优先使用 GitHub 原生 CI 徽章和仓库内页面，不写死仓库数和版本号。
- 图片和徽章应提供 `alt` 文本，并尽量长期可用；不要加入需要第三方图片代理的动态徽章，以免加载失败时只剩蓝链。

## 提交规范

1. 从 `main` 创建短命分支。
2. 使用简洁的中文提交信息，例如：`docs: 更新精选项目`。
3. 提交 Pull Request 后本地预览 Markdown，确认链接、表格与图片没有破坏排版。
4. 合并后删除分支。

## 自动检查

`.github/workflows/check-profile.yml` 会在 `main` 的推送、Pull Request 和每月定时任务中检查：

- README 中使用的 GitHub 原生图片地址是否返回成功；
- README 中的本地图片是否存在，且不包含会暴露成蓝链的失效链接；
- 文件是否保留 UTF-8 编码与结尾换行。

如果第三方图片服务临时不可用，可以等重试结果，也可以将对应图片替换为稳定的本地或官方来源。
