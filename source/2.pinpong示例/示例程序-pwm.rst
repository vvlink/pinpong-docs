pwm
===========================================

.. code-block:: python

    import sys
    import time
    from pinpong.pinpong import *

    board = PinPong("uno","com99")
    board.connect()
    pwm0 = PWM(board,Pin(board,Pin.D6))

    while True:
        for i in range(255):
            print(i)
            pwm0.duty(i)
            time.sleep(0.05)
