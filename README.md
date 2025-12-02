# Superstore-PowerBI_Dashboard
# Superstore Sales Dashboard

## 📊 项目概述
这是一个使用 Power BI 创建的零售销售分析仪表板，基于 Kaggle Superstore 数据集。

## 🎯 业务目标
- 分析 2014-2017 年销售趋势
- 识别高利润和亏损产品
- 评估不同地区和客户细分的表现
- 为业务决策提供数据支持

## 📁 数据来源
- **数据集**: Kaggle Superstore Dataset
- **记录数**: 9,994 条订单
- **时间范围**: 2014-2017
- **包含内容**: 订单、客户、产品、地区信息

## 🔧 技术栈
- **工具**: Power BI Desktop
- **数据处理**: Power Query
- **计算逻辑**: DAX
- **可视化**: 20+ 交互式图表

## 📈 核心功能

### 页面 1: 执行摘要
- 关键 KPI 监控
- 销售趋势分析
- 地区和类别对比

### 页面 2: 销售深度分析
- 月度销售和利润
- Top 10 产品排名
- 客户细分表现

### 页面 3: 利润分析
- 产品利润率热力图
- 折扣影响分析
- 亏损产品识别

### 页面 4: 客户洞察
- 客户价值分布
- 重复购买行为
- 客户细分矩阵

## 💡 关键发现

1. **销售趋势**: 2017年销售额达到$733K，同比增长 20.4%
2. **地区表现**: 西部地区销售占比最高（31.6%），但利润率偏低
3. **产品分析**: 
   - Technology 类别利润率最高（14.2%）
   - Tables 子类别持续亏损，建议调整定价
4. **折扣影响**: 高折扣（>20%）产品利润率显著降低
5. **客户洞察**: 20% 的客户贡献了 60% 的销售额

## 📊 DAX 亮点
```dax
// 同比增长计算
YoY Growth = 
VAR CurrentSales = [Total Sales]
VAR LastYearSales = 
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
RETURN
    DIVIDE(CurrentSales - LastYearSales, LastYearSales, 0)

// 客户留存率
Customer Retention Rate = 
DIVIDE([Repeat Customers], [Total Customers], 0)
```

## 🖼️ 截图展示


## 🚀 如何使用

1. 下载 `Superstore-Dashboard.pbix` 文件
2. 用 Power BI Desktop 打开
3. 数据会自动刷新（如果数据源路径正确）
4. 使用切片器进行交互式分析

## 📝 学习要点

本项目展示了以下 Power BI 技能：
- ✅ Power Query 数据清洗和转换
- ✅ 数据建模（日期表、关系）
- ✅ DAX 度量值（时间智能、聚合）
- ✅ 多页面仪表板设计
- ✅ 交互式筛选和钻取
- ✅ 条件格式和视觉最佳实践
