
==================
Mac OS X 平台安装
==================

   

1、启动用命令行，（打开任意finder窗口，键入Shift+Command+U）, 双击“终端”。
输入命令行，安装pinPong库

.. code-block:: bash

        $ pip install pinpong



.. image::  images/2.png

.. image::  images/3.png


安装成功后，我们可以到pinpong的目录下，看一下示例代码。


2、找到python库的路径，最简单的方式，运行python, import system, 通过print(sys.path)打印出python库的路径。


3、更改路径至pinpong的目录下，

.. code-block:: bash

        $ cd /..../python3.7/site-packages/pinpong


.. image::  images/3.png


4、列出目录下的文件，ls,我们可以看到有个examples文件夹，示例代码就在这个文件夹中。

.. code-block:: bash

    
    $ cd example 
    $ ls



.. image::  images/4.png


-----------------
快速开始
-----------------


1、启动用命令行，（打开任意finder窗口，键入Shift+Command+U）, 双击“终端”。
        

2、先不连接UNO板，在终端中输入命令行


.. code-block:: bash    
    
        
        $ ls /dev/cu*
        


3、输入命令行后会列出一系列的设备名，然后连接上UNO板，再次输入同样的命令行，比较两次得到的设备，并记录下UNO的设备名称。在这教程中，UNO的设备名称为

::
        /dev/cu.usbmodem144101

.. image::  images/1.png

4、然后我们更改路径至pinpong库样例代码文件夹，

.. code-block:: bash


        $ cd /.../python3.7/site-packages/pinpong



5、以blink.py为例，首先需要编辑blink.py，修改主控板的信息，将示例中leonardo修改为uno, 将com口信息修改为刚才得到的设备名称。





6、blink.py代码样例


.. code-block:: python


    import sys
    import time
    from pinpong.pinpong import *

    LED_PIN = 13

    #board = PinPong("leonardo","com5")
    board = PinPong("uno","/dev/cu.usbmodem144101")
    board.connect()

    board.pin_mode(LED_PIN, OUTPUT)
    while True:
        board.write_digital(LED_PIN, 0)
        time.sleep(1)

        board.write_digital(LED_PIN, 90)
        time.sleep(1)



修改保存后，用python来运行这个文件，


.. code-block:: bash

    $ python blink.py



UNO的板载LED开始闪烁，运行成功。 