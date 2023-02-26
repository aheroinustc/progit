本文档参考了如下链接：

- [Markdown Guide](https://www.markdownguide.org/)

- [Markdown Preview Enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)

- [Getting started with writing and formatting on GitHub](https://docs.github.com/zh/get-started/writing-on-github)

此处出现的语法，已经验证在github上面支持。

# 【标题】

# Heading level 1
## Heading level 2
### Heading level 3
#### Heading level 4
##### Heading level 5
###### Heading level 6


# 【段落】
要创建段落，请使用空白行分隔一行或多行文本。

I really like using Markdown.

I think I'll use it to format all of my documents
from now on.


# 【换行】
请以两个或多个空格结束一行，然后键入回车即可。

This is the first line.  
And this is the second line.


# 【强调】

## 【加粗】
I just love **bold text**.

I just love __bold text__.	

Love**is**bold.	

## 【倾斜】
Italicized text is the *cat's meow*.

Italicized text is the _cat's meow_.

A*cat*meow	

## 【加粗并倾斜】

This text is ***really important***.

This text is ___really important___.

**This is really _very_ important text**.	

## 【删除线】
~~This was mistaken text~~

## 【上/下标】

LV<sup>TM</sup>

LV<sub>TM</sub>

# 【区块引用】

## 【单段落】
> Dorothy followed her through many of the beautiful rooms in her castle.

## 【多段落】

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

## 【嵌套】

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

## 【混合】

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.


# 【列表】

## 【有序列表】

1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item
5. Fifth item


## 【无序列表】

破折号（-），星号（*）或加号（+）都可以

- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item

### 【无序列表包含段落】
-   This is the first list item.
-   Here's the second list item.

    I need to add another paragraph below the second list item.
-   And here's the third list item.

### 【无序列表包含块引用】
-   This is the first list item.
-   Here's the second list item.
    > A blockquote would look great below the second list item.
-   And here's the third list item.

## 【混合列表】

1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item


# 【任务清单】
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media


# 【引用代码】

缩进至少四个空格或一个制表符。当它们在列表中时，将它们缩进八个空格或两个制表符。

## 直接展示代码块

    <html>
    <head>
        <title>Test</title>
    </head>

## 列表中的代码块
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
        <head>
            <title>Test</title>
        </head>

3.  Update the title to match the name of your website.


## 使用单反引号\`

使用单反引号可标注句子中的代码或命令。 反引号中的文本不会被格式化。 

Use `git status` to list all new or modified files that haven't yet been committed.

`git for windows`是Git的Windows版本。

`vim`是优秀的linux文本编辑器。

**反引号转义**

``Use `code` in your Markdown file.``


## 围栏代码块

如果不想使用缩进来产生代码块，可以使用如下风格:

通过在代码块的前后输入三反引号```，可创建围栏代码块。

我们建议在代码块的前后各留一个空白行，使原始格式更易辨读。

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

要在列表中保留格式，请确保将非围栏代码块缩进八个空格。

**语法高亮**

```java
 public class HelloWorld{
    pubic static void main(String[] args){

    }
 }
```
# 【图片】

**直接展示图片**

![Tux, the Linux mascot](./tux.png "企鹅")

**列表中的图片**
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.
   
    ![Tux, the Linux mascot](./tux.png)
3. Close the file.

# 【水平分隔线】
可在一行中用三个及以上的星号、减号、下划线来建立一个分隔线。
为了兼容性，之前之后留一空白行。

***

---

___

所有这三个的渲染输出看起来都相同。

# 【链接】

## 展示链接
[google](https://www.google.com/)

## 带有标题提示的链接
[baidu](https://www.baidu.com/  "百度一下，你就知道")

## 快速展示URL或者邮箱
<https://www.google.com/>

<fake@example.com>

## 格式化链接

I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.

## Reference-style链接
 
This is the [Markdown Guide][1].

> This site was built using [GitHub Pages][2].

参考放置位置通常是底部。

## 带有链接的图片
[![Tux, the Linux mascot](./tux.png)][3]

此次使用了图片的相对位置。或者直接从互联网引用：

![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)


# 【转义字符示例】

\*  \-  \+  \\ \! \|  

\`code\`

# 【脚注】

脚注使您可以添加注释和参考，而不会使文档正文混乱。

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code:

    Indent paragraphs to include them in the footnote.
    
    `{ my code }`
    
    Add as many paragraphs as you like.

# 表格 { #table }

可以使用竖线 `|` 和连字符 `-` 创建表。

连字符用于创建每列的标题，而竖线用于分隔每列。

| Syntax   | Description |
|-------   |-------      |
| Header   | Title       |
| Paragraph| Text        |

无需在列内准确对齐。 标题行的第一列中必须至少有三个横线。

| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |

## 对齐|格式化

可以在表格中使用格式，例如链接、内联代码块和文本样式：

| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |

可以通过在标题行中连字符的左侧、右侧或两侧添加冒号 `:`，来靠左、靠右或居中对齐列中的文本。

若要包含竖线 `|` 作为单元格中的内容，请在竖线前使用 `\`

| Syntax      | Description | Test Text     |
|:---         |:---:        |---:           |
| Header\|    | **Title**   | a&#124;b      |
| Paragraph   | [baidu][1]  | `vim`         |

[1]: https:www.baidu.com


# 【标题id】
[跳转到标题：表格](#table)

[1]: https://www.markdownguide.org
[2]: <https://pages.github.com/>  "GitHub Pages"
[3]: <https://zh.wikipedia.org/zh/Tux> "Tux"