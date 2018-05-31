---
layout: post
category: "learn"
title:  "C++学习笔记"
tags: [C, C++, 程序设计]
---

本文收集整理C++学习过程中的一些关键问题，未特殊说明的情况下，本文指C++11
版本。

### 一、基本语言

#### 1. const限定符
* 定义常量：`const int a = 7`
* 指针
  * 内容不可变：`const int* p = &a`
  * 指针不可变：`int* const p = &a`
  * 都不可变: `const int* const p = &a`
* 引用：`const int &rval = ival`
* 函数
  * const指针参数: `void test(int *const a)`
  * const引用参数：`void test(const int& a)`
  * const成员函数：`void func() const`

#### 2. 左值(lvalue)与右值(rvalue)
* 定义：概括的讲，凡是能够取地址的可以称之为左值，反之称之为右值。
* 引用：对应的引用分别为左值引用(T &)和右值引用(T &&)
* std::move：把左值转换成由右值引用
* std::forward: 按照原来的类型转发
* 引用折叠规则(前者为接受类型，后者为进入类型，=>表示引用折叠后的类型)：
```
T& + & => T&
T&& + & => T&
T& + && => T&
T&& + && => T&&
```

### 二、类型推断
#### 1. 模板类型推断
* 类型推断中引用类型被忽略
* 当推断右值引用的类型时，左值参数推断为左值
* 传值的函数参数，其const和volatile限定符被忽略
* 数组和函数名称通常被推断为指针，除非他们被初始化为引用