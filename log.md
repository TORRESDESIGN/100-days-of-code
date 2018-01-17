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


<h2 align="center">Day 7: Wednesday January 10th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I continued on the Truncate a string alogrithm today, having issues with the last part regarding <= 3 part, keeps running the code twice. Here's my progress: 

```
<script>
/*function truncateString(str, num) {
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

truncateString("A-tisket a-tasket A green and yellow basket", 2);*/


function truncateString(str, num) {
  var dots = "...";
  var strLength = str.length;
  if(num < str.length) {
    if(num <= 3) {
      var newInt = strLength - num;
      var res = str.slice(0, newInt);
      var finalString = res.concat(dots);
      console.log(finalString);
    }
    var newInt = num - 3;
    var res = str.slice(0, newInt);
    var finalString = res.concat(dots);
    console.log(finalString);
  } else {
    console.log(str);
  }
}

/*truncateString("A-", 1); */
truncateString("Absolutely Longer", 2)


/*
if str arg length is longer than num arg, truncate the str with "..." ending, so that the new str... length is = to the num
if the num arg is <= to 3, truncate the str with "..." ending

1. if str arg length is longer than num arg, do the following:
2. num - 3 = var numSlice
3. str.slice(0, numSlice) = var res
4. res + "..." = var finalString
5. 
6. 
*/

</script>
```
I know I'm super close to completing this, and I'm just overthinking it.

**Thoughts:** I'm a bit disappointed with myself, because I thought I would finish this and continue on. I was a bit scatter brain today, kept thinking i knew the answer, but couldn't execute it. I went back to rewriting my notes of action, and did not finish that, so today was a struggle.

**Link to tweet:** [Daniel Torres Day 7](https://twitter.com/RoosterMonster/status/951269304955097088)


<h2 align="center">Day 8: Thursday January 11th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finished the Truncate a string alogrithm today, the issues with the last part regarding <= 3 part, was related to the testing practices of using console.log() without a return statement afterwasrds. I've been reading that we should move on from using console.log() to test code, I need to work on that eventually. Here's my code:

```
<script>
function truncateString(str, num) {
  var finalString;
  if(num < str.length) {
    if(num <= 3) {
      finalString = str.slice(0, num).concat("...");
      console.log(finalString);
      return;
    }
    finalString = str.slice(0, num - 3).concat("...");
    console.log(finalString);
  } else {
    console.log(str);
  }
}

/*truncateString("A-", 1);*/ 
truncateString("A-tisket a-tasket A green and yellow basket", "A-tisket a-tasket A green and yellow basket".length + 2)


/*
if str arg length is longer than num arg, truncate the str with "..." ending, so that the new str... length is = to the num
if the num arg is <= to 3, truncate the str with "..." ending

1. if str arg length is longer than num arg, do the following:
2. str.slice(0, num - 3) = var res
3. res + "..." = var finalString
4. else return str
5. if num arg <= 3, do the following
6. str.slice(0, str.length - num) = var res
7. res + "..." = var finalString
*/
</script>
```
My code was longer due to the holding variables I created, but learned that I didn't need them, and that shorten my code quiet a bit. 

**Thoughts:** I'm a little less scatterbrain today, but I'm happy with what I learned, even though I didn't expect to take this long to finish this algorithm.

**Link to tweet:** [Daniel Torres Day 8](https://twitter.com/RoosterMonster/status/951562279283187712)

<h2 align="center">Day 9: Friday January 12th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I started on a new alogorithm today; chunky monkey. I have to write a function that splits an array into groups the length of the second arg. I have to use protoype to do this as well. Here's my code so far before I figured out I'm suppose to use protype:
```
<script>
function chunkArrayInGroups(arr, size) {
  var myArray = [];
  var newArr;
  var newArrLength;
  for(var i = 0; i < arr.length; i++) {
    newArrLength = arr - size;
    
    var res = arr.slice(arr[0], size);
    console.log(res);
  }
}


chunkArrayInGroups(["a", "b", "c", "d"], 2);

/*
1.
*/

/*
0. Create a var myArray = []
1. Create a for loop that iterates through the 1st arg and pushes info into 1st array of var myArray until iterate # is == to 2nd arg
2. Than continue the loop and push info into the 2nd array
3. return myArray
*/
</script>
```
I didn't get very far in my opinion, I spent a lot of time trying to understand prototype. I still don't fully understand.

**Thoughts:** I feel pretty dense right now, because I can't understand protypes.

**Link to tweet:** [Daniel Torres Day 9](https://twitter.com/RoosterMonster/status/952086859563200512)


<h2 align="center">Day 10: Saturday January 13th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I took a pause to learn about prototypes, I've been struggling to understand it, but it's slowly making sense after taking this time to read multiple articles and playing with the property. Here's my little sandbox code examples:

```
<script>
/*Prototype properties
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain
https://www.pluralsight.com/blog/software-development/understanding-javascript-prototypes
https://guide.freecodecamp.org/javascript/prototypes*/

/*var o = {
  a: 2,
  m: function() {
    return this.a + 1;
  }
};

var p = Object.create(o);
p.a = 4;

console.log(p.m());*/

/*var a = {a: 4};
var b = Object.create(a);
var c = Object.create(b);
var d = Object.create(null);

console.log(d.hasOwnProperty);*/

catA._proto_;

</script>
```

**Thoughts:** I'm in the dark about this property, but I do see a little bit of light.

**Link to tweet:** [Daniel Torres Day 10](https://twitter.com/RoosterMonster/status/952438912907059201)


<h2 align="center">Day 11: Sunday January 14th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I continued learning about prototypes, and It makes more sense now. I'm going to try to tackle that algorithm next time. Here's some of my code on prototypes:
```
<script>
/*Prototype properties
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain
https://www.pluralsight.com/blog/software-development/understanding-javascript-prototypes
https://javascriptweblog.wordpress.com/2010/06/07/understanding-javascript-prototypes/ <---Good!
https://guide.freecodecamp.org/javascript/prototypes*/

var Circle = function(radius) {
  this.radius = radius;
}

Circle.prototype.area = function() {
  return Math.PI*this.radius*this.radius;
}

var a = new Circle(3),
    b = new Circle(4);

console.log(a.area().toFixed());

</script>
```
This new trick seems pretty powerful, and I'm excited to use it.

**Thoughts:** I'm feeling pretty good with what I know of prototypes so far.

**Link to tweet:** [Daniel Torres Day 11](https://twitter.com/RoosterMonster/status/952777666138025984)


<h2 align="center">Day 12: Monday January 15th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I continued learning about prototypes, I read different authors take on it and tested it out. I'm not going to share any code, since it's just messing around and mostly reading I did today.

**Thoughts:** I'm feeling pretty exhausted, staying up late reading about this complex property.

**Link to tweet:** [Daniel Torres Day 12](https://twitter.com/RoosterMonster/status/953192200753459201)


<h2 align="center">Day 13: Tuesday January 16th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finished my prototype algorithm on feecodecamp, turns out I didn't need to read about prototypes as much as I did, but it will help in the future to be familiar. I learn some neat tricks on this algorithm though. Here's my solution:

```
<script>
function chunkArrayInGroups(arr, size) {
  var finalArray = [];
  
  for(var i = 0; i < arr.length/size; i++) {
    finalArray.push(arr.slice(i * size, (i + 1) * size));
  }
  console.log(finalArray);
}


chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6, 7, 8], 4);

</script>
```
**Thoughts:** I'm intrigued with this algorithm, feeling neutral, a bit disappointed that I fogot that 0 times any number is 0 :sadface:

**Link to tweet:** [Daniel Torres Day 13](https://twitter.com/RoosterMonster/status/953522163994181632)
