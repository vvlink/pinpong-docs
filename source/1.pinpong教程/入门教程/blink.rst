示例程序-blink
===============

.. code-block:: python


import sys
import time
from pinpong.pinpong import *

board = PinPong("uno","com17")
board.connect()
d13 = Pin(board, Pin.D7, Pin.OUT)

while True:
  d13.value(0)
  time.sleep(1)

  d13.value(1)
  time.sleep(1)
