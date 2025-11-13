---
title: "导航"
permalink: /mmistakes/navigation/
excerpt: "介绍如何定制主导航和启用面包屑链接。"
last_modified_at: 2025-11-11T15:59:40-04:00
toc: true
---

通过 Jekyll 数据文件定制站点导航链接。

## 主导航

主导航链接使用“要事优先”设计模式。也就是说，导航项会水平自动适应浏览器宽度，当不能全部显示时会使用折叠模式将部分菜单隐藏。

定义链接需要添加 title 和 URL 到 `_data/navigation.yml` 的 `main` 键下：

```yaml
main:
  - title: "Quick-Start Guide"
    url: /docs/quick-start-guide/
  - title: "Posts"
    url: /year-archive/
  - title: "Categories"
    url: /categories/
  - title: "Tags"
    url: /tags/
  - title: "Pages"
    url: /page-archive/
  - title: "Collections"
    url: /collection-archive/
  - title: "External Link"
    url: https://google.com
    target: _blank
```

这将为你创建一个如下图的自适应主导航菜单：

![priority plus masthead animation]({{ "/assets/images/mm-priority-plus-masthead.gif" | relative_url }})

你可以选择为每个 `main` 键下的 `title` 添加 `description`。 `description` 内容会在用户使用桌面浏览器并将鼠标指向链接时显示一个提示。

**专业提示：** 将最重要的链接放在前面以便使其随时可见，以免被隐藏到**菜单开关**之内。
{: .notice--info}

## 面包屑导航（ 测试版）

启用面包屑链接可以帮助访问者更好了解站点导航的层次。由于生成方法很脆弱，所以生成的链接并不总是可靠的。最好的办法是：

1. 基于永久链接结构使用分类，例如 `permalink: /:categories/:title/`
2. 手动为每个分类创建页面或者使用插件 [jekyll-archives](https://github.com/jekyll/jekyll-archives) 来自动生成。如果这些页面不存在，面包屑链接将会崩溃。

![breadcrumb navigation example]({{ "/assets/images/mm-breadcrumbs-example.jpg" | relative_url }})

```yaml
breadcrumbs: true  # 默认关闭
```

面包屑导航开始链接文本和分割符可以在 `_data/ui-text.yml` 中设置。

```yaml
breadcrumb_home_label : "Home"
breadcrumb_separator  : "/"
```

类似于 `Start > Blog > My Awesome Post` 的面包屑导航可以这样设置：

```yaml
breadcrumb_home_label : "Start"
breadcrumb_separator  : ">"
```

## 定制侧边栏导航菜单

查阅[**边栏**文档]({{ "/mmistakes/layouts/#custom-sidebar-navigation-menu" | relative_url }})获取更多关于定制导航菜单信息。
