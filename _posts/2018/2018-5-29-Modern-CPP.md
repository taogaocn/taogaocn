---
layout: post
category: "learn"
title:  "C++学习笔记"
tags: [C, C++, 程序设计]
---

本文收集整理C++学习过程中的一些关键问题，未特殊说明的情况下，本文指C++11
版本。

### 基本语言

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

### 一、类型推断
#### 1. 模板类型推断
* 类型推断中引用类型被忽略
* 当推断右值引用的类型时，左值参数推断为左值
* 传值的函数参数，其const和volatile限定符被忽略
* 数组和函数名称通常被推断为指针，除非他们被初始化为引用

#### 2. auto类型推断
* auto类型推断和模板类型推断一致（除了auto类型推断假定以{}初始化
的类型为std::initializer_list<T>）
* [C++14] auto作为函数返回值或lambda参数采用模板类型推断

#### 3. decltype类型推断
* decltype几乎总是返回变量或表达式的类型
* 对于T类型的左值表达式，decltype返回T&类型
* [C++14] 支持decltype(auto)，在这种形式下采用decltype类型推断决定auto的类型

#### 4. 查看推断的类型
* 查看方法：IDE、编译错误(template<typename T> class TD)、标准库typeid(x).name
以及Boost TypeIndex库。
* 有些方法的获得的推断类型可能不准确，因此记住推断规则仍然有意义。

### 二、auto

#### 5. 优先使用auto类型声明

* auto类型必须被初始化，通常可以免除由于类型不匹配导致的移植性和效率问题，简化
重构的过程，减少需要的输入。
* auto类型受到第2项和第6项规则的支配。

#### 6. 当auto类型推断出非需要的类型时使用显式类型初始化器

* "不可见"的代理类型可能导致auto推断出错误的类型
* 通过显式的类型转换使得auto推断出需要的类型static_cast<type>()

### 三、移植到现代C++

#### 7. 在创建对象时区分()和{}

* 大括号初始化（{}）是最常用的初始化语法（可以避免一些错误）
* 在构造重载中，大括号初始化可能的情况下优先匹配std::initializer_list参数，
即使其它构造函数提供更好的匹配
* 两种初始化方式（{}和()）不同的一个示例是用两个参数构造std::vector
* 在模板内部选择不同初始化方式可能比较具有挑战性

#### 8. 优先使用nullptr

* 尽量使用nullptr而不是0和NULL
* 避免重载整数和指针类型

### 参考书籍
* Effective Modern C++
