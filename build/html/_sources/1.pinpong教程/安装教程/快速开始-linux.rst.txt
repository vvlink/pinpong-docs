
============
Linux平台
============



1、打开终端，Ctrl+Alt+T，并连接上UNO板，在终端中输入，


.. code-block:: bash    
    
        
        $ ls /dev/ttyACM*


2、输入上述命令后，会出现设备的端口号，记录下来


.. image::  images/linux_quickstart1.png


3、找到示例代码，我们已blink.py为例，修改主控板名称为uno和端口号为ttyACM0。修改后保存


.. image::  images/linux_quickstart3.png


4、运行blink.py，uno板开始闪烁，运行成功

.. image::  images/linux_quickstart4.png
