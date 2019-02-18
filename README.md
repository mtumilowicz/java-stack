# java-stack

_Reference_: https://www.amazon.com/Java-Language-Features-Modules-Expressions/dp/1484233476

# frame
_Reference_: https://docs.oracle.com/javase/specs/jvms/se9/html/jvms-2.html#jvms-2.6

* represents method invocation (in a given thread)
*

# stack
_Reference_: https://docs.oracle.com/javase/specs/jvms/se9/html/jvms-2.html#jvms-2.5.2

* each thread in a JVM has its own JVM stack
* created when thread is created
* LIFO
* stores frames
* when new method is invoked new frame is pushed to the top of the stack
* when the method invocation completes the stack is popped out from the stack
* stack contains: 
* may differ on different implementations of JVM (could contain more info)

# projects
* https://github.com/mtumilowicz/java8-stack-stackwalking
* https://github.com/mtumilowicz/java9-stack-stackwalking