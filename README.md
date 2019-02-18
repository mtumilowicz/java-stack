# java-stack

_Reference_: https://www.amazon.com/Java-Language-Features-Modules-Expressions/dp/1484233476

# frame
_Reference_: https://docs.oracle.com/javase/specs/jvms/se11/html/jvms-2.html#jvms-2.6

* is used to store data and partial results, as well as to perform dynamic linking, 
return values for methods, and dispatch exceptions
* new frame is created each time a method is invoked
* a frame is destroyed when its method invocation completes, whether that completion is normal or abrupt 
(it throws an uncaught exception)
* represents method invocation (in a given thread)
* it is an invocation context of a method
* for a given thread only one frame is active at any point
* active frame is called _current frame_ , corresponding method - _current method_, class declaring method - 
_current class_ 
* frames are allocated from the Java Virtual Machine stack of the thread creating the frame
* each frame has its own array of local variables, its own operand stack, and a reference 
to the run-time constant pool of the class of the current method.
* the sizes of the local variable array and the operand stack are determined at compile-time and are 
supplied along with the code for the method associated with the frame
* frame ceases to be current if its method invokes another method or if its method completes
* flow: 
    * when a method is invoked, a new frame is created and becomes current when control transfers to the new method
    * on method return, the current frame passes back the result of its method invocation, if any, to the previous frame
    * the current frame is then discarded as the previous frame becomes the current one.
    * frame created by a thread is local to that thread and cannot be referenced by any other thread
    
## local variables
_Reference_: https://docs.oracle.com/javase/specs/jvms/se11/html/jvms-2.html#jvms-2.6.1

## operand stack
_Reference_: https://docs.oracle.com/javase/specs/jvms/se11/html/jvms-2.html#jvms-2.6.2

## run-time constant pool
_Reference_: https://docs.oracle.com/javase/specs/jvms/se11/html/jvms-2.html#jvms-2.5.5

# stack
_Reference_: https://docs.oracle.com/javase/specs/jvms/se11/html/jvms-2.html#jvms-2.5.2

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