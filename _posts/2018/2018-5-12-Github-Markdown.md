---
layout: post
category: "learn"
title:  "Github上Markdown语法"
tags: [Markdown, Github]
---
由于撰写博客的需要，本文将总结Github上Markdown的主要语法，以备参考。

# 1. 标题

* **语法:**
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
* **效果:**
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

# 2. 列表

## (1) 带编号的列表
* **语法:**
```
1. one
2. two
3. three
```
* **效果:**
1. one
2. two
3. three

## (2) 不带编号的列表
* **语法:**

```
* one
* two
* three
- one
- two
- three
  - item 1
  * item 2
```

* **效果:**
* one
* two
* three
- one
- two
- three
  - item 1
  * item 2

# 3. 图片

* **语法:**

```
![Dog](attach/2018/2018-05-12/dog.jpeg)
```

* **效果:**
![Dog](attach/2018/2018-05-12/dog.jpeg)

# 4. 链接

* **语法:**

```
[GitHub](http://github.com)
```

* **效果:**
[GitHub](http://github.com)

# 5. 引用

* **语法:**

```
> We're living the future so
> the present is our past.
```

* **效果:**

> We're living the future so
> the present is our past.

# 6. 代码

* **语法:**

```
`var example = true`
    if (isAwesome){
        return true
    }
```

* **效果:**

`var example = true`

    if (isAwesome){
        return true
    }

# 7. 文本强调

* **语法:**

```
**加粗**__加粗__*斜体*_斜体_
```

* **效果:**

**加粗**
__加粗__
*斜体*
_斜体_

# 8. 任务列表

* **语法:**

```
- [x] 写博客
- [ ] 写代码
```

* **效果:**

- [x] 写博客
- [ ] 写代码
