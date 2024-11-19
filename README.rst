CMake
*****

介绍
============

CMake 是一个跨平台的开源构建系统生成器。
完整文档请访问 `CMake 首页`_ 和 `CMake 文档页面`_。`CMake 社区维基`_ 也提供了有用的指南和配方。

.. _`CMake 首页`: https://cmake.org 
.. _`CMake 文档页面`: https://cmake.org/documentation 
.. _`CMake 社区维基`: https://gitlab.kitware.com/cmake/community/-/wikis/home 

CMake 由 `Kitware`_ 维护和支持，并与一群富有成效的贡献者社区合作开发。

.. _`Kitware`: https://www.kitware.com/cmake 

许可证
=======

CMake 在 OSI 批准的 BSD 3-条款许可证下发布。
详情请参阅 `Copyright.txt`_。

.. _`Copyright.txt`: Copyright.txt

构建 CMake
==============

支持的平台
-------------------

* 微软 Windows
* 苹果 macOS
* Linux
* FreeBSD
* OpenBSD
* Solaris
* AIX

其他类 UNIX 操作系统也可能直接支持，如果不可以
移植 CMake 到该平台也不应该是一个大问题。
请在 `CMake 论坛`_ 发帖询问其他人是否有
关于该平台的经验。

.. _`CMake 论坛`: https://discourse.cmake.org 

使用 CMake 构建 CMake
-------------------------

你可以像构建任何其他基于 CMake 的项目一样构建 CMake：
使用已安装的 CMake 在这个源代码树上运行，使用您喜欢的
生成器和选项。然后构建并安装它。

要构建文档，请安装 `Sphinx`_ 并使用
``-DSPHINX_HTML=ON`` 和/或 ``-DSPHINX_MAN=ON`` 配置 CMake 以启用 "html" 或
"man" 构建器。如果工具未自动找到，添加 ``-DSPHINX_EXECUTABLE=/path/to/sphinx-build``。

构建完成后，在 CMake 构建目录中运行 ``ctest`` 来运行测试套件。
详情请参阅 `CMake 测试指南`_。

.. _`Sphinx`: https://sphinx-doc.org 
.. _`CMake 测试指南`: Help/dev/testing.rst

从零开始构建 CMake
---------------------------


UNIX/Mac OSX/MinGW/MSYS/Cygwin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

您需要有一个支持 C++11 的 C++ 编译器和 ``make`` 安装。
在 CMake 的源代码目录中运行 ``bootstrap`` 脚本。
您可以使用 ``--help`` 选项查看支持的选项。
您可以使用 ``--prefix=<install_prefix>`` 选项指定 CMake 的自定义
安装目录。成功完成后，
运行 ``make`` 和 ``make install``。

例如，如果您只想从源代码构建并安装 CMake，
可以直接在源代码树中构建::

  $ ./bootstrap && make && sudo make install

或者，如果您计划开发 CMake 或以其他方式运行测试套件，请创建
一个单独的构建树::

  $ mkdir build && cd build
  $ ../bootstrap && make

Windows
^^^^^^^

在 Windows 下构建 CMake 有两种方式：

1. 使用 VS 2015 或更高版本的 MSVC 编译。
   您需要下载并安装 CMake 的二进制版本。您可以从
   `CMake 下载页面`_ 获取这些版本。然后按照上述
   `使用 CMake 构建 CMake`_ 的说明进行。

2. 在 MSYS2 下使用 MinGW 自举。
   下载并安装 `MSYS2`_。然后安装所需的构建工具::

     $ pacman -S --needed git base-devel mingw-w64-x86_64-gcc

   如上所述自举。

.. _`CMake 下载页面`: https://cmake.org/download 
.. _`MSYS2`: https://www.msys2.org/ 

报告错误
==============

如果您发现了一个错误：

1. 如果您有一个补丁，请阅读 `CONTRIBUTING.rst`_ 文档。

2. 否则，请在 `CMake 论坛`_ 发帖询问
   预期和观察到的行为，以确定它是否真的
   是一个错误。

3. 最后，如果上述步骤无法解决问题，请在 `CMake 问题跟踪器`_ 中
   打开一个条目。

.. _`CMake 问题跟踪器`: https://gitlab.kitware.com/cmake/cmake/-/issues 

贡献
============

请参阅 `CONTRIBUTING.rst`_ 了解如何贡献。

.. _`CONTRIBUTING.rst`: CONTRIBUTING.rst
