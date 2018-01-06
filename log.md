<h1 align="center">100 Days of code with Daniel Torres</h1>

<img src="https://s20.postimg.org/be602idq5/hero_Image2.png" alt="illustration of my my tools to code and design">
Howdy World! You are about to witness the journey of a soon-to-be dad take on the 100-day coding challenge. As of today January 4th, 2018 I shall commit to doing at least 1 hour of coding a day. I know this will be good for me, as practice makes perfect(or a good dev that is).
I will share my progress, and also share some of my internal thoughts and emotions, as I'm sure there will be capricious moments. Well it's now time to roll of my sleeves and start this journey.

<h2 align="center">Day 1: Thursday January 4th, 2018</h2>

**Today's Progress:** Today I worked on a basic algorithm problem on Freecodecamp, challenge: Return Largest Numbers in Arrays. This is what the problem looks like:
```
<script>
function largestOfFour(arr) {
  return arr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
</script>
```
Basically I need to code an algorithm that loops through the multi-dimensional array and extracting the  largest number in each sub-array, and spit it out into it's own array, essentially this: [5,27,39,1001]

While working on this, I ran into an issue where my for loop was no working correctly, and after tyring to troubleshoot the issue time and time again, I discovered it was just a typo, freaking typo. I hate when that happens.:triumph:

I did not finish, but I hope to make better progress tomorrow.:smile:
Here's is my blueprint:

1.Loop through all the main arrays

2.If number is > 0 store it as var largestNum

3.Compare the next number vs var largestNum, if number is bigger, it takes it's place

4.Once it cycles through a sub array it stores the var largestNum and pushes that number into var largestArray

5.Once it cycles through all the sub arrays, there should be 4 numbers

6.Join all those numbers into one array

7.Eat Pizza as reward



**Thoughts:** This wasn't a very good start for me, I got pretty tripped up on that typo. I know this a harder challenge and it takes time, but I relish that satisfaction of when a problem is solved. I'm sure tomorrow will be much better.

**Link to tweet:** [Daniel Torres Day1](https://twitter.com/RoosterMonster/status/949122795883044864)

<h2 align="center">Day 2: Friday January 5th, 2018</h2>

**Today's Progress:** Today I continued to work on my basic algorithm problem on Freecodecamp, challenge: Return Largest Numbers in Arrays. This is what I have so far:
```
<script>
var largestInt = 0;
var largestArray = [];

function largestOfFour(arr) {
  for(var i=0; i < arr.length; i++) {
    for(var j =0; j < arr[i].length; j++) {
      if(largestInt < arr[i][j]) {
        largestInt = arr[i][j];
        console.log(largestInt);
      }
    }
  }
}

largestOfFour([[4, 5, 1, 3],[1,2,3,4]]);
</script>
```
I got it to return the 2 largest numbers, so a little progress here. Hopefully tomorrow I can finsih it!

**Thoughts:** Today was tough, the if statement inside the for loop was giving me problems. I got it to work, but it's not perfect. I know these struggles are just going to solidfy my knowledge so I don't run across them again. Tomorrow shall be a better day!

**Link to tweet:** [Daniel Torres Day2](https://twitter.com/RoosterMonster/status/949543114628190209)



