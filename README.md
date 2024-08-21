# Another Graph Editor  cn_zh 汉化版本


# 别样制图

一款受 [CS Academy's graph editor](https://csacademy.com/app/graph_editor/)，启发的图编辑器，专为竞赛编程设计。

使用React、Typescript、Tailwind CSS和HTML Canvas制作。


<p align="center">
    <img src="screenshots/main.png?" />
</p>

<p align="center">
<em>A Three-Component Graph</em>
</p>

## 特性

常见输入格式：
边列表 u v [w]，表示从节点 u 到节点 v 的一条边，其中 w 是可选的边标签。
Leetcode风格的邻接表字符串，如 [[2,4],[1,3],[2,1],[4,3]]；确保字符串内无空格。
父子数组，其中 p[i] 和 c[i] 表示从节点 p[i] 到 c[i] 的一条边。
假设节点数量非零，还可以为每个节点打上标签。这在给定数组 a 的场景下很有用，其中 a[i] 对应节点 i 的值。
标签偏移（将零索引输入转换为一索引，反之亦然）
深色/浅色主题
无向/有向模式
普通/树模式
显示/隐藏桥和割点
显示/隐藏连通分量

<p align="center">
    <img src="screenshots/parentChild.png?" />
</p>

<p align="center">
<em>A Demonstration of the Parent-Child Input Format</em>
</p>

## 父子输入格式演示

> [!NOTE]
> *树模式* 和 *桥* 仅适用于无向图。

> [!NOTE]
> 对于有向图，将显示**强连通分量**。

## 配置

除了浅色/深色主题外，还提供两个滑块，用于在离散间隔内调整*节点半径*和*线条粗细*。

> [!NOTE]
> 当节点半径改变时，字体大小会相应缩放以保持可读性。

默认情况下，图处于*力导向模式*，其中边将一切连接在一起，节点相互排斥，创造出类似太空的效果。要禁用此行为，只需切换*锁定模式*。

## 使用方法

根据您的喜好调整输入格式并开始输入！

> [!NOTE]
> 如果您来自像[Codeforces](https://codeforces.com/)这样的平台，并且输入数据包含`n m`，分别表示顶点和边的数量，请在复制粘贴测试用例数据时**省略**它。同样，如果您有一个数组`p`，其中`p[i]`表示`i`的父节点，请仔细检查父节点数组是否与子节点数组对齐。

> [!NOTE]
> 要输入单个节点，请输入`u`或`u u`。

> [!NOTE]
> 在输入节点标签时，如果您想跳过某个特定节点，请使用字符`_`作为占位符。

### 树模式

在此模式下，输入数据中出现的*第一个*节点将成为根节点；因此，如果您需要将某个任意节点`u`作为根节点，请在输入数据的顶部输入`u`。

<p align="center">
    <img src="screenshots/twoRoot.png?" />
</p>

<p align="center">
<em>Making Node 2 the Root Instead of Node 1</em>
</p>

如果图不是树怎么办？那么，将显示**深度优先搜索（DFS）树**，其中*回边*将以虚线显示。

<p align="center">
    <img src="screenshots/dfsTree.png?" />
</p>

<p align="center">
<em>A DFS Tree With an Offset of -1</em>
</p>

## Credits

- [CS Academy's Graph Editor](https://csacademy.com/app/graph_editor/)
- [Codeforces](https://codeforces.com/)
- [Atcoder](https://atcoder.jp/)
- [USACO Guide](https://usaco.guide/)
- [-is-this-fft-'s Blog on the DFS Tree](https://codeforces.com/blog/entry/68138)
