---
layout: page
title: SparkSource Quality
description: SparkSource software quality follows high standards.
---

软件的质量常常决定着产品的命运。质量差劲的软件纵然有着华丽的功能也无法让客户和
用户满意，而且后期修复缺陷的投入往往是前期完善设计的数十倍，甚至最终导致灾难性的后
果，比如波音 737 MAX 系列客机就是因为软件缺陷造成空难，并被全面停飞。反过来，
GNU GCC 虽然没有易用的图形界面，但是它作为一款基础性软件工具非常注重设计的严谨
性和代码的健壮性。每次发布，GNU GCC 都会跑海量测试用例，回归覆盖非常精细的使用
场景，而且作为一款编译器，GNU GCC 的自我编译也非常严格。正是因为有这样的测试，
GNU GCC 一直是编译工具中的标杆产品。

SparkSource 开发团队多年服务于对软件质量有着高要求的关键任务工程领域。他们在
SparkSource 的产品设计之初就全面制定了软件质量要求，无论是代码风格、单元测试、
接口测试，还是集成测试，乃至最后的用户问题跟踪，我们都遵循行业领先的准则。

今天，我们就来看看 SparkSource 在静态代码检查方面的出色表现。SparkSource 的
代码几乎全部都是用 C++ 语言写成的，而 C++ 语言有多种复杂的功能，如果稍有疏忽
就会引入难以发现的代码质量问题。SparkSource 对代码编译的要求一直是零警告——
这是一个看似容易，但是对 SparkSource 这样的大型软件系统比较挑战，需要对每行
代码认真分析、仔细设计。

对于每次代码提交，除了编译零警告，我们还引入以著名自由软件 CPPCHECK 为中心的
静态代码检查——标准也是零警告。CPPCHECK 是一款专注于检查代码缺陷的自由软件。
它可以检查 C++ 代码的合规性，避免未定以行为。它可以检查代码的安全性，避免多种
安全漏洞。它还可以检查代码针对 cert、MISRA 等行业标准的规范性。在这些检测中
SparkSource 一直保持着零风险。

除了静态代码检查的高标准，Sparksource 的使用测试也通过设计形成自我闭环。因
为 SparkSource 的三大核心模块：
SparkEngine
SparkStudio
SparkPlayer
能够互相测试——SparkStudio 和 SparkPlayer 都是由 SparkEngine 开发和驱动，
SparkStudio 的使用就是对 SparkEngine 的测试，SparkPlayer 的运行和使用就是
对 SparkStudio 的测试。这就保证我们在工具开发中就完成了大量的核心代码测试
和验证。

当然，这些只是最基本的测试。SparkSource 还要经历更多、更全面、更严格的测试。
为其如此，它才能作为一款人机界面的通用型基础设计和开发工具，在多个关键任务
的行业应用中受到众多客户的喜爱。
