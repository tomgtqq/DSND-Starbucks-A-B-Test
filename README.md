## 星巴克促销活动 A/B 测试

<div align="center">
<img src="https://opj.ca/wp-content/uploads/2018/02/New-Starbucks-Logo-1200x969.jpg" width="20%" height="20%">
</div>
 
#### 背景信息

星巴克原先使用该数据集作为面试题。这道练习的数据包含 120,000 个数据点，按照 2:1 的比例划分为训练文件和测试文件。数据模拟的实验测试了一项广告宣传活动，看看该宣传活动能否吸引更多客户购买定价为 10 美元的特定产品。由于公司分发每份宣传资料的成本为 0.15 美元，所以宣传资料最好仅面向最相关的人群。每个数据点都有一列表示是否向某个人发送了产品宣传资料，另一列表示此人最终是否购买了该产品。每个人还有另外 7 个相关特征，表示为 V1-V7。

#### 优化策略

你的任务是通过训练数据了解 V1-V7 存在什么规律表明应该向用户分发宣传资料。具体而言，你的目标是最大化以下指标：

* **增量响应率 (IRR)** 

IRR 表示与没有收到宣传资料相比，因为推广活动而购买产品的客户增加了多少。从数学角度来说，IRR 等于推广小组的购买者人数与购买者小组客户总数的比例 (_treatment_) 减去非推广小组的购买者人数与非推广小组的客户总数的比例 (_control_)。

```
  IRR = purch_treat/cust_treat - purch_ctrl/cust_ctrl
```

* **净增量收入 (NIR)**

NIR 表示分发宣传资料后获得（丢失）了多少收入。从数学角度来讲，NIR 等于收到宣传资料的购买者总人数的 10 倍减去分发的宣传资料份数的 0.15 倍，再减去没有收到宣传资料的购买者人数的 10 倍。

```
  NIR = (10*purch_treat - 0.15*cust_treat) - 10*purch_ctrl
```

### Built With

* [Pandas](https://pandas.pydata.org/) - pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool.
* [scikit-learn](https://scikit-learn.org) - scikit-learn is a Python module for machine learning built on top of SciPy.

### Versioning

* We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

### Authors

* **Tom Ge** - *Fullstack egineer* - [github profile](https://github.com/tomgtqq)

### License

* This project is licensed under the MIT License
