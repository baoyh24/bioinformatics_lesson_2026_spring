# lecture 2: higher dimension information

## linguistics vs bioinformatics

| 语言学                    | 模型               | 软件                            |
| ------------------------- | ------------------ | ------------------------------- |
| regular：声音识别（一维） | HMM： gene finder  | Genscan（mRNA）/Pfam（Protein） |
| context-free              | SCFG：RNA二级结构  | Rfam                            |
| context-sensitive         | transformer（LLM） | AlphaFold                       |

- 隐马尔可夫模型：HMM：参考按照一定的语法生成句子——可以按照一定的规则生成序列
  - 生成过程（derivation path）-parsing即为生成结果（sequence）

- CFG：调整生成“语法”：一次生成一对碱基/一个loop——对应产生RNA二级结构
  - derivation path = parsing tree = structure
  - 协同突变：配对碱基同时突变不影响二维结构
- transformer：在输出过程中同时考虑临近和更远的部分（self-attention）而不是只考虑上一个元素
  - 每个新元素生成都需要考虑全局
  - 基于强的运算能力

- higher dimension？组学
  - system thinking：干预单个基因所产生的影响未必是自然的
  - AI virtual cell & multiOmics
  - 精准医疗：MultiOmics input：clinical data+genomics data
    - obstacles in early discovery of cancer：时空异质性：空间（细胞类型）差异性；发展周期长，不同阶段有较大区别
    - 多维数据收集&建模——识别高风险人群/早期诊断
    - foundational model 适应不同组学分析/multi-model 合作