这里介绍了一些Github支持的高级格式。

# 【创建折叠部分】

<details><summary>点击此处展开</summary>
<p>

#### We can hide anything, even code!

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

</p>
</details>

Markdown 是默认折叠的。


# 【创建图表】

可以使用以下三种不同的语法在 Markdown 中创建关系图：`mermaid`、`geoJSON` 和 `topoJSON`、`ASCII STL`。

## 创建 Mermaid 关系图

Mermaid 是一款受 Markdown 启发的工具，可将文本呈现为关系图。 例如，Mermaid 可以呈现流程图、序列图、饼图等。 有关详细信息，请参阅 [Mermaid 文档](https://mermaid.js.org/config/Tutorials.html)。

使用 `mermaid` 语言标识符在围栏代码块中添加 Mermaid 语法。

Here is a simple flow chart:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;

```

```mermaid
erDiagram
          CUSTOMER }|..|{ DELIVERY-ADDRESS : has
          CUSTOMER ||--o{ ORDER : places
          CUSTOMER ||--o{ INVOICE : "liable for"
          DELIVERY-ADDRESS ||--o{ ORDER : receives
          INVOICE ||--|{ ORDER : covers
          ORDER ||--|{ ORDER-ITEM : includes
          PRODUCT-CATEGORY ||--|{ PRODUCT : contains
          PRODUCT ||--o{ ORDER-ITEM : "ordered in"

```

# 【编写数学表达式】

为了实现数学表达式的清晰传达，GitHub 支持 Markdown 中 LaTeX 格式的数学表达式。

使用Markdown在GitHub上显示数学表达式。

GitHub 的数学呈现功能使用 [MathJax](https://www.mathjax.org/)；是一种基于 `JavaScript` 的开源显示引擎。

**内联表达式**

注意空格。

$(\mathrm{i})\ x=\frac{-b\pm \sqrt{b^{2} -4ac}}{2a}$ ; $(\mathrm{ii})\ f(a) = {1\over 2\pi i} \oint \frac{f(z)}{z-a}dz$ ; $(\mathrm{iii})\ \iiint _{V} f( x,y,z) dV = \iiint\limits _{V} f( x,y,z) dxdydz$.

**块表达式**

$$(\nabla_X Y)^k = X^i (\nabla_i Y)^k =
           X^i \left( \frac{\partial Y^k}{\partial x^i} + \Gamma_{im}^k Y^m \right)$$

$$\int_D (\mathbf{\nabla} \cdot \mathbf{F})dV=\int_{\partial D} \mathbf{F}\cdot \mathbf{n}dS$$

$$\sigma = \sqrt{ \frac{1}{N} \sum_{i=1}^N (x_i -\mu)^2}$$

$$\begin{pmatrix}  
  a_{11} & \cdots & a_{1n} \\  
  \vdots & \ddots & \vdots \\  
  a_{m1} & \cdots & a_{mn}  
\end{pmatrix}$$

$$\begin{matrix}  
a & b \\ 
c & d  
\end{matrix}$$  

$$O = \begin{bmatrix}  
  0 & 0 & \cdots & 0 \\  
  0 & 0 & \cdots & 0 \\  
  \vdots & \vdots & \ddots & \vdots \\  
  0 & 0 & \cdots & 0  
\end{bmatrix}$$

$$\begin{vmatrix} 
a & b\\ 
c & d  
\end{vmatrix}$$

**围栏表达式**

```math

\vec{\nabla} \times \vec{F} =
            \left( \frac{\partial F_z}{\partial y} - \frac{\partial F_y}{\partial z} \right) \mathbf{i}
          + \left( \frac{\partial F_x}{\partial z} - \frac{\partial F_z}{\partial x} \right) \mathbf{j}
          + \left( \frac{\partial F_y}{\partial x} - \frac{\partial F_x}{\partial y} \right) \mathbf{k} 
  
```

```math
\begin{array}{l}  
  \nabla \cdot \mathbf{D} =\rho _f \\  
  \nabla \cdot \mathbf{B} = 0 \\  
  \nabla \times  \mathbf{E} = -\cfrac{\partial \mathbf{B}}{\partial t }  \\  
  \nabla \times  \mathbf{H} = \mathbf{J}_f +  \cfrac{\partial \mathbf{D}}{\partial t }   
\end{array} 
```

# 【警示语】
Markdown不提供直接支持，可以结合区块引用和`Emoji`来实现。

> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.

# 【视频快照】

如果Markdown应用程序支持HTML，您应该能够通过复制和粘贴YouTube等视频网站提供的HTML代码，在 Markdown文件中嵌入视频。此处展示快照。

[![冒險雷探長｜Lei's adventure](https://img.youtube.com/vi/Oo9uMA2FL6I/0.jpg)][1]

[1]: <https://www.youtube.com/watch?v=Oo9uMA2FL6I> "冒險雷探長"
