# BCI学习

## 第一章 引言
### 知识背景
* 基础神经科学✖️
* 大脑信号记录和刺激技术〰️
* 基本的信号处理技术✔️
* 机器学习技术✔️
### BCI处理步骤
![BCI学习](https://github.com/lipervol/BCI_Learning/blob/master/47E8921B-B550-454A-B667-E385478E9072.jpeg)
1. **脑电信号的记录**：采用侵入式和非侵入式记录
2. **信号处理**：**伪迹去除和特征提取**
3. **模式识别和机器学习**
4. **感知反馈**：反馈到大脑
5. **刺激信号处理**：
   **刺激模式**：要求能够达到模拟脑区常见活动，并到达预期效果，需要使用能够产生正确刺激模式的信号处理技术（和潜在的机器学习技术）（？）
7. **脑刺激**：利用侵入式和非侵入式的刺激技术将*从信号处理环节接受到的刺激模式*（？）用于刺激大脑 

## 第二章 神经科学基础
### 神经元（*复杂的电化学设备*）
* 神经元细胞膜由磷脂双分子层构成，这种防渗层种存在**离子通道**，可以选测性的让特定的类型的离子通过
* 膜外钠离子、氯离子、钙离子浓度大，膜内钾离子、*阴离子（通过主动运输）*（？）浓度较大，细胞膜内外约有-70mV的电位差
### 动作电位或峰电位
* 接收到足够强的输入-->Na+快速流入细胞内-->膜电位迅速升高-->K+通道打开-->K+外流出细胞-->膜电位下降
* 膜电位快速上升和下降的现象称为**动作电位或峰电位**（神经元受刺激后膜外正离子*钠离子*流入，膜内从相对于膜外-70mV左右的电位迅速升高到接近膜外电位，之后钠钾泵工作让膜内外恢复电位差）
* 峰电位波形是固定的，本身几乎不携带信息，携带信息的是放电率（每秒钟出现的峰电位的数量）和峰电位出现的时间，因此神经元可以用具有0或1的数字输出模型来表示
* 峰电位常用在其出现时刻的一根短柱条来表示

### 树突和轴突
![神经元](https://github.com/lipervol/BCI_Learning/blob/master/F788CAB9-0EFB-4884-82BD-67E86B120213.png)
* **树突**：与胞体连接的带分支的树形结构
* **轴突**：树突的一个分支，轴突将神经元的输出峰电位传送到其他神经元，峰电位起始于胞体和轴突的连接点附近，沿轴突方向向下传播
* **髓磷脂**：一种白色的髓鞘，覆盖轴突，可以**显著提高峰电位长距离传播的速度**
* **白质**：由连接大脑不同区域的带髓鞘的轴突聚集而成
* **灰质**：由胞体聚集而成

### 突触
![突触](https://github.com/lipervol/BCI_Learning/blob/master/0CF37960-2219-4362-B799-E40C70905708.jpeg)
* 突触本质上是一个神经元（称为突出前神经元）的轴突与另一个神经元（称为突出后神经元）树突（或神经元胞体）的间隙或者裂缝，动作电位到达突触时，前神经元释放神经递质，神经递质作用于后神经元受体上，使离子通道打开，继而影响局部电位
* 突触可以处于兴奋或抑制状态，兴奋性突触使突触后细胞的局部膜电位瞬时上升，这个上升电位称之为**兴奋性突触后电位（EPSP）**，提高后神经元产生峰电位的可能性；于此相反，抑制性突触产生**抑制性突触电位（IPSP）**，可以暂时降低后神经元的局部膜电位
* 一个神经元处于兴奋或抑制，是根据他**形成的突触类型以及突触后神经元**来决定的，**每个神经元只能形成一种突触**，因此一个兴奋性神经元需要抑制另一个神经元，就必须先使一个抑制性的*中间神经元*兴奋，通过它再去抑制目标神经元
* **脑电**被认为是大脑皮层中锥体细胞树突收到刺激后产生的传递到胞体的电位（突触后电位，**不是神经冲动**），这个电位不符合全或无定律，有重叠性质，传输速度慢，存在时间较长。
