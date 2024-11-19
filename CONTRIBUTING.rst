贡献给 CMake
*********************

以下总结了贡献更改的过程。
更多信息请查看 `CMake 开发`_ 文档。

.. _`CMake 开发`: Help/dev/README.rst

社区
=========

CMake 由 `Kitware`_ 维护和支持，并与一群富有成效的贡献者社区合作开发。
请在 `CMake 论坛`_ 的 ``Development`` 类别中发帖，以提出开发话题的讨论。

.. _`Kitware`: https://www.kitware.com/cmake
.. _`CMake 论坛`: https://discourse.cmake.org

补丁
=======

CMake 使用 `Kitware 的 GitLab 实例`_ 来管理开发和代码审查。
要贡献补丁：

#. 将上游的 `CMake 仓库`_ 复制到个人账户。
#. 运行 `Utilities/SetupForDevelopment.sh`_ 进行本地 git 配置。
#. 查看 `构建 CMake`_ 了解如何在本地构建 CMake。
#. 查阅 `CMake 源代码指南`_ 了解编码指南和 `CMake 测试指南`_ 了解测试指南。
#. 创建一个适合您工作的专题分支。
   所有新工作都基于上游的 ``master`` 分支。
   只有在修复该版本中新功能的问题或回归时，才基于上游的 ``release`` 分支工作。
   如果有疑问，请优先选择 ``master``。在特定情况下，审查者可能简单地要求重新基线。
#. 创建提交，使增量、独特、逻辑完整的更改具有适当的 `提交消息`_。
#. 将专题分支推送到个人在 GitLab 上的仓库分支。
#. 创建一个 GitLab 合并请求，目标是上游的 ``master`` 分支（即使更改旨在合并到 ``release`` 分支）。
   勾选标有 "Allow commits from members who can merge to the target branch" 的复选框。
   这将允许维护者代表您进行小的编辑。

合并请求将进入 `CMake 审查流程`_ 以供考虑。

.. _`Kitware 的 GitLab 实例`: https://gitlab.kitware.com
.. _`CMake 仓库`: https://gitlab.kitware.com/cmake/cmake
.. _`Utilities/SetupForDevelopment.sh`: Utilities/SetupForDevelopment.sh
.. _`构建 CMake`: README.rst#building-cmake
.. _`CMake 源代码指南`: Help/dev/source.rst
.. _`CMake 测试指南`: Help/dev/testing.rst
.. _`提交消息`: Help/dev/review.rst#commit-messages
.. _`CMake 审查流程`: Help/dev/review.rst

CMake Dashboard 客户端
======================

`CMake 审查流程`_ 的 *集成测试* 步骤使用一组测试机器，这些机器按照自己的时间表跟踪集成分支，以推动测试并将结果提交到 `CMake CDash 页面`_。
任何人都可以提供测试机器，以帮助保持对其平台的支持。

更多信息请查看 `CMake 集成测试`_ 文档。

.. _`CMake CDash 页面`: https://open.cdash.org/index.php?project=CMake
.. _`CMake 集成测试`: Help/dev/integration-testing.rst

许可证
=======

我们不要求任何正式的版权转让或许可协议。
任何故意向上游发送的贡献都被认为是在 OSI 批准的 BSD 3-clause 许可证的条款下提供的。
详情请参阅 `Copyright.txt`_。

.. _`Copyright.txt`: Copyright.txt