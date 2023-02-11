<div>
In this exercise, we need to execute 7 functions (A, B, .. G) so that we'll have 7 integers (randomally made) printed. then we need to give the sum of those number as input in order to get the flag.
<br></br>
in order to do so, we're going to use buffer overflow on the stack in such way we overflow the return address of the ropme function to jump to A, and also overflowing the return address of A func to jump to B, and so on until we overflow the return address of the G func in order to jump back to ropme so we can give the sum as the result.

<div dir='ltr'>
    <span style="font-size: 20px">FLAG: </span>
    <span>
    Magic_spell_1s_4vad4_K3daVr4!
    </span>
</div>
</div>