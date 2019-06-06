# 组合模式

## 问题

- 用户想表示对象的部分-整体层次结构。
- 并希望忽略组合对象与单个对象的不同，统一地使用组合结构中的所有对象。
- 描述了**如何将容器对象和叶子对象进行递归组合**，使得**用户在使用时无须对它们进行区分**，可以**一致地对待容器对象和叶子对象**。

## 详解

### 组合模式

- 又叫做“**整体-部分模式**”。
- 它使树型结构的问题中，**模糊了简单元素和复杂元素的概念**，客户程序可以像处理简单元素一样来处理复杂元素,从而使得客户程序与复杂元素的内部结构**解耦**。

![compositedetail](../../images/composite/compositedetail.png)

### 三种角色

- **抽象组件类(Component)**：组合中的对象声明接口，实现所有类共有接口的行为。声明用于访问和管理Component的子部件的接口。
- **叶子节点(Leaf)**：叶节点对象，叶节点没有子节点。由于叶节点不能增加分支和树叶，所以叶节点的Add和Remove没有实际意义。
- **组件集合类(Composite)**：实现Componet的相关操作，比如Add和Remove操作。其中包含Component 的容器，用来存储叶节点集合，有叶节点行为，用来存储叶节点集合。

## 实现步骤

### 一、定义抽象组件接口

![compositestep1](../../images/composite/compositestep1.png)

### 二、实现叶子节点类，实现抽象组件类的接口

![compositestep2](../../images/composite/compositestep2.png)

### 三、实现组件集合类，实现抽象组件类的接口

![compositestep3](../../images/composite/compositestep3.png)

### 四、定义环境类，将叶子节点和组件集合加入根组件集合

![compositestep4](../../images/composite/compositestep4.png)

