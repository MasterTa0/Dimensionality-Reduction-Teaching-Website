<div align="center">

# 降维（Dimensionality Reduction）教学网站

统计学习 / 数据挖掘 · 常用降维方法的直觉、推导与实务（PCA / LDA / t-SNE / UMAP 等）

- Web（GitHub Pages）：
<p>
  <a href="https://masterta0.github.io/Dimensionality-Reduction-Teaching-Website/">
    <img alt="GitHub Pages" src="https://img.shields.io/badge/GitHub%20Pages-Online-blue" />
  </a>
</p>



</div>

---

## 目录

- [Access](#access)
- [Course Outline](#course-outline)
- [Learning Objectives](#learning-objectives)
- [Local Preview](#local-preview)
- [Deployment (GitHub Pages)](#deployment-github-pages)
- [References](#references)
- [Contributing](#contributing)
- [License](#license)

---


## Course Outline

本网站面向“能用 + 能解释”的学习目标，强调直觉、关键公式与实务选择。建议从 PCA 入门，再扩展到监督/非线性与流形学习方法。

1. **为什么需要降维**
   - 维度灾难与可视化需求
   - 冗余特征、噪声与泛化
   - 压缩与特征工程视角

2. **线性无监督降维：PCA**
   - 几何直觉：最大方差投影
   - 协方差矩阵特征分解 / SVD 视角
   - 主成分选择（解释方差比、Scree plot）
   - 标准化、中心化与实现细节

3. **线性监督降维：LDA（Fisher 判别）**
   - 类内散度与类间散度
   - 广义特征值问题
   - 与分类器的关系（作为预处理 vs 端到端）

4. **非线性与流形学习**
   - t-SNE：邻域保持与可视化（强调“可视化优先”）
   - UMAP：图结构与流形假设（强调速度与可扩展性）
   - Isomap / LLE 等方法的直觉对比（可选）

5. **随机投影与高维近似**
   - Johnson–Lindenstrauss 引理直觉
   - 计算效率与近似误差权衡

6. **模型选择与实务要点**
   - 降维用于：可视化 / 去噪 / 压缩 / 提升下游模型
   - 过拟合与信息泄漏（训练集拟合降维器，再变换测试集）
   - 解释性 vs 表现 vs 可视化的取舍
   - 常见坑：未标准化、把 t-SNE 当特征工程、维度选取拍脑袋

7. **练习与案例（可扩展）**
   - Iris / MNIST 可视化对比（PCA vs t-SNE vs UMAP）
   - 高维稀疏特征的压缩与聚类/分类效果对比

---

## Learning Objectives

完成学习后，你应能够：

- 解释“降维”的三类常见目标：**可视化 / 压缩去噪 / 下游任务辅助**
- 熟练复述 PCA 的直觉与数学形式（特征分解/SVD、解释方差）
- 理解 LDA 的监督思想（类间最大化、类内最小化）与适用条件
- 清楚 t-SNE、UMAP 的定位：更偏可视化与结构展示，而非稳定的特征工程
- 能根据数据形态与任务选择合适方法，并说明取舍理由
- 掌握正确的工程流程：**先在训练集拟合降维器，再对验证/测试集变换**

---

## Local Preview

本项目为静态网页，建议用本地静态服务器预览：

### Option A: Python

```bash
python3 -m http.server 8000
# 浏览器打开：http://localhost:8000
