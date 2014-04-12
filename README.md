Arduino-Timer
=============

A very powerful set of classes (or a library) that implements a set of timeout timers.  By default up to five timers can be executed simultaneously, but this can be changed easily by modifying a single #define.  Each alarm calls a user's function and passes a pointer to a user's object.  Two examples of usage are provided.
As written Timer/Counter 2 is used as the timers' clock.  The timer overflow interrupt increments a 15 bit counter and checks whether the new count matches any of the running timers.  Each timed out timer has its callback function executed, its repeats count decremented, and is removed from the list of timers if the new repeat count is zero.  Setting the repeats to zero outside the service routine results in infinite repetition of the timer.
