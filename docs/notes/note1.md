---
layout: default
title: note of lecture 1
---


# lecture 1 课堂笔记
<br>

## 课程基础要求  
<br>
- 数学基础  
- 软件安装  
- 基本编程能力  
>在课程中通过**实践**学习编程  
>需要有一定linux基础
<br>
<br>

## “AI4Omics”基础能力  
<br>
- biology and medical science  
- math  
- bioinformatics  
- computer science  
>“我们将教授生物信息学方面的专业技能，这些技能不是单纯地运行软件的能力，而是让你们拥有**探索各种真实数据的自由**”  
>self-learning&group study
<br>
<br>

## 4 steps of bioinformatics  
>解读“language of life”

### 1. question  
- 意识  
- 基因（为什么如此之少？如何影响健康？）  
<br>
### 2. information  
- 生命信息编码形式：DNA/RNA序列  
- NGS(next generation sequencing)  
    - DNA-seq  
    - RNA-seq  
    - epigenetics  
    - DNA/RNA/Protein interactions  
- 大数据/高维数据：多个体/多细胞/多组学  
- 宏基因组数据： 
    - environmental  
    - organismal  
<br>
### 3. analysis  
- 方法：NGS+bioinformatics tool  
- 例子：RNA variantions；cell types；gene signatures  
<br>
### 4. modeling  
- probabilistic model  
    - regression model：linear/logistic  
    - neural network model：deep learning  
-computational algorithm  
    - e.g. number sorting algorithm, dynamic programming algorithm  
<br>
<br>

## new paradigm driven by big-data 
<br>

### traditional hypothesis-driven science  
- question  
- information  
- analysis  
- modeling  
<br>

### big-data driven science  
- information  
- analysis  
- modeling  
- question  
>数据收集的极高效率+多角度分析可以让我们看到从未被发现的问题？
<br>
<br>

---
## 思考题：算法与模型的区别？  
<br>
<img width="2256" height="806" alt="屏幕截图 2026-03-03 191259" src="https://github.com/user-attachments/assets/9ff32bee-1925-4a13-bfad-bc16e5885776" />{: style="width: 100%;"}

<br>

## 思考题：鸡兔同笼  
<br>

### 小学解法  
假设笼子里全是鸡，则共应有14*2=28条腿。多出的38-28=10条腿代表其中有10/2=5只兔子。  
则鸡有9只，兔子有5只。  
<br>
### 中学解法  
设有x只鸡，y只兔子：  
x+y=14  
2x+4y=38  
解得x=9，y=5。  
<br>

## 思考题：为何小规模私有公司能赶上人类基因组计划？  
- 风险更高但更快的测序策略：HGP使用层次化shotgun策略，首先构建BAC文库，并通过基于序列标签的物理图谱首先确定每一片段的物理位置，再分别对各个大片段进行sanger测序和拼装。celera则采取全基因组shotgun测序方法，同时借助不同长度的DNA文库提供的“配对末端”信息，直接连接小片段。  
- 硬件设施支持和组装算法：celera获得了来自其他公司的支持，包括自动化测序设备、超级计算机等，并开发了专门的组装软件。这是他们处理全基因组鸟枪法产生的大量数据的基础。
- 借助HGP的公开数据：celera通过将序列与已发表的HGP数据（根据HGP的协定，测序结果需在24小时内向世界公开）比较，获得序列的物理位置信息。根据Nature的报道，HGP的数据可能帮助celera将测序深度从10倍降低到4倍，数据占比达到50%。这也引发了celera测序结果独立性的质疑。  
