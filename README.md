# ProtOS
Lightweight operating system for Arduino IDE compiler

Execution environment specifically designed to be run on weak arduinos.
ProtOS provides its' own standard library, it is capable of managing proto-threads,
implements command interface and introduces it's own nicely macro-wrapped exception handler.

The only thing you need to perform manually is redefining main() function so that it could support exception handling and
command line interface. Just replace it with the code below (or from main.cpp):

#include <musthave>
int main()
{
  try
  (
    setup();
    rethrow(); //I prefer manual rethrowing
    //this way code is more intuitive (but more ugly, yeah)
    for(;;)
    {
      faulty(loop()); //this is also possible this way
      if (_runSerialEvent) runSerialEvent();
    }
  )
}
