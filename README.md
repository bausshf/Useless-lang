# Useless

Useless is a useless programming language providing a programming language that is everything but intuitive.

Not only does it have a very limited and useless set of instructions and operators, it will also add additional instructions that basically do nothing to make each application use more resource, memory and decrease performance.

The instructions inserted are based on previous instructions given and thus it's almost impossible to predict what the application will actually end up doing, thus making it more useless as your programs will almost never do as you attend.

It is however possible to write programs in Useless that works, but they'll be counter-intuitive, full of performance issues nd will do all kind of extra things that the program really didn't mean to do.

The compiled program will produce a really ugly set of C code that will be almost cryptic and looks obfuscated because of all the useless things a Useless application does.

Also Useless only has two variables that you can use. One is the counter for loops, the other is a pointer to memory allocated in which you can only increment the pointer until it reaches out of bounds, then it'll roll-back to the first offset.


## So what's the point of Useless?

Since every programmer seem to not care about performance or if programs work correctly, why should a programmer care about whether a programming language works or not?

Useless is perfect for modern day programmers, because no modern programmers care about actual programming anymore.

This programming language will provide the perfect set of instructions and behavior of any enterprise software written today. You probably wouldn't even notice a difference from a program written in Useless or a program writte in Java by 10 Junior Developers who's on a tight schedule. So why waste time on a huge build system, fancy programming languages etc. when you can just use Useless and have your useless enterprise software written without the burden of other useless tools. In reality you just need one useless tool and that's Useless.

## Examples of extra things Useless does without you instructing it to:

* Allocating memory will always allocate extra memory that you didn't request.

* Loops will only be executed if the number given is less than a random number generated at process start. The random number generated at process start is based on a seed that holds the value of the amount of instructions the program has (Not including the instructions Useless inserts.) - This means that it's possible to determine the seed/random number, but it also means that the behavior of the application depends on the amount of instructions given, as well the random number determined from it, making it even more useless.

* The memory allocated is freed every time a loop begins, meaning you cannot use any data out of scope.

* If the amount of instructions in the program is odd then the allocated buffer memory will only be half the size you request to allocate.

* If the first and last value of the current memory is 255 then the program will shutdown without any messages or warnings. These values are analyzed after ex. a file has been read to prevent the program shutting down in the middle of reading the file. This makes Useless very useless because it will only be able to handle specific memory and not all files. If the amount of instructions in the program is an odd number then it'll also shutdown during reading of files.

* All loops will be executed double as many times, but their actual actions are only executed the requested amount of time, instead of that there is put a 100ms delay per execution for the extra loops, making loops ineffecient and useless.

* If the program has arguments passed to it then it'll shutdown unless the amount of instructions is odd then the initial memory will be arguments passed to the program, but all the values of the arguments will be swapped around making it impossible and useless to properly use the passed arguments.

## Instructions

### &

Allocate memory to the size of the current pointer's offset with the size of an int. Ex. if "(pointer + offset) ... (pointer + offset + 3)" equals an integer value of 500 then 500 bytes are allocated and the previous memory is freed. That's because you can only have a single allocation in Useless at a time.

### *

Will move the pointer's offset one up until it hits the boundary of the memory then it'll go back to the first offset. This means that to decrease the offset of the pointer you must increase it until it rolls over.

### +

Will increment the memory value at the pointer's current offset. The pointer is always pointing to a byte value, meaning to add the value of a 32bit integer you must incrememnt the pointer's value and move the pointer's offset 3 times since a 32bit integer holds a value of 4 bytes.

### .

Will increment the value of the loop pointer. The loop pointer always points to memory of size_t (32bit integer on x86 / 64bit integer on x64)

###  ( ... )

This is a loop and it'll execute everything inbetween while the value of the loop pointer isn't 0.

### >

Writes the current pointer value to stdout.

### <

Reads the current line of stdin into memory.

### >>

Writes to a file with a name that is the amount of instructions the program has with the extension ".useless" and the content will be the first value of the memory as a 32bit integer as the amount of bytes to write and then from that offset it'll write every following byte until it reads the given amount of bytes to write.

### <<

Reads from a file with a name that is the amount of instructions the program has with the extension ".useless" and fills the memory with the content of the file.

### !

This instruction will execute a random instruction and must be placed at least 16 times per application. If the amount of instructions of the program is odd then it must be placed 32 times. The application will shutdown without any warnings or errors when the amount of the **!** instruction doesn't match the necessary amount.
