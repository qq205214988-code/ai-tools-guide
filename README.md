# 我的 AI 工具库

这是一个可以发布到 GitHub Pages 的静态网站。

发布后你会得到一个长期网址，例如：

```text
https://你的GitHub用户名.github.io/ai-tools-guide/
```

以后你想更新工具，不需要改网页样式，只改 `tools.json`。

新版页面已经支持：

- 搜索工具名、用途、标签和自己的备注
- 按分类筛选
- 按标签、价格、状态筛选
- 在浏览器本地收藏常用工具
- 点击工具查看详情
- 复制每个工具的新手提示词
- 展示推荐指数、替代工具和自己的试用记录

## 文件说明

- `index.html`：网站页面，不常改。
- `tools.json`：工具数据，常用来新增、删除、修改工具。

## 推荐发布方式：GitHub Pages

1. 登录 GitHub。
2. 新建一个仓库，名字建议用：

```text
ai-tools-guide
```

3. 把这个文件夹里的 `index.html` 和 `tools.json` 上传到仓库根目录。
4. 打开仓库的 `Settings`。
5. 左侧找到 `Pages`。
6. `Build and deployment` 选择：

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

7. 保存后等待 1 到 3 分钟。
8. GitHub 会给你一个网址，通常是：

```text
https://你的GitHub用户名.github.io/ai-tools-guide/
```

## 以后怎么新增一个工具

打开 `tools.json`，复制任意一段工具资料，粘贴到列表里，然后修改字段。

示例：

```json
{
  "name": "工具名称",
  "abbr": "缩写",
  "category": "分类",
  "tag": "热门/好用/冷门好用/试用中",
  "url": "https://官网地址.com/",
  "color": "#2563EB",
  "what": "它能帮我做什么",
  "best": "适合什么人或什么场景",
  "difference": "和同类相比有什么区别",
  "pricing": "免费+付费",
  "status": "试用中",
  "rating": 4,
  "tags": ["中文好用", "适合小白"],
  "prompt": "这个工具最好用的提示词模板",
  "alternatives": ["替代工具1", "替代工具2"],
  "myNote": "我自己的试用感受"
}
```

注意：每一段工具资料之间要用英文逗号 `,` 隔开。

## 字段怎么填

- `pricing`：价格印象，例如 `免费`、`免费+付费`、`付费为主`。
- `status`：你的使用状态，例如 `常用`、`试用中`、`待试用`、`已踩坑`。
- `rating`：推荐指数，填写 1 到 5。
- `tags`：筛选标签，可以写多个，例如 `中文好用`、`手机可用`、`商用需确认`。
- `prompt`：这个工具最适合的新手提示词。
- `alternatives`：同类替代工具。
- `myNote`：你自己的真实试用记录。

## 建议分类

你可以继续使用这些分类：

- 聊天写作
- 搜索研究
- 办公PPT
- 图片设计
- 视频数字人
- 编程开发
- 音频会议

也可以新增自己的分类，比如：

- 我常用
- 正在试用
- 已踩坑
- 付费中
- 客户推荐

新增分类不需要改代码，只要在 `tools.json` 的 `category` 里写新分类，网页会自动显示。

## 更新多久生效

保存 `tools.json` 后，GitHub Pages 通常 1 到 3 分钟内更新。

如果手机上还是旧内容，可以刷新页面，或者关闭浏览器重新打开。
