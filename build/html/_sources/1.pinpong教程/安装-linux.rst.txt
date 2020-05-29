==================
Linux 平台安装
==================

.. glossary::

   Linux 

1、终端中输入sudo pip install pinpong即可安装。  


.. code-block:: bash

        $ sudo pip install pinpong


.. image::  ../images/linux_install1.png

2、找到python库的路径，最简单的方式，运行python3, import pinpong, 通过print(pinpong.__path__)打印出pinpong库的路径。


.. code-block:: python

        import pinpong
        print(pinpong.__path__)


.. image::  ../images/linux_install4.png

3、更改路径至pinpong的目录下的example中，可以看到示例程序都在这个文件夹。

.. image::  ../images/linux_install5.png

