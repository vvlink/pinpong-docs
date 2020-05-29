
==================
Mac OS X 平台安装
==================

.. glossary::

    Mac OS X 

   

1、启动用命令行，（打开任意finder窗口，键入Shift+Command+U）, 双击“终端”。
输入命令行，安装pinPong库

.. code-block:: bash

        $ pip install pinpong



.. image::  ../images/2.png

.. image::  ../images/3.png


安装成功后，我们可以到pinpong的目录下，看一下示例代码。


2、找到python库的路径，最简单的方式，运行python, import system, 通过print(sys.path)打印出python库的路径。


3、更改路径至pinpong的目录下，

.. code-block:: bash

        $ cd /..../python3.7/site-packages/pinpong


.. image::  ../images/3.png


4、列出目录下的文件，ls,我们可以看到有个examples文件夹，示例代码就在这个文件夹中。

.. code-block:: bash

    
    $ cd example 
    $ ls



.. image::  ../images/4.png

