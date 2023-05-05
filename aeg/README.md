<div>
In this exercise, we get a random binary and have 10 seconds to give it argv[1] to get shell

<br></br>

99% of the binaries are of the following format:

1. get hex input from argv[1]
2. xoring it (one xor value for odd indices of input and another for even indices)
3. matching the input against 0x30 values
4. in case all values were correct, call memcpy with the rest of the input, into the stack

the (primary) random bits are:
1. the xor values
2. the 0x30 values

our exploit is going as follows:
1. finding the xor values
2. finding the 0x30 values in order to get to the memcpy
3. exploit the stack overflow on the memcpy in order to write to RDI address to "sh" and partially overwrite libc address on the stack with the lower 6 bytes of system (bruteforce of 3 bytes)

how we achieved every level:
1. binary analysis with pwntools
2. binary analysis with pwntools + building pseudo-memory in order to find the 0x30 values
3. writing "sh" to the global buffer and using rop to pop it into RDI, and then put 6 bytes into libc address (libc_start_main+240)


<div dir='ltr'>
    <span style="font-size: 20px">FLAG: </span>
    <span>
    I wonder if MAYHEM can beat this challenge...? :)
    </span>
</div>
</div>