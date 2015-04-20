# Hg工作仓库权限管理 #

参考:
  * [如何组织在线图书工程](http://code.google.com/p/openbookproject/wiki/HowToBuildBookOnline)
    * [基于Sphinx的图书协同](http://code.google.com/p/openbookproject/wiki/FlowSphinx#%E6%B5%81%E7%A8%8B)
  * [理解配置管理](http://code.google.com/p/kcpycamp/wiki/HowtoScm)
  * [了解分布式版本管理系统](http://code.google.com/p/kcpycamp/wiki/AbtDvcs)
    * [Hg基础使用](http://code.google.com/p/kcpycamp/wiki/HgUsage)
    * [Hg简单協作](http://code.google.com/p/kcpycamp/wiki/HgFlows)

## 操作简述 ##
推荐使用 bitbucket.org 支持的简单分支仓库及权限控制:

  * 任何人,随时可以克隆一个分支仓库,成为私人工作仓库,开展翻译:
    * 但是,要想将贡献纳入正式发布仓库中,必须 发起[合并申请](http://confluence.atlassian.com/display/BITBUCKET/Accepting+a+Pull+Request+for+a+Bitbucket+Repository)
  * 在获得团队认可并绑定正式发布仓库写权限后,就可以直接将成果推送进来了

注意::
> - 不论是否要和其它人協同,对远程仓库进行版本操作时,一定要坚守以下流程:
    1. 检入本地变更: `hg ci -m "更新日志"`
    1. 下拉远程变更: `hg pull -u`
    1. 解决可能冲突,并再次检入
    1. 推送远程仓库: `hg push`

提示::
```
# 在配置文件 .hgrc 中打开图形化日志插件
[extensions]
graphlog =
[alias] 
ll = glog --style compact
```
![http://the-art-of-community-chinese-translation.googlecode.com/files/zq_2011-10-18-144635_779x480_scrot.png](http://the-art-of-community-chinese-translation.googlecode.com/files/zq_2011-10-18-144635_779x480_scrot.png)

  * 就可以非常直观的看到分支情景,有利于判定合并什么...