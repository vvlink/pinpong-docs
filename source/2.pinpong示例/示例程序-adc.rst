adc
===========================================

.. code-block:: python

    import sys
    import time
    from pinpong.pinpong import *

    board = PinPong("uno","com99")
    board.connect()

    adc0 = ADC(board,Pin(board, Pin.A0))
    adc1 = ADC(board,Pin(board, Pin.A1))

    while True:
        v = adc0.read()
        print("A0=", v)
        v = adc1.read()
        print("A1=", v)
        time.sleep(0.5)
