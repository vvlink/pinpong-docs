buzzer
===========================================


.. code-block:: python


    import sys
    import time
    from pinpong.pinpong import *
    from pinpong.libs.DFRobot_BUZZER import *

    board = PinPong("uno","com99")
    board.connect()

    buzzer = DFRobot_BUZZER(board, Pin(board,Pin.D7))
    buzzer.freq(200)

    while True:
        print("freq=", buzzer.freq())
        buzzer.on()
        time.sleep(1)
        buzzer.off()
        time.sleep(1)
        buzzer.freq(buzzer.freq()+100)
