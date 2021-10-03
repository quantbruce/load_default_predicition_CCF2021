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
|编号|预处理手段|线下AUC测评分数|线上AUC分数|代码版本|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|未考虑引入train_inter, 进行了PSI选择特征, 12折交叉验证|0.869422|0.87505447910|baseline_20210929_v1|mysub_20210929_2219_seed|

### 2021.9.30
|编号|预处理手段|线下AUC测评分数|线上AUC分数|代码版本|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|未考虑train_public和train_inter分布差异，对两部分训练集合并处理，进行了PSI选择特征, (交叉验证)cv=12|0.803242 | 未提交 |mysub_20210930_2059_seed|
|2|未考虑train_public和train_inter分布差异, 根据特征重要性结果，删除了重要性排名靠后的若干变量，cv=10| 0.878252 | 0.88206691 |baseline_20210930_v1|mysub_20210930_2349_seed| 

### 2021.10.2
|编号|预处理手段|线下AUC测评分数|线上AUC分数|代码版本|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|引入train_inter进行分析，并根据train_pulic预测train_inter，并从train_inter中选取满足条件的样本来扩充train_public数据集|0.983422|**0.88547781**|baseline_20211002_v1|mysub_20211002_2340_seed|

分析: 虽然成绩有所提高，排名也进了6%，但是线下分数远高于了线上分数，预测出现了过拟合。
      初步分析，应该是train_inter融合时，出现了信息泄露。 具体原因，后续进一步挖掘。  

### 2021.10.3
|编号|预处理手段|线下AUC测评分数|线上AUC分数|代码版本|数据版本|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|在昨天的基础上，添加了post_code的衍生变量|0.984907|没有提升|baseline_20211003_v1|mysub_20211003_1657_seed|



-------------------------------------------------------------

# 三. Models


后续补充



