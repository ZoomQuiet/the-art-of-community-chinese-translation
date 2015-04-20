

# 概述 #
说明如何参与 "[TAoC~社区的艺术](Introduction.md) 图书翻译工程";
简述整体过程，详细指引如何获得相关资源,和技能加入分布式協作团队来完成翻译;

## 资源关系 ##

![http://wiki.the-art-of-community-chinese-translation.googlecode.com/hg/fig/mapOBPres.png](http://wiki.the-art-of-community-chinese-translation.googlecode.com/hg/fig/mapOBPres.png)

  * 交流[列表](http://groups.google.com/group/taoc-chinese-translation/)
  * 工程[管理](https://code.google.com/p/the-art-of-community-chinese-translation/)
  * 版本[仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh/)
  * 自动[发布](http://taoc-zh.readthedocs.org/)<sup>查阅</sup>

## 加入流程 ##
简要的约定加入以及图书撰写流程:
  * `自愿是第一要求，认真是第二要求，坚持是第三要求`

### 条件 ###

  1. 原始条件是有 [taoc-chinese-translation](http://groups.google.com/group/taoc-chinese-translation/)发言权
  1. 基本条件是有 [工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh/) 的权限
  1. 顶级条件是有 [知识仓库](https://code.google.com/p/the-art-of-community-chinese-translation.wiki/) 的权限

### 过程 ###
**任何人** 只要认同 "[TAoC~社区的艺术](Introduction.md) 图书翻译工程" 的意义,不论任何知识/管理/技术经验,
都可以随时加入!

详细步骤如下:
  1. 订阅[列表](http://groups.google.com/group/taoc-chinese-translation/),通过 taoc-chinese-translation@googlegroups.com 和团队成员交流
    * 参考: http://code.google.com/p/kcpycamp/wiki/HowtoDiscuss
  1. 注册 https://bitbucket.org 并 克隆 [工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh)
    * 参考: http://code.google.com/p/kcpycamp/wiki/HgUsage
    * 具体操作: `hg clone https://bitbucket.org/ZoomQuiet/the-art-of-community-zh`
  1. 尝试进行翻译,并在本地进行编译测试效果,最终将翻译样章,推送到你的工作仓库中
    * 参考: http://code.google.com/p/pymotwcn/wiki/SphinxprojectHowto
    * 本地安装好 Python+Sphinx 后:
      * 编译出本地的HTML图书站: `make html`
    * 检入翻译成果到本地仓库: `hg ci -m "ch** 章节,翻译进展, 作为提交日志"`
    * 推送翻译成果到远端仓库: `hg push`
    * 向 [工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh) 发起[合并申请](http://confluence.atlassian.com/display/BITBUCKET/Accepting+a+Pull+Request+for+a+Bitbucket+Repository),以便正式成员评估翻译成果
  1. 在主持人,或是其它成员,认可翻译成果后,将
    1. 接受合并申请,将你的翻译成果,从你的克隆仓库中合并到[工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh)中
    1. 进一步的,开放[工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh)的权限给你,这样你就可以重新克隆 [工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh) 到本地,直接将翻译成果推送到 [工作仓库](https://bitbucket.org/ZoomQuiet/the-art-of-community-zh) 中,第一时间被所有成员知道!
  1. 接下来,就可以分配[知识仓库](https://code.google.com/p/the-art-of-community-chinese-translation.wiki/)的权限
    * 作为正式成员
    * 持续更新[进展日志](https://code.google.com/p/the-art-of-community-chinese-translation/wiki/TaocZhLog)


#### 注意 ####
```前述第三步```,不能直接从本地的仓库克隆向主仓库进行更新推送;

  * 这是确保以后来的人多了,不至于产生推送时的版本混乱,进行的分布式協同:
    * Hg 支持自由的仓库克隆,任何人可以随时建立目标仓库的私人克隆
    * http://bitbucket.org/ZoomQuiet/the-art-of-community-zh
    * 点击 frok
    * 你将获得
```
    http://bitbucket.org/[你的帐号名]/the-art-of-community-zh/overview
```
      * 这个完全属于你全权控制的仓库
      * 你可以任意操作
      * 也同样可以邀请朋友来联合翻译...
    * 但是, docspy3zh.readthedocs.org 的自动化统一预览发布,只能绑定
> > http://bitbucket.org/ZoomQuiet/the-art-of-community-zh
    * 所以,你的翻译贡献想为社区使用,就得通过仓库间的合并得以实现
      * 具体作法就是提出 变更申请
      * 参考: [合并申请](http://confluence.atlassian.com/display/BITBUCKET/Accepting+a+Pull+Request+for+a+Bitbucket+Repository)
      * 在你的仓库界面中点击 "Send pull request"
      * 填写合并申请说明
    * 主仓库的管理员们就收到了推送申请
      * 进行评审后,
      * 由主仓库进行 Update pull request ~ 拉合并操作
      * 就正式从你的私人仓库,接收到了翻译变更


## TODO ##
  * 综述当前组织团队
  * 简化资源权限获取过程


