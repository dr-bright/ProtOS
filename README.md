# ProtOS
Lightweight operating system for limited devices.

It is an execution environment specifically designed to be run on weak arduinos or anywhere where needed. ProtOS provides its' own standard library, it is capable of managing proto-threads, implements command interface and introduces it's own nicely macro-wrapped exception handler.

For now we are in deep alpha testing mode, we have no wiki and a majority of modules missing but with your patience and support anything is possible :D

The only thing you definetely need to perform manually is redefining main() function.
If you code in Arduino IDE (80% of the cases, I think) you need to find main() function inside:
"arduino-ide/hardware/cores/arduino/Arduino.h"
and then redefine it
-


Here comes short tutorial of utilizing key features of ProtOS:

                             ~~~~WIP~~~~
