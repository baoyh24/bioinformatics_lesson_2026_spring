# Reads mapping--Bowtie

### 基本流程

- BWT算法：轮换后按首字母排列——实现相同字母相邻排列，便于压缩
- 在BWT算法变换后，相同字母的顺序不变
- last-first mapping （LF mapping）：通过指针跳转找到短序列？？而不是查找
- 确定序列位置：
  - 通过LF走到头
  - milestone：每32行设置一个已知位置的milestone，通过LF检索序列位置时走到milestone即可

- checkpoint：记录各个碱基的rank



### memory cost

- BWT=genome size
- milestone~50% genome size
- checkpoints~15% genome size
- Bowtie速度的提升主要源于BWT支持的LF mapping而不是BWT算法的存储压缩



### 容错与重复

- 在无法匹配上时，先随意修改为另一个碱基重新尝试，如果map上了则继续进行，同时记录好mismatch情况
- 容错的调整：根据mapping对象更改，例如microRNA 21~23bp，一般不允许错配，但是mRNA片段~200bp则允许，使用默认的容错数
- 如果研究transposon，则需要允许重复。但如果研究蛋白质基因则一般不允许大量重复（使用默认参数）



### 思考题

为什么bowtie不需要存储第一列的rank也可以迅速移动指针



