<h1 align="center">100 Days of code with Daniel Torres</h1>

<img src="https://s20.postimg.org/be602idq5/hero_Image2.png" alt="illustration of my my tools to code and design">
Howdy World! You are about to witness the journey of a soon-to-be dad take on the 100-day coding challenge. As of today January 4th, 2018 I shall commit to doing at least 1 hour of coding a day. I know this will be good for me, as practice makes perfect(or a good dev that is).
I will share my progress, and also share some of my internal thoughts and emotions, as I'm sure there will be capricious moments. Well it's now time to roll of my sleeves and start this journey.

<h2 align="center">Day 1: Thursday January 4th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

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

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

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

<h2 align="center">Day 3: Saturday January 6th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** Today I continued to work...more like struggle on my basic algorithm problem on Freecodecamp, challenge: Return Largest Numbers in Arrays. This is what I have so far:

```
<script>
var largestInt = 0;
var largestArray = [];

function largestOfFour(arr) {
  for(var i=0; i < arr.length; i++) {
    for(var j =0; j < arr[i].length; j++) {
      if(arr[i][j] > largestInt) {
        largestInt = arr[i][j];
      }
    }
    console.log(largestInt);
  }
}

largestOfFour([[4, 5, 1, 3],[1,2,3,6]]);
</script>
```
It's spitting the largest number correctly from each sub array, I'm having trouble storing those numbers into a new array.

**Thoughts:** The struggle is real, but I beleive I am making progress from learning from my mistakes, on what works and what doesn't. Hopefully it makes more sense tomorrow.

**Link to tweet:** [Daniel Torres Day3](https://twitter.com/RoosterMonster/status/949543114628190209)

<h2 align="center">Day 4: Sunday January 7th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** Today was a glorious day! I finished my algorithm problem on Freecodecamp, challenge: Return Largest Numbers in Arrays. This is my solution:

```
<script>
var largestInt = 0;
var largestArray = [];

function largestOfFour(arr) {
  for(var i=0; i < arr.length; i++) {
    largestInt = arr[i][0];
    for(var j =0; j < arr[i].length; j++) {
      if(arr[i][j] > largestInt) {
        largestInt = arr[i][j];
      }
    }/*for loop 2*/
    largestArray.push(largestInt);
  }/*for loop 1*/
  console.log(largestArray);
}

largestOfFour([[13, 27, 18, 26], [4, 5, 1, 3], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
</script>
```
I was near the end of my hour when I figured this out, it was the function parameter index that was the missing key.
This should be extremely valuable and key to cycling and extracting info from arrays.

**Thoughts:** I'm happy with the solution, I'm sure their is an easier method. Excited to see what other ways I can use this trick.

**Link to tweet:** [Daniel Torres Day4](https://twitter.com/RoosterMonster/status/950234835263483904)

<h2 align="center">Day 5: Monday January 8th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** Today was a fantastic day! I finished 2 algorithm problems on Freecodecamp, challenge 1: Confirm the ending. This is my solution:

```
<script>

function confirmEnding(str, target) {
  strLength = str.length;
  targetLength = target.length;
  num = strLength - targetLength;
  res = str.substring(num)
  if (target == res) {
    console.log(true);
  } else {
    console.log(false);
  }
}

/*confirmEnding("Bastian", "n");*/
confirmEnding("He has to give me a new name", "dog");
/*
1. Split arg string to an array if more than one word otherwise just store single word in an array
2. Compare target arg to last element of split array
3.if target arg is == to last element, return true
*/

/* Possible solution is to get length of target arg, minus the string length, and with that number use in substring method to match*/
</script>
```
I've been jotting down notes on how I attend to tackle the problem, this has help me to solve the problem quicker it seems, so I included those with my code. This must be a personal record for me, because I solved this problem on the 1st attempt, so thats a great feeling.
challenge 2: Repeat a string by the second argument. This is my solution:
```
<script>
function repeatStringNumTimes(str, num) { 
  if(num < 0) {
    num = " ";
  }
  res = str.repeat (num);
  console.log(res);
}

repeatStringNumTimes("abc", -1);

/*
1. return string arg however many times the number arg is
2. return an empty string if number arg is a negative int
*/
</script>
```
I completed this challenge pretty quickly as well, just not as quick as the 1st one. A little bit of trial and error did the trick here.

**Thoughts:** I'm super happy to have completed 2 algorithm challenges with ease.:heart_eyes_cat:

**Link to tweet:** [Daniel Torres Day5](https://twitter.com/RoosterMonster/status/950634093456146432)


<h2 align="center">Day 6: Tuesday January 9th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I started on a new alogrithm today, wrote down my steps and competed the code, but there seems to be a lack of clear instructions/request for the objective. Here's my progress: 
```
<script>
function truncateString(str, num) {
  var dots = "...";
  var strLength = str.length;
  if (num > 3) {
    var newString = num - 3;
    var res = str.slice(0, newString);
    var finalString = res.concat(dots);
  } else {
    res = str.slice(0, num);
    finalString = res.concat(dots);
  }
  console.log(finalString);
}

truncateString("A-tisket a-tasket A green and yellow basket", 2);

/*
1. Get the length of the string arg and store it in var strLength
2. If int arg is greater than 3 than do the following
3. Ing arg - 3 = var newString
4. str slice(0, newString) = var res
5. var res + "..." = final string
6. else add "..." to str = final string
*/
</script>
```
I'll have to look into the blog and see if anyone has a clear understanding of the instructions/results wanted.

**Thoughts:** I'm a mix bag of emotions right now. I was able to code what i thought the instructions wanted, but there's something else wanted as well that is not clear in the instructions.

**Link to tweet:** [Daniel Torres Day 6](https://twitter.com/RoosterMonster/status/950955559355793409)


