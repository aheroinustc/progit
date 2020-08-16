markdown基本语法介绍

本文档基于<https://www.markdownguide.org/>上面的内容。

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


# 【强调：加粗/倾斜】

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

This is really***very***important text.	

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


# 【代码块】
缩进至少四个空格或一个制表符。  
当它们在列表中时，将它们缩进八个空格或两个制表符。

**直接展示代码块**

    <html>
    <head>
        <title>Test</title>
    </head>

**列表中的代码块**
1.  Open the file.
2.  Find the following code block on line 21:

        <html>
        <head>
            <title>Test</title>
        </head>

3.  Update the title to match the name of your website.


# 【图片】

**直接展示图片**

![](./tux.png "企鹅")

**列表中的图片**
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.
   
    ![](./tux.png)
3. Close the file.



# 【反引号】

要将单词或短语表示为代码，请将其括在反引号（`）中。

`git for windows`是Git的Windows版本。

`vim`是优秀的linux文本编辑器。

**反引号转义**

``Use `code` in your Markdown file.``



# 【水平分隔线】
可在一行中用三个及以上的星号、减号、下划线来建立一个分隔线。

***
---
___

所有这三个的渲染输出看起来都相同。

# 【链接】

## 展示链接
[google](https://www.google.com/)

## 带有标题提示的链接
[baidu](https://www.baidu.com/  "百度一下，你就知道")

## 展示地址
<https://www.google.com/>

## Reference-style链接
 
This is the [Markdown Guide][1].

[1]:(https://www.markdownguide.org)

## 带有链接的图片
[![](./tux.png)](https://www.markdownguide.org)


# 【转义字符】

\* Without the backslash, this would be a bullet in an unordered list.

\`code\`