---
title: "工具类"
permalink: /mmistakes/utility-classes/
excerpt: "用于对齐图文、按钮样式和警示的 CSS 类。"
last_modified_at: 2018-11-25T19:46:43-05:00
toc: true
toc_label: "工具类"
toc_icon: "cogs"
---

使用 Kramdown Markdown 渲染 Jekyll 文本允许添加 [block](http://kramdown.gettalong.org/quickref.html#block-attributes) 和 [行内属性](http://kramdown.gettalong.org/quickref.html#inline-attributes)。如果你想使用 Markdown 书写和添加定制图文样式，那么这很有用。

**Jekyll 3：** Kramdown 是 `jekyll new` 创建站点时默认的编辑格式，它也用于 GitHub Pages。如果不想用 Kramdown？当然可以。下面的类仍然可以用于标准 HTML。
{: .notice--warning}

## 文本对齐

使用下面的类对齐文本块。

左对齐文本用 `.text-left`
{: .text-left}

```markdown
Left aligned text
{: .text-left}
```

---

居中对齐文本用 `.text-center`
{: .text-center}

```markdown
Center aligned text.
{: .text-center}
```

---

右对齐文本用 `.text-right`
{: .text-right}

```markdown
Right aligned text.
{: .text-right}
```

---

**两端对齐文本**用 `.text-justify` Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque vel eleifend odio, eu elementum purus. In hac habitasse platea dictumst. Fusce sed sapien eleifend, sollicitudin neque non, faucibus est. Proin tempus nisi eu arcu facilisis, eget venenatis eros consequat.
{: .text-justify}

```markdown
Justified text.
{: .text-justify}
```

---

不换行文本用 `.text-nowrap`
{: .text-nowrap}

```markdown
No wrap text.
{: .text-nowrap}
```

## 图像对齐

定位图像用下面的类。

![image-center]({{ "/assets/images/image-alignment-580x300.jpg" | relative_url }}){: .align-center}

上面的图像被居中（**centered**）了。

```markdown
![image-center](/assets/images/filename.jpg){: .align-center}
```

---

![image-left]({{ "/assets/images/image-alignment-150x150.jpg" | relative_url }}){: .align-left} 一个 150×150 大小的图像使用 **左对齐**，段落的文字会将图像之外的剩余部分环绕包围起来。图像的上侧、下侧、右侧都会留下一定的空间以保持与文字之间的留白。图像就在那里，左侧对的非常齐。右侧并不是需要我关心的，就是这样。既然是左对齐，就不要让别人说你做的不对——你就说左侧对没对齐吧？

```markdown
![image-left](/assets/images/filename.jpg){: .align-left}
```

---

![image-right]({{ "/assets/images/image-alignment-300x200.jpg" | relative_url }}){: .align-right}

现在再进行**右对齐**。同样，图像的上侧、下侧和左侧也必须留下一定的空间做留白。这样图像就在那里，右侧对的非常齐。图像的左侧不需要关心对没对齐，因为者不是重点。既然是右对齐，就不要让别人说三道四——你就说右侧对没对齐吧？

```markdown
![image-right](/assets/images/filename.jpg){: .align-right}
```

---

![full]({{ "/assets/images/image-alignment-1200x4002.jpg" | relative_url }})
{: .full}

上面的图像右侧延伸到了父容器的外侧。

```markdown
![full](/assets/images/filename.jpg)
{: .full}
```

## 按钮

当时用 `.btn .btn--primary` 类时，链接就有了更多形式的展示。

```html
<a href="#" class="btn btn--primary">Link Text</a>
```

| 按钮类型      | 示例    | 类    | Kramdown |
| ------        | ------- | ----- | ------- |
| Default       | [Text](#link){: .btn} | `.btn` | `[Text](#link){: .btn}` |
| Primary       | [Text](#link){: .btn .btn--primary} | `.btn .btn--primary` | `[Text](#link){: .btn .btn--primary}` |
| Success       | [Text](#link){: .btn .btn--success} | `.btn .btn--success` | `[Text](#link){: .btn .btn--success}` |
| Warning       | [Text](#link){: .btn .btn--warning} | `.btn .btn--warning` | `[Text](#link){: .btn .btn--warning}` |
| Danger        | [Text](#link){: .btn .btn--danger} | `.btn .btn--danger` | `[Text](#link){: .btn .btn--danger}` |
| Info          | [Text](#link){: .btn .btn--info} | `.btn .btn--info` | `[Text](#link){: .btn .btn--info}` |
| Inverse       | [Text](#link){: .btn .btn--inverse} | `.btn .btn--inverse` | `[Text](#link){: .btn .btn--inverse}` |
| Light Outline | [Text](#link){: .btn .btn--light-outline} | `.btn .btn--light-outline` | `[Text](#link){: .btn .btn--light-outline}` |

| 按钮型号    | 示例    | 类    | Kramdown |
| ----------- | ------- | ----- | -------- |
| X-Large     | [X-Large Button](#){: .btn .btn--primary .btn--x-large} | `.btn .btn--primary .btn--x-large` | `[Text](#link){: .btn .btn--primary .btn--x-large}` |
| Large       | [Large Button](#){: .btn .btn--primary .btn--large} | `.btn .btn--primary .btn--large` | `[Text](#link){: .btn .btn--primary .btn--large}` |
| Default     | [Default Button](#){: .btn .btn--primary} | `.btn .btn--primary` | `[Text](#link){: .btn .btn--primary }` |
| Small       | [Small Button](#){: .btn .btn--primary .btn--small} | `.btn .btn--primary .btn--small` | `[Text](#link){: .btn .btn--primary .btn--small}` |

## 警示

将一段文字变成警示。

| 警示类型    | 类                 |
| ----------- | -----              |
| Default     | `.notice`          |
| Primary     | `.notice--primary` |
| Info        | `.notice--info`    |
| Warning     | `.notice--warning` |
| Success     | `.notice--success` |
| Danger      | `.notice--danger`  |

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice}` class.
{: .notice}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--primary}` class.
{: .notice--primary}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--info}` class.
{: .notice--info}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--warning}` class.
{: .notice--warning}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--success}` class.
{: .notice--success}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--danger}` class.
{: .notice--danger}

{% capture notice-text %}
You can also add the `.notice` class to a `<div>` element.

* Bullet point 1
* Bullet point 2
{% endcapture %}

<div class="notice--info">
  <h4 class="no_toc">Notice Headline:</h4>
  {{ notice-text | markdownify }}
</div>
