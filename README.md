# 789Bingo · APP下载奖励活动

前台原型、后台原型与 PRD 需求文档（v1.0）的静态站点，可直接部署到 GitHub Pages。

## 目录结构

```
index.html            入口页：左侧目录 + 右侧内容区
pages/
  frontend.dc.html    前台交互原型（H5 + APP + 演示控制台）
  sidebar-entry.dc.html  侧边菜单入口三态
  popups.html         领取弹窗三态（整合页）
  claim-anim.html     领取动效：Loading / 成功 / 失败（整合页）
  popup-*.dc.html、claim-*.dc.html  整合页引用的单张状态稿
  admin.dc.html       后台交互原型（活动中心 › APP下载奖励活动）
  prd.html            PRD 需求文档（单页，含章节锚点）
  checklist.html      功能自查清单（设计 / 开发 / 测试，可勾选，查看PRD 可定位并荧光标出相关内容）
  support.js          原型运行时（含 React，无需联网加载）
assets/               原型使用的图片素材
.nojekyll             关闭 Jekyll 处理
```

## 部署到 GitHub Pages

1. 将压缩包解压到仓库根目录（或任意子目录），提交并推送。
2. 仓库 Settings › Pages › Build and deployment：Source 选择 “Deploy from a branch”，Branch 选择对应分支与目录（`/ (root)` 或所在子目录）。
3. 等待部署完成后访问 `https://<用户名>.github.io/<仓库名>/`。

## 本地预览

原型页面需要通过 HTTP 访问（不要直接双击打开文件）：

```bash
python3 -m http.server 8000
# 浏览器访问 http://localhost:8000/
```

## 说明

- 视觉效果仅以 UI 设计稿为准，原型仅用于说明页面内容、交互流程与业务逻辑。
- 支持通过地址直接定位，例如 `index.html#prd/s9-3` 打开 PRD 第 9.3 节，`index.html#ad/admin` 打开后台原型。
