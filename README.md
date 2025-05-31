# 现金流时间分布图 | Cash Flow Time Distribution Visualization

一个交互式的财富积累策略可视化工具，帮助理解不同投资策略的现金流特征和时间分布。

An interactive wealth accumulation strategy visualization tool that helps understand the cash flow characteristics and time distribution of different investment strategies.

## 🌟 功能特点 | Features

- 📊 **动态数据可视化** - 使用 D3.js 创建交互式现金流图表
- 🎯 **三种策略对比** - 短期爆发型、中期稳定型、长期指数型投资策略
- 📱 **响应式设计** - 适配桌面端和移动端设备
- 🖱️ **交互式体验** - 鼠标悬停显示详细数据信息
- 🎨 **现代化UI** - 渐变背景、卡片式布局、优雅动画效果

## 📈 投资策略分析 | Investment Strategy Analysis

### 短期爆发型（0-12个月）
- **特点**: 快速现金流，需要持续投入
- **适用**: 副业开发、轻资产创业、平台经济
- **收益曲线**: 前期快速增长，后期增速放缓

### 中期稳定型（1-3年）
- **特点**: 稳定被动收入，复利效应开始显现
- **适用**: 股息投资、REITs基金、债券基金
- **收益曲线**: 阶梯式增长，6-12个月进入稳定期

### 长期指数型（3年以上）
- **特点**: 指数增长，真正的"睡后收入"
- **适用**: 房产租赁、版权收入、企业股权
- **收益曲线**: 18个月后增速加快，后期呈指数级增长

## 🚀 快速开始 | Quick Start

### 本地运行
1. 克隆项目到本地
```bash
git clone [repository-url]
cd invest.kerrickchan.com
```

2. 直接在浏览器中打开 `index.html` 文件
```bash
open index.html
```

### 本地服务器运行
如果需要通过本地服务器运行（推荐）：

```bash
# 使用 Python
python -m http.server 8000

# 使用 Node.js http-server
npx http-server

# 使用 PHP
php -S localhost:8000
```

然后在浏览器中访问 `http://localhost:8000`

## 🛠️ 技术栈 | Tech Stack

- **前端框架**: 纯 HTML/CSS/JavaScript
- **数据可视化**: D3.js v7
- **样式**: CSS3 (Flexbox, Grid, 渐变, 动画)
- **字体**: Segoe UI, Microsoft JhengHei
- **响应式**: 媒体查询适配移动端

## 📱 浏览器支持 | Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📊 数据模型 | Data Model

图表基于以下假设生成模拟数据：
- 月投入金额: ¥3,000
- 年化收益率: 4%-12%
- 时间范围: 0-36个月

### 计算公式示例
```javascript
// 短期现金流计算
if (month <= 6) {
    shortTerm = Math.pow(month, 1.8) * 100;
} else if (month <= 18) {
    shortTerm = 1800 + (month - 6) * 100;
} else {
    shortTerm = 3000 - (month - 18) * 50;
}
```

## 🎨 界面设计 | UI Design

### 颜色方案
- **主色调**: #2c5282 (深蓝)
- **短期策略**: #4299e1 (蓝色)
- **中期策略**: #f56565 (红色)
- **长期策略**: #ed8936 (橙色)
- **背景渐变**: #f5f7fa → #e4edf5

### 布局特点
- 容器最大宽度: 1200px
- 卡片圆角: 12px
- 阴影效果: 多层次 box-shadow
- 动画: hover 效果和 transition

## 📁 项目结构 | Project Structure

```
invest.kerrickchan.com/
├── index.html          # 主页面文件
├── README.md           # 项目说明文档
└── assets/             # 静态资源（可选）
    ├── images/         # 图片资源
    └── fonts/          # 字体文件
```

## 🔧 自定义配置 | Customization

### 修改数据参数
在 `generateData()` 函数中调整：
- 时间范围（当前为36个月）
- 收益计算公式
- 增长率参数

### 修改样式
在 CSS 部分调整：
- 颜色主题
- 字体设置
- 布局尺寸
- 动画效果

### 添加新策略
1. 在数据生成函数中添加新的计算逻辑
2. 在图例中添加新的策略项
3. 在可视化代码中添加对应的曲线绘制

## 📝 许可证 | License

本项目仅供学习和研究使用。投资有风险，实际收益可能因市场波动和个人执行力而异。

This project is for educational and research purposes only. Investment involves risks, and actual returns may vary due to market fluctuations and individual execution capabilities.

## 🤝 贡献 | Contributing

欢迎提交 Issue 和 Pull Request 来改进这个项目！

Issues and Pull Requests are welcome to improve this project!

## 📞 联系方式 | Contact

- 项目作者: Kerrick Chan
- 邮箱: [your-email@example.com]
- 网站: invest.kerrickchan.com

---

> "财富积累如同竹子生长 - 前4年仅长3厘米，第5年开始每天疯长30厘米。现金流建设初期的缓慢不是停滞，而是在扎根。"

*注：图表数据基于理论计算，实际投资请咨询专业理财顾问。*
