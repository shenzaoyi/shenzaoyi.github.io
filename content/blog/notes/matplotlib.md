---
title: matplotlib
categories:
  - blog
contributors:
  - shenzaoyi
date: 2024-09-07
draft: false
---
## 核心内容和逻辑
1. Axis 单个数轴
2. Axes 坐标系
3. Figure 整个画面
4. Artist 画面中所有东西
![[9ff586fa31ccd5a71ddaf07b40f4bbef.jpg]]
### matlab语法
```python
seasons = [1,2,3,4,5]
stock1 = [3,4,2,5,7]
plt.figure(figsize=(9,3))
plt.subplot(211)
plt.bar(seasons,stock1)
plt.subplot(212)
plt.plot(seasons,stock1,"b^--")
plt.show()
```
### 面向对象语法
```python
    seasons = [1,2,3,4,5]
    stock1 = [3,4,2,5,7]
    fig, axes = plt.subplots(2,1)
    axes[0].bar(seasons,stock1)
    axes[1].plot(seasons,stock1)
    plt.show()
```

### 布局
```python
fig = plt.figure() # 初始化
ax = plt.subplot() # 初始化一个坐标系
ax = fig.add_subplot() # 初始化并添加一个坐标系
fig.add_gridspec() # 添加网格辅助定位
fg, ax = plt.subplot(m,n) # m行n列坐标系

# 定制
plt.figure(参数...)
- figsize(m,n) # m 英尺 n 英寸
plt.subplots(参数...)
- subplot_kw='projection': 'polar' 
```

### 动画(Animation)
