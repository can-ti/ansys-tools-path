ansys-tools-path
================

|pyansys| |python| |pypi| |GH-CI| |codecov| |MIT| |black|

.. |pyansys| image:: https://img.shields.io/badge/Py-Ansys-ffc107.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAIAAACQkWg2AAABDklEQVQ4jWNgoDfg5mD8vE7q/3bpVyskbW0sMRUwofHD7Dh5OBkZGBgW7/3W2tZpa2tLQEOyOzeEsfumlK2tbVpaGj4N6jIs1lpsDAwMJ278sveMY2BgCA0NFRISwqkhyQ1q/Nyd3zg4OBgYGNjZ2ePi4rB5loGBhZnhxTLJ/9ulv26Q4uVk1NXV/f///////69du4Zdg78lx//t0v+3S88rFISInD59GqIH2esIJ8G9O2/XVwhjzpw5EAam1xkkBJn/bJX+v1365hxxuCAfH9+3b9/+////48cPuNehNsS7cDEzMTAwMMzb+Q2u4dOnT2vWrMHu9ZtzxP9vl/69RVpCkBlZ3N7enoDXBwEAAA+YYitOilMVAAAAAElFTkSuQmCC
   :target: https://docs.pyansys.com/
   :alt: PyAnsys

.. |python| image:: https://img.shields.io/pypi/pyversions/ansys-tools-path?logo=pypi
   :target: https://pypi.org/project/ansys-tools-path/
   :alt: Python

.. |pypi| image:: https://img.shields.io/pypi/v/ansys-tools-path.svg?logo=python&logoColor=white
   :target: https://pypi.org/project/ansys-tools-path
   :alt: PyPI

.. |codecov| image:: https://codecov.io/gh/ansys/ansys-tools-path/branch/main/graph/badge.svg
   :target: https://codecov.io/gh/ansys/ansys-tools-path
   :alt: Codecov

.. |GH-CI| image:: https://github.com/ansys/ansys-tools-path/actions/workflows/ci_cd.yml/badge.svg
   :target: https://github.com/ansys/ansys-tools-path/actions/workflows/ci_cd.yml
   :alt: GH-CI

.. |MIT| image:: https://img.shields.io/badge/License-MIT-yellow.svg
   :target: https://opensource.org/licenses/MIT
   :alt: MIT

.. |black| image:: https://img.shields.io/badge/code%20style-black-000000.svg?style=flat
   :target: https://github.com/psf/black
   :alt: Black


一个用于在本地机器中定位 Ansys 产品的库。

.. contribute_start

How to install
--------------

提供了两种安装模式：用户模式和开发者模式。

For users
^^^^^^^^^
**用户模式**

.. howtoinstallusers_start

要安装 ``ansys-tools-path`` ，请确保已安装最新版本的 `pip`_ 。为此，请运行

.. code:: bash

    python -m pip install -U pip

然后，您可以简单地执行：

.. code:: bash

    python -m pip install ansys-tools-path

.. howtoinstallusers_end

For developers
^^^^^^^^^^^^^^
**开发者模式**

在开发者模式下安装 ``ansys-tools-path`` 可以修改源代码并对其进行增强。

在为该项目做出贡献之前，请参考 `PyAnsys Developer's guide`_ 。您需要遵循以下步骤：

#. 首先克隆该版本库：

   .. code:: bash

      git clone https://github.com/ansys/ansys-tools-path

#. 创建一个全新的 Python 环境并激活它：

   .. code:: bash

      # 创建虚拟环境
      python -m venv .venv

      # 在 POSIX 系统中激活
      source .venv/bin/activate

      # 在 Windows CMD 环境中激活
      .venv\Scripts\activate.bat

      # 在 Windows Powershell 中激活
      .venv\Scripts\Activate.ps1

#. 确保拥有最新的所需构建系统、文档、测试和 CI 工具：

   .. code:: bash

      python -m pip install .[tests]
      python -m pip install .[doc]
      python -m pip install .[build]


#. 以可编辑模式安装项目：

   .. code:: bash

      python -m pip install --editable ansys-tools-path


How to testing
--------------
**如何测试**

如果需要，您可以随时从命令行调用样式命令（ `black`_ 、 `isort`_ 、 `flake8`_ ...）或单元测试命令（ `pytest`_ ）。
不过，这并不能保证你的项目是在一个隔离的环境中进行测试的，这也是 `tox`_ 等工具存在的原因。


A note on pre-commit
^^^^^^^^^^^^^^^^^^^^

样式检查利用了 `pre-commit`_ 。我们不强制但鼓励开发人员通过以下方式安装该工具：

.. code:: bash

    python -m pip install pre-commit && pre-commit install


Documentation
-------------

在构建文档时，您可以运行 `Sphinx`_ Makefile 中提供的常规规则，例如：

.. code:: bash

    make -C doc/ html && your_browser_name doc/html/index.html

- ``make -C doc/ html`` ：这个命令在 doc/ 目录下执行 make html 命令。make 是一个构建工具，它根据 Makefile 文件中的规则来构建项目。在这个例子中，make html 通常用于从 reStructuredText 文件生成 HTML 文档。
- ``&&`` ：这是一个 shell 命令连接符，它表示只有当前面的命令成功执行后，才会执行后面的命令。
- ``your_browser_name doc/html/index.html`` ：这个命令会在你的浏览器中打开 doc/html/index.html 文件。你需要将 your_browser_name 替换为你的浏览器的命令行名称，例如 firefox、chrome 等。

Distributing
------------

如果要创建源文件或 wheel  文件，首先要安装 building requirements ，然后执行构建模块：

.. code:: bash

    python -m pip install .[build]
    python -m build
    python -m twine check dist/*


.. LINKS AND REFERENCES
.. _black: https://github.com/psf/black
.. _flake8: https://flake8.pycqa.org/en/latest/
.. _isort: https://github.com/PyCQA/isort
.. _pip: https://pypi.org/project/pip/
.. _pre-commit: https://pre-commit.com/
.. _PyAnsys Developer's guide: https://dev.docs.pyansys.com/
.. _pytest: https://docs.pytest.org/en/stable/
.. _Sphinx: https://www.sphinx-doc.org/en/master/
.. _tox: https://tox.wiki/