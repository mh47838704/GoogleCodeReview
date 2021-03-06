# 术语
* 作者：代码提交的人
* CR/cr：code review 代码检视
* 代码owner：目前负责管理代码的人
* 检视者/代码reviewer：cr代码的人
* 变更(CL)：change list，代表一次代码合并请求
# cr的标准
cr的主要目的是保证google代码库的代码健康度随着时间的增长而得到提升，所有的cr的工具和流程都是为了这个目的而设计的

为了达到这样的目的，有一系列的折中和平衡需要考虑

首先开发者必须要保证他们所做的事情有进步有改进。如果从来没有向代码库提交一个改进，那么这个代码库永远不会被改进。
同理，如果说代码检视的人让任何变更提交代码库很困难，那么开发人员就没有动力在将来进行改进了。

另外一方面，代码检视的需要保证每一次的变更的质量，使得整个代码库的健康度不会随着时间的推移而下降。这个问题和棘手，
因为，通常代码库的健康度的下降都是由于许多次低质量代码变更影响的，特别是一些团队在一个时间很紧迫的情况下，
他们认为为了完成目标不得不采取一些更加快捷的方式。

同样，作为代码检视的人对他们所检视的代码拥有所有权和责任，他们想要保证代码库的稳定性、可维护性以及其他所有在"cr要点"中提及的。

所以，我们总结出如下规则作为cr的标准：
"总的来说，如果一次变更能提高整体代码库的质量，即使这个变更不完美，也是可以通过的"，这是cr指导的最高准则，当然也有许多限制。
比如说，如果一次变更添加了本次系统不需要的特性，即使这个特性设计良好，那么代码检视的人也可以拒绝掉

一个关键的要点是"没有完美的代码，只有更好的代码"，代码检视者不应该要求代码的开发者把变更中每一部分的代码都打造的非常完善才能提交。
代码检视的人应该权衡改进本身的重要性以及改进的成本。作为代码检视人应该追求的是持续的提神，而不是追求完美。
一次代码变更总的来说能提升系统的维护性、可读性以及可理解性，那么这次变更不应该由于其不完美而被延迟数天或者甚至一周才通过。

代码检视的人可以随意表达一些可以改进的建议（这个建议不是特别重要的），通过在建议前面加上Nit（not important）的前缀。
这样可以让变更提交的人知道，这仅仅是一个优化改进的建议，他们可以选择忽略。

注意：没有任何事情可以证明变更的提交一定会使得系统的健康度下降，只有可能在一些紧急变更的情况下发生。

# 辅助
cr有一个很重要的功能是帮助那些才学习语言、框架、软件设计的开发者，因为每一次cr的人留下的评论都能让他们学习到新的东西。
分享知识也是提升代码库质量的一部分。需要记住的是，如果你的评论只是纯粹的学习建议，而不是本片文章中描述的致命的标准问题，
那么建议在评论前面加上"Nit"，或者是指明一下这个评论不是强制代码开发者需要解决的

# 原则
* 技术事实和技术数据大于个人偏好和意见
* 关于编码规范问题，编码规范是绝对权威，任何没有在编码规范的规范都是纯粹的个人偏好，风格应该与现在的保持一致。如果该风格没有先例，那么就接受开发者的
* 软件设计的各个方面从来不是一个风格问题或者是个人偏好，它们基于一些基本的原则并应该在这些原则之间做一些权衡，而不是简单的个人观点。
当然有时候也有一些有效的观点。如果观点的提出人能证明（可以通过一些数据或者一些坚实的工程规则）这些观点方案是有效的，那么作为检视的人应该接受提出人的偏好。
否则是否选择接受应该取决于软件设计的基本原则
* 如果没有其他的规则可遵循，那么检视的人可以要求本次变更的编码风格和现有代码库中的风格保持一致，前提是不能影响整个代码库的健康度

# 解决冲突
在cr过程中的任何冲突，首要的始终应该是开发人员和检视人员试图达成一致，基于本篇的内容以及其他其他文档内容在《The CL Author’s Guide——变更提交者指南》 and this 《Reviewer Guide——检视者指南》.

如果很难达成一致，那么开发者和检视人员应该面对面的或者视频交流，而不只是通过代码审查评论来解决冲突，（如果使用面对面或者视频会议的方式，那么请将讨论的结果积累在cr的评论中，以供将来的读者参考）

如果通过上述的方法仍然无法解决冲突，最常用的方法就是把该问题往上升级，通常升级的方式是让团队参与讨论，并应该有一名技术领导在，并询问代码owner的的决定
，或者是寻求工程经理的帮助。但是一定不要因为无法达成一致而导致变更驻留无法提交

[下一节：在cr过程中需要关注哪些点](https://github.com/mh47838704/GoogleCodeReview/blob/master/review/looking-for.md)