---
title: "文集"
permalink: /mmistakes/collections/
excerpt: "文集使用建议和默认 Front Matter。"
last_modified_at: 2025-11-11T16:00:02-04:00
---

文集正如你所知道的页面和文章一样，如果你对它们还一无所知，那么请先阅读 [Jekyll 文档](https://jekyllrb.com/docs/collections/)了解文集知识。

主题内建支持文集，你可以查看[这几个示例](https://mmistakes.github.io/minimal-mistakes/collection-archive/)演示站点——（[portfolio](https://mmistakes.github.io/minimal-mistakes/portfolio/)，[recipes](https://mmistakes.github.io/minimal-mistakes/recipes/)，[pets](https://mmistakes.github.io/minimal-mistakes/pets/)）。 

**文集示例：** 这组文档就使用了[文集](https://github.com/{{ site.repository }}/blob/master/docs/_docs/)，你完全可以参考使用。
{: .notice--info}

---

一个流行的文集用例是建立个人网站的个人档案，让我们赶紧来完成这个设置。

**第一步：** 通过添加下面代码到 `_config.yml` 配置档案文集。

```yaml
collections:
  portfolio:
    output: true
    permalink: /:collection/:path/
```

这会为 `_portfolio` 文件夹内的每个 portfolio 文档在 `_site/portfolio/<document-filename>/` 文件夹内生成 `index.html` 文件。

**第二步：** 正如文章和页面你需要为文集设置默认的 Front Matter：

```yaml
defaults:
  # _portfolio
  - scope:
      path: ""
      type: portfolio
    values:
      layout: single
      author_profile: false
      share: true
```

**第三步：** 现在在 `_pages` 文件夹内建立一个 portfolio.md 文件。

```yaml
---
title: Portfolio
layout: collection
permalink: /portfolio/
collection: portfolio
entries_layout: grid
classes: wide
---
```

**第四步：** 创建诸如 [`_portfolio/foo-bar-website.md`](https://github.com/{{ site.repository }}/blob/master/docs/_portfolio/foo-bar-website.md) 的内容页面，最终显示如下。

![portfolio collection example]({{ "/assets/images/mm-portfolio-collection-example.jpg" | relative_url }})
