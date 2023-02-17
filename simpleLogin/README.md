<div>
In this exercise, we have to authenticate in order to get to function which executes shell
<br></br>
The program takes input, decodes it as base64, (checks for decoded length of less than 13 chars), hashes the decoded input with md5 and then checks it against hard coded hash.
<br></br>
Luckily, the last 4 bytes gets loaded to the EBP register as a result of bad memcpy to the wrong destination (var of size 8, while the input can be up to 12 bytes). we use that to load to EBP the address of the input and put in the middle 4 bytes of the input the address of shell.

</div>