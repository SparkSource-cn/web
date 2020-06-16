# -*- mode:org; coding: utf-8 -*-

#+TITLE:     SparkSource 优雅处理高端仪表应用界面
#+AUTHOR:    Wensheng Xie
#+EMAIL:     wxie@member.fsf.org
#+LANGUAGE:  zh
#+OPTIONS: H:2 num:nil toc:nil \n:nil @:t ::t |:t ^:{} _:{} *:t TeX:t LaTeX:t
#+STYLE: <link rel="stylesheet" type="text/css" href="org.css" />
#+LATEX_CLASS: myclass
#+LATEX_CLASS_OPTIONS: [a4paper]
#+ATTR_LATEX: width=0.38\textwidth wrap placement={r}{0.4\textwidth}
#+ATTR_LATEX: :float multicolumn
#+REVEAL_TRANS: None
#+REVEAL_THEME: Black
#+TAGS: @work(w) @home(h) @road(r) laptop(l) pc(p) { @read : @read_book @read_ebook }
#+ATTR_ORG: :width 30 
#+ATTR_HTML: width="100px"
#+EXPORT_SELECT_TAGS: export
#+EXPORT_EXCLUDE_TAGS: noexport
#+STARTUP: fold

随着汽车电子的不断发展和人们需求的日益增多，车内仪表的功能也越来越复杂，其应用界面也越来越亮
丽多变。高端仪表应用不仅提供传统仪表带有的转速和车速信息，也为驾驶者展示更为丰富的车内、车外
信息，比如，车道信息和其他车辆的距离信息。这些信息的展现方式对驾驶者的操控判断和车内乘客的安
全都有关键的作用。

智能驾舱的概念近年来也炙手可热，它其中的一个重要特点就是仪表信息和娱乐信息互通。智能驾舱的一
个典型应用就是仪表导航显示——在驾驶者容易观察的仪表上显示导航地图和导航提示信息。

更进一步，虚拟现实——在仪表上显示虚拟的物体，如车内电子宠物——也开始纳入日益发展的车内应用
开发的日程。增强现实——在仪表上显示比实际更丰富的内容，比如和前车的距离——会让驾驶者能够有
更确切的信息做判断。

过去，这些高级应用的人机界面的设计和开发都需要投入较大的人力。现在 SparkSource 在基础架构
上自然支持车内多来源信息交互，展现方式又可以灵活定制；而其高效的图形处理引擎能够保证画面的
实时性和流畅度。一款基于 SparkSource 的高级仪表应用界面只需经过设计这一个环节就可以进行实
车验证，在缩短开发周期的同时也大大降低人力需求。

下面的视频就是 SparkSource 从沟通客户需求到实机展示总共投入1个人月的结果。
1. 带有虚拟现实效果的仪表
