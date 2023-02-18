<div>
In this exercise, we play rpg game in order to get the flag.
<br></br>
our goal is to win one of the dragon (we'll win the Mama dragon) because when we win we have UAF to address we can write input to.
<br></br>
We'll use the Priest. At the start we'll lose to the baby dragon in order to play against the Mama Dragon. Then we'll use invincibility twice and refresh one (those 3 attacks x 4) so the dragon will heal up to 128 health which will overflow the hp of the dragon making the program think we won.
<br></br>
After that we can give input which with UAF will cause to jump to our input as address, and we'll give it the shell address.
</div>