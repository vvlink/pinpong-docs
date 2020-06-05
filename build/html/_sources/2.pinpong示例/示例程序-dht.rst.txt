dht
===========================================

.. code-block:: python


    import sys
    import time
    from pinpong.pinpong import *
    from pinpong.libs.DFRobot_DHT import *


    board = PinPong("uno","com99")
    board.connect()

    dht11 = DFRobot_DHT11(board, Pin(board,Pin.D7))
    dht22 = DFRobot_DHT22(board, Pin(board,Pin.D6))

    while True:
        temp = dht11.temperature()
        humi = dht11.humidity()
        print("dht11 temperature=",temp," humidity=",humi)
        
        temp = dht22.temperature()
        humi = dht22.humidity()
        print("dht11 temperature=",temp," humidity=",humi)
        time.sleep(1)
