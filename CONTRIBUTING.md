# 维护这份个人主页

这是 `flowli（type_云）` 的 GitHub Profile README 仓库。GitHub 会把 `main` 分支根目录的 `README.md` 展示在个人账号主页。

## 修改内容

- `README.md`：一句事实型简介、博客入口与精选项目说明。
- `assets/profile-banner.svg`：个人页头图；优先改本地资源，不依赖会过期的第三方横幅服务。
- 只写已经公开、可核实的信息；不要加入未经确认的联系方式、经历或社交账号。
- 主页重点展示 `Doodle`、`proofpack-cli`、`LanZe`；`conchbase` 与 `pagurus` 放在次要维护说明中，不与重点条目争视觉层级。
- Pinned repositories 展示 `Doodle`、`proofpack-cli`、`LanZe`、`conchbase`、`pagurus`，与 README 的项目范围保持一致；私有仓库、fork、归档仓库和公开证明不足的实验项目不加入展示。
- 项目链接优先指向本账号下的公开仓库；动态状态优先使用 GitHub 原生 CI 徽章和仓库内页面，不写死仓库数和版本号。
- 头图、正文、Bio 统一使用 `flowli（type_云）`；头像和账号显示名由 GitHub 个人资料设置维护。
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
