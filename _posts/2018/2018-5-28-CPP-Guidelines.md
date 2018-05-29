---
layout: post
category: "learn"
title:  "C/C++编码规范"
tags: [C, C++, 程序设计]
---

本文收集整理C和C++语言的编程规范，用于个人编码时参考查阅。

### 一、指导原则

### 二、基础

#### 1. 缩进

每级缩进4个字符，通常每列不超过80个字符。

#### 2. 断行

断行符只应用于宏定义，通常以操作符为首进行断行，并匹配其级别。

```
AVeryLongVariableOne = AVeryLongVariableTwo + AVeryLongVariableThree;

// 正确
AVeryLongVariableOne
    = AVeryLongVariableTwo + AVeryLongVariableThree;

// 正确
AVeryLongVariableOne = AVeryLongVariableTwo
                       + AVeryLongVariableThree;

// 错误，以字符结尾
AVeryLongVariableOne = AVeryLongVariableTwo +
                       AVeryLongVariableThree;
if (Condition1 && Condition2) {}

// 正确
if (Condition1
    && Condition2){}

// 错误，级别不匹配
if (Condition1
   && Condition2) {}

// 错误，以操作符结尾
if (Condition1 &&
    Condition2) {}
```

#### 3. 空格
除括号之外，标识符、关键字、标点符号间应该用一个空格隔开。

#### 4. 命名
* 名字应自我解释其作用
* 命名模式应该在项目中一致
* 全大写的命名应该只用于宏、常量和枚举类型
* 变量名不应该以下划线开头
* 类或结构体的成员变量可以以下划线结尾

#### 5. 子句
子句应该以新行开始。

```
// 正确
if (condition) {
        ...
}
else {
        ...
}

// 错误
if (condition) {
        ...
} else {
        ...
}
```

### 三、标准库的使用
#### 1. 标准库使用基本原则
* 尽量使用库
* 尽量使用标准库
* 不要添加组件到std名字空间
* 利用类型安全的方式使用标准库

#### 2. 容器
* 尽量使用STL的array和vector替代C风格的array
* 尽量使用STL的vector容器，除非有足够的理由使用其它容器
* 注意边界检查

#### 3. 字符串
* 

### 相关链接
* [Awesome C++](https://github.com/fffaraz/awesome-cpp)
* [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md)
