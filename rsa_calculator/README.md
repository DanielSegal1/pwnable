<div>
In this exercise, we use rsa calculator in order to get shell

<br></br>

the bugs we'll use in order to exploit the machine:
1. in the RSA_decrypt function, the decrypted value getting printf'd as the first parameter, hence, format string volnurability

our steps will be as follows

1. setting valid rsa keys (in order to use other functions)
2. encrypting the string 'bash'
3. encrypting format string which overwrites the printf got address with the system function address
4. decrypting the encrypted format string + the printf plt address (lower 8 bytes + higher 8 bytes)
5. decrypting the string 'bash' (in order to make the 'printf' (sytem) func to be called with it)
6. we have shell!

<div dir='ltr'>
    <span style="font-size: 20px">FLAG: </span>
    <span>
    what a stupid buggy rsa calculator! :(
    </span>
</div>
</div>