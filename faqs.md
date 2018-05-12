---
layout: page
title: "备忘"
---

### 五级工程师

著名前苏联物理学家朗道曾经给出过一个五级物理学家的划分，吴军老师在此基础上，
给出了“五级工程师”的划分：

* 第五级： 能独立解决问题，完成工程工作。
* 第四级： 能知道和带领其他人一同完成更有影响力的工作。
* 第三级： 能独立设计和实现产品，并且在市场上获得成功。
* 第二级： 能设计与实现别人不能做出的产品，也就是说他的作用很难取代。
* 第一级： 开创一个产业。

### 高效能人士的七个习惯

个人领域的成功：从依赖到独立

* 积极主动 个人愿景的原则
* 以终为始 自我领导的原则
* 要事第一 自我管理的原则

公众领域的成功：从独立到互赖

* 双赢思维 人际领导的原则
* 知彼解己 同理心交流的原则 
* 统合综效 创造性合作的原则 
* 不断更新 平衡的自我更新原则 

### 常用的Git命令与工作流程

#### Gihub工作流程
```
# 1.fork项目到自己帐号下
# 2.clone项目到本地
git clone git@github.com:me/em.git
# 3.查看分支
git branch
git branch -a
# 4. 根据远端分支创建本地分支
git checkout -b dev origin/dev
# 5. 添加团队仓库
git remote -v
git remote add upstream 团队项目地址
# 6. 和上游仓库同步
git fetch upstream
git merge upstream/dev
or
git fetch upstream/dev
git rebase upstream/dev
or
git pull --rebase upstream/dev
# 7. 本地修改并push到远端
git push origin HEAD:dev
# 8. 向团队仓库发送pull request
# 9. 团队负责人review并接收pull request
```

#### Git rebase vs merge
* 当你从remote去pull的时候，永远使用rebase （保留commit历史）
* 当你完成了一个功能后打算合并到主干分支的时候，永远使用merge
  （丢弃功能开发历史）

### 常用的Linux命令
* 查看占用端口号的服务：netstat -nlp
