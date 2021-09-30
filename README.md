# 比赛全周期试验记录
-------------------------------------------------------------
队友：AlvinAi96、Algor_Bruce <br>
整理者：Algor_Bruce <br>
记录整理模板参考：https://github.com/AlvinAi96/serverless_prediction#readme


该比赛项目分为三大模块：数据探索性分析、数据预处理(含特征工程)、模型(调参及融合)

# 一. EDA
后续补充

-------------------------------------------------------------

# 二. DataPreposss

### 2021.9.29
首次提交baselines
|编号|预处理手段|线下AUC测评分数|线上AUC分数|提交时间|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|未考虑引入train_inter, 进行了PSI选择特征, 12折交叉验证|0.869422|0.87505447910|2021.9.29|v0|

### 2021.9.30
|编号|预处理手段|线下AUC测评分数|线上AUC分数|提交时间|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|未考虑train_public和train_inter分布差异，对两部分训练集合并处理，进行了PSI选择特征, (交叉验证)cv=12|0.803242 | 未提交 | —— | v0 |
|2|根据特征重要性结果，删除了重要性排名靠后的若干变量，cv=10| 0.878252 |  0.88206691| v1 | 

-------------------------------------------------------------
# 三. Models

后续补充



