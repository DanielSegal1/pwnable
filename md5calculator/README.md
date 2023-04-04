<div>
In this exercise, we give input in base64 which then decoded in server side and outputs the md5 hash of it.

<br></br>

We can overflow the input but there is a canary cookie in the stack so first we will want to find its value.
In order to find the canary value, we exploit the function my_hash which "seeds" the random func with the current time, generating some random numbers and then sums some of them up with the canary cookie, and outputs the result.


to exploit it we'll seed our random func at the same time (thus getting the same randoms), and then compare the result of the server with ours to get the canary cookie value.
<br></br>
once we have the canary value we'll want to generate the input to overflow the stack in such way that the return address is the system func, and the param is address where we stored /bin/bash.
<br></br>

<div dir='ltr'>
    <span style="font-size: 20px">FLAG: </span>
    <span>
    Canary, Stack guard, Stack protector.. what is the correct expression?
    </span>
</div>
</div>