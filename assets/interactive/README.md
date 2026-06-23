# 交互演示

## 布朗运动与随机游走

**文件：** [`brownian-random-walk.html`](brownian-random-walk.html)

**打开方式：**

1. 在资源管理器中双击该 HTML 文件；或
2. 在项目根目录执行：
   ```bash
   # Windows
   start assets\interactive\brownian-random-walk.html
   ```

**功能：**

- **数学 · 布朗运动**：一维离散布朗运动路径动画，实时显示步数与位置 W(t)
- **量化金融 · 股价路径**：多只虚拟股票随机游走 + 终点价格直方图
- 播放 / 暂停 / 单步 / 重置，可调速度与路径数量

与第一章 Notebook 实验一（50 只虚拟股票随机游走）概念一致，适合自学演示。

---

## 日收益率动态演示

**文件：** [`daily-return-demo.html`](daily-return-demo.html)

**配套章节：** `notebooks/phase2_intro/01_理解波动率.ipynb` · 5.3 节

**打开方式：**

1. 在 Notebook 公式下方点击链接跳转；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\daily-return-demo.html
   ```

**功能：**

- 逐日代入 $r_t = (P_t - P_{t-1}) / P_{t-1}$，显示 $P_{t-1}$（橙）与 $P_t$（蓝）
- **252 个交易日**（约一年）模拟行情，逐日播放
- 左侧面板公式代入 + 右侧双图（价格 + 收益率柱状图）
- 播放 / 暂停 / 单步 / 重置，可调速度

动画在独立页面中运行，不占用 Notebook 体积，大陆网络也可离线使用。

---

## 样本标准差动态演示

**文件：** [`std-dev-demo.html`](std-dev-demo.html)

**配套章节：** `notebooks/phase2_intro/01_理解波动率.ipynb` · 5.4 节

**打开方式：**

1. 在 Notebook 公式下方点击链接跳转；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\std-dev-demo.html
   ```

**功能：**

- 动态演示样本标准差公式：$\sigma = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(r_i-\bar{r})^2}$
- **251 个交易日收益率**（约一年），与日收益率演示同源
- 逐步显示当前 $r_i$、均值 $\bar{r}$、偏差平方 $(r_i-\bar{r})^2$ 和累加项
- 同步更新当前样本下的 $\sigma$ 结果（至少 2 个样本后生效）
- 播放 / 暂停 / 单步 / 重置，可调速度

---

## 总体方差动态演示

**文件：** [`population-variance-demo.html`](population-variance-demo.html)

**配套章节：** `notebooks/phase2_intro/01_理解波动率.ipynb` · 总体方差公式 (2-1a)

**打开方式：**

1. 在 Notebook 公式下方点击链接跳转；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\population-variance-demo.html
   ```

**功能：**

- 动态演示总体方差公式：$s^2 = \frac{1}{N}\sum_{j=1}^{N}(x_j-\bar{x})^2$
- **251 个对数收益率** $x_j$（约一年），逐步代入
- 左侧实时显示 $x_j$、$\bar{x}$、$(x_j-\bar{x})^2$、$\Sigma$ 与 **除以 N** 后的 $s^2$
- 强调与样本标准差的区别：**分母是 N，不是 N-1**
- 播放 / 暂停 / 单步 / 重置，可调速度

---

## 方差修正四种公式 · 合一演示

**文件：** [`variance-formulas-demo.html`](variance-formulas-demo.html)

**配套章节：** `notebooks/phase2_intro/01_理解波动率.ipynb` · 「结合收益率分布的方差修正」

**打开方式：**

1. 在 Notebook 各公式下方点击对应链接（带 `#` 锚点直达场景）；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\variance-formulas-demo.html
   ```

**四个场景（同一页面，顶部标签切换）：**

| 锚点 | 公式 | 演示内容 |
|------|------|----------|
| `#2-1b` | $s^2=\frac{1}{N}\sum x_j^2$ | 忽略均值，逐步累加 $x_j^2$ |
| `#2-2` | (2-2)(2-3) 无偏估计 | 对比 ÷$N$ 与 ÷$N-1$，验证修正因子 |
| `#jensen` | $E(s)<\sigma$ | 蒙特卡洛展示詹森不等式 |
| `#2-4` | $f_N(s)$ | 调节 $N$ 观察样本标准差 PDF 形态 |

- 251 个对数收益率样本（场景 1、2）；播放 / 暂停 / 单步 / 重置

---

## 夏普比率动态演示

**文件：** [`sharpe-ratio-demo.html`](sharpe-ratio-demo.html)

**配套章节：** `notebooks/phase2_intro/02_夏普比率与Beta.ipynb` · 6.1 节

**打开方式：**

1. 在 Notebook 公式下方点击链接跳转；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\sharpe-ratio-demo.html
   ```

**功能：**

- 动态演示：$\text{Sharpe} \approx \dfrac{\text{年化收益} - r_f}{\text{年化波动率}}$（$r_f=4\%$）
- **10 只美股**（AkShare 日线 · 最近 **300** 个交易日），顶部可切换标的
- 逐步出现日收益，实时更新年化收益、年化波动、超额收益与 Sharpe
- 播放 / 暂停 / 单步 / 重置，可调速度

---

## Beta 动态演示

**文件：** [`beta-demo.html`](beta-demo.html)

**配套章节：** `notebooks/phase2_intro/02_夏普比率与Beta.ipynb` · 6.3 节

**打开方式：**

1. 在 Notebook 公式下方点击链接跳转；或
2. 双击 HTML 文件；或
   ```bash
   start assets\interactive\beta-demo.html
   ```

**功能：**

- 动态演示：$\beta = \dfrac{\text{Cov}(R_{\text{股}}, R_{\text{市}})}{\text{Var}(R_{\text{市}})}$
- **9 只个股** vs **SPY** 大盘（AkShare · 300 交易日），顶部切换标的
- 上图：个股与 SPY 日收益；下图：β 演化（含 β=1 参考线）
- 左侧实时显示 Cov、Var、β 代入过程
- 播放 / 暂停 / 单步 / 重置，可调速度
