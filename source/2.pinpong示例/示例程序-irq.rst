irq
===========================================

.. code-block:: python

    import sys
    import time
    from pinpong.pinpong import *

    board = PinPong("uno","com99")
    board.connect()

    btn = Pin(board, Pin.D8, Pin.IN)

    def btn_handler(data):
        print("\n-----")
        print("pin_mode = ", data[0])
        print("pin = ", data[1])
        print("value = ", data[2])

    #btn.irq(trigger=Pin.IRQ_FALLING, handler=btn_handler)
    btn.irq(trigger=Pin.IRQ_RISING, handler=btn_handler)
    #btn.irq(trigger=Pin.IRQ_RISING+Pin.IRQ_FALLING, handler=btn_handler)

    while True:
        time.sleep(1)
