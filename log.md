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
**Thoughts:** I'm intrigued with this algorithm, feeling neutral, a bit disappointed that I fogot that 0 times any number is 0 :sob:

**Link to tweet:** [Daniel Torres Day 13](https://twitter.com/RoosterMonster/status/953522163994181632)


<h2 align="center">Day 14: Wednesday January 17th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finished another algorithm today on FreeCodeCamp, and started/almost finsihed a 2nd algorithm. Here's my solution for the 1st algorithm:
```
<script>
function slasher(arr, howMany) {
  var finalArray = [];
  
  if(arr.length > howMany) {
    finalArray = arr.slice(howMany, arr.length);
  } else {
    finalArray = arr.slice(arr.length, arr.length);
  }
  
  console.log(finalArray);
}

slasher([1, 2, 3], 9);

/*
Instruction: chop arg1 from the index 0 to arg2 and return the remaining numbers if any
1. Make a var finalArray = [];
2. if arr.length > howMany do this: 
3. slice arr1(howMany, arr.length) into finalArray
4. else slice arr1(arr.length, arr.length) into finalArray
*/
</script>
```
Pretty stoked that I solved it:sunglasses:. I almost solved my 2nd algorithm, but I need more time to figure the missing last piece:confused:. Here's what I have so far:
```
<script>
function mutation(arr) {
  var temp, n, a;
  
  for(var i = 0; i < arr[1].length; i++) {
    temp = arr[1].charAt(i);
    n = arr[0].indexOf(temp);
    
    if(n !== -1) {
      a = "true";
    } else {
      a = "false";
    }
    if(a == "false") {
      a = "false";
    }
    console.log(a);
    return;
  }
}

mutation(["hello", "neo"]);

/*
1. Create a for loop that itterates through arr1[1] and does an indexOf check through arr1[0]
2. if all the letters are found return true otherwise return false
*/
</scirpt>
```
I know tomorrow I will finsih this:sunglasses:.

**Thoughts:** I'm feeling pretty good with my progress, especially with this commitment, so I must bask in this moment:sunglasses:.

**Link to tweet:** [Daniel Torres Day 14](https://twitter.com/RoosterMonster/status/953901527617323008)


<h2 align="center">Day 15: Thursday January 18th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** The 2nd algorithm is doing something funny, I think I'm trying to rush it and making mistakes:worried:. Somehow managed to create some infinite loops that crashed my browser. I've been using codepen to practice my code before transfering it to FreeCodeCamp. Here's on of my mess ups:
```
<script>

function mutation(arr) {
  var temp, n,
      a = true;
  do {
    for(var i = 0; i < arr[1].length; i++) {
      temp = arr[1].charAt(i);
      n = arr[0].indexOf(temp);
      
      if(n !== -1) {
        a = true;
      } else {
        a = false;
        return a;
      }
    }
  }
  while (a !== true);
  return a;
}

mutation(["hello", "Hello"]);

</script>
```
I keep thinking that I'm writing ugly code too.

**Thoughts:** I'm a little bummed out that I didn't finish, but I know I'm close.

**Link to tweet:** [Daniel Torres Day 15](https://twitter.com/RoosterMonster/status/954168162659966976)


<h2 align="center">Day 16: Friday January 19th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I didn't finish the algorithm, but I am taking a step back and re-evaluating my blueprint on how to complete this challenge. Not going to show code here as it's not much.

**Thoughts:** Today was a tough day, from begining to end, I'm unhappy that I didn't finish, but I am happy that I atleast coded for an hour, and keeping strong on this 100 day challenge.

**Link to tweet:** [Daniel Torres Day 16](https://twitter.com/RoosterMonster/status/954597424827285504)


<h2 align="center">Day 17: Saturday January 20th, 2018</h2>

**Link to Project:** [Chart.js](https://codepen.io/RoosterMonster/pen/LeqdoZ)

**Today's Progress:** I took a pause from my algorithm to play with a Javascript library called Chart.js, I want to document my progress with a line graph to set up future goals, so I can stay on track in FreeCodeCamp. Here's my experimental code so far, needs more work, bur pretty neat.
```
<script>
var ctx = document.getElementById('lineChart').getContext('2d');
var chart = new Chart(ctx, {
  type: 'line',
  
  data: {
    labels: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, ],
    datasets: [{
      label: "My First Dataset",
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [0, 0, 0, 1, 0, 0, 0, 1, 2, 0, 1, 1, 1, 0],
    }]
  },
});
</script>
```

**Thoughts:** Today was fun break to learn something new, something to add to my arsenal, since data is sucn a big deal now days.

**Link to tweet:** [Daniel Torres Day 17](https://twitter.com/RoosterMonster/status/954950293870886912)


<h2 align="center">Day 18: Sunday January 21th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I came back to my FreeCodeCamp algorithm problem(Mutations), retstarted it from scratch, and completed it. I keep thinking I must of completed my code unorthodox(ugly code), but I got the job done. Here's my solution:
```
<script>
function mutation(arr) {
  var argA = arr.slice(0, 1).toString().toLowerCase();
  var argB = arr.slice(1, 2).toString().toLowerCase();
  var verdict = true;
  
  for(var i = 0; i < argA.length; i ++) {
    var temp = argB.charAt(i);
    var num = argA.indexOf(temp);
    
    if(num !== -1) {
      
    } else {
      verdict = false;
      
    }
    
  }//end of for loop
  console.log(verdict);
  
  
}

mutation(["voodoo", "no"]);

/*
1. Convert both arr to lowerCase
2. itterate arr[1] with a for loop
3. Compare each of those letters to arr[0]
4. If false returns, stop code and return false
5  Otherwise return true
*/
</script>
```
I did something new with my if statement that I've never done before. I wonder if it's ok or bad practice.

**Thoughts:** I'm happy:smiley: that I was able to craft some code together to get the job done. I do wonder if I'm writing terrible code though:grimacing:.

**Link to tweet:** [Daniel Torres Day 18](https://twitter.com/RoosterMonster/status/955330638545997824)


<h2 align="center">Day 19: Monday January 22th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I started a new algorithm today, I'm pretty sure I know what to do, just so exhausted from the day:expressionless:, but atleast I did sit down to code. Here's my code vomit:
```
<script>
var falsey = [false, null, undefined, 0, NaN, '', ""];
var finalArray = [];


function bouncer(arr) {
 for(var i = 0; i < falsey.length; i++) {
    for(var j = 0; j < falsey[i].length; j++) {
      if(arr[i] !== falsey[j]) {
        finalArray.push(slice(i + (i + 1)));
      }
    }   
  }
  console.log(finalArray)
}

bouncer([7, "ate", "", false, 9]);

/*
Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
1. Iterate through the array.
2. If the aray is identical to falsey elements(null, undefined, ' ", etc), then remove those falsey from the array
3. Return the array with all the falsey's removed

poss. toos: Map, Array filter, booleans
*/

</scirpt>
```
I'm sure I'll finish this tomorrow, once I get more sleep in me.

**Thoughts:** Today was a long day, and not happy that I can't code well when I'm exhausted, but oh well.

**Link to tweet:** [Daniel Torres Day 19](https://twitter.com/RoosterMonster/status/955719453748051968)


<h2 align="center">Day 20: Tuesday January 23rd, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finished an algorithm on FreeCodeCamp, had my ups and downs, and curiousity tangents on ES6 tricks that didn't make sense to me, but didn't matter for now. Here's my solution:
```
<script>
// falsey = [false, null, undefined, 0, NaN, '', ""];
var finalArray = [];


function bouncer(arr) {
  finalArray = arr.filter(function (val) {
    return val;
  });
  console.log(finalArray);
}

bouncer([false, null, 0, NaN, undefined, ""]);

/*
Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
1. Iterate through the array.
2. If the aray is identical to falsey elements(null, undefined, ' ", etc), then remove those falsey from the array
3. Return the array with all the falsey's removed

poss. toos: Map, Array filter, booleans
*/
</script>
```
I started a new algorithm too, should finsih that soon from what I can tell. Here's my blueprint:
```
<script>
function destroyer(arr) {
  // Remove all the values
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);

/*
Filter out numbers of the 2nd Arg if present in the 1st Arg*
1. make a var argA = arr[0]
2. make a var argB = arr[1]
3. make a var finalArray
4. filter out argA if it equals argB and return the remains
*/
</script>
```
**Thoughts:** Today was a good day ultimately, but I had some confusion come my way that led to tangents, but all good learning experience.

**Link to tweet:** [Daniel Torres Day 20](https://twitter.com/RoosterMonster/status/956073285984440320)


<h2 align="center">Day 21: Wednesday January 24th, 2018</h2>

**Link to Project:** [Chart.JS](https://codepen.io/RoosterMonster/pen/LeqdoZ?editors=1010)

**Today's Progress:** I took a pause today from FreeCodeCamp, to do some other coding related things. I did a little bit of game development, and messed with Chart.JS again. I linked my graph WIP in the link above.

**Thoughts:** Today was a bit frustrating:disappointed: with chart.js. Hitting the FreeCodeCamp train again tomorrow.

**Link to tweet:** [Daniel Torres Day 21](https://twitter.com/RoosterMonster/status/956458163397513217)


<h2 align="center">Day 22: Thursday January 25th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I returned to work on my FCC algorithm, ran into a problem of there being more arguments than parameters which I've never came across to dealing with. I turned to my trusty Javascript book - The definitive guide, and was enlightened about this issue. Tomorros I shall finish the code. This is what I have so far:
```
<script>
var finalArray = [];
var argA; // = [1, 2, 3, 1, 2, 3]
var argB = [];

function destroyer(arr, brr, crr) { 
  var argA = arr;
  argB.push(brr, crr);
  
  finalArray = argA.filter(function(val) {
    return val !== argB[0] && val !== argB[1];
  })
  console.log(finalArray);
}

destroyer([3, 5, 1, 2, 2], 2, 3, 5);

/*
Filter out numbers of the 2nd Arg if present in the 1st Arg*
1. make a var argA = arr[0]
2. make a var argB = arr[1] & arr[2]
3. make a var finalArray
4. filter out argA if it equals argB and return the remains
*/
</script>
```
**Thoughts:** Today was great, even though I didn't finish my code. I did learn about uneven function parametes vs arguments, which will be a valuable arrow in my quiver(lol):satisfied:.

**Link to tweet:** [Daniel Torres Day 22](https://twitter.com/RoosterMonster/status/956779340674433024)


<h2 align="center">Day 23: Friday January 26th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I continued to work on my FCC algorithm, I'm so close to finishing my the algorithm. I must stop since I have to go to bed so I'm not a zombie at work tomorrow, but I'm so close! Here's what I have so far:
```
<script>
var finalArray = [];
var argA; // = [1, 2, 3, 1, 2, 3]
var argB = [];

function destroyer(a, b, c, /*optional*/d) { 
  var argA = a;
  if(arguments.length <= 3) {
    argB.push(b, c);
  } else {
    argB.push(b, c, d);
  }
  
  finalArray = argA.filter(function(val) {
    return val !== argB[0] && val !== argB[1] && val !== argB[2];
  });
  console.log(argB);
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);

/*
Filter out numbers of the 2nd Arg if present in the 1st Arg*
1. make a var argA = arr[0]
2. make a var argB = arr[1] & arr[2]
3. make a var finalArray
4. filter out argA if it equals argB and return the remains
*/
</script>
```
**Thoughts:** Today was good, would of been better if I would of finished my code. Exhaustion is getting the best of me.

**Link to tweet:** [Daniel Torres Day 23](https://twitter.com/RoosterMonster/status/957127803052244992)


<h2 align="center">Day 24: Saturday January 27th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I continued to work on my FCC algorithm, and I completed it succesfully. Here's how I did it:
```
<script>
var finalArray = [];
var argA; // = [1, 2, 3, 1, 2, 3]
var argB = [];

function destroyer(a, b, c, d) { 
  argA = a;
  if(arguments.length <= 3) {
    argB.push(b, c);
  } else {
    argB.push(b, c, d);
  }
  
  finalArray = argA.filter(function(val) {
    return val !== argB[0] && val !== argB[1] && val !== argB[2];
  });
  console.log(finalArray);
}

destroyer([3, 5, 1, 2, 2], 2, 3, 5);

/*
Filter out numbers of the 2nd Arg if present in the 1st Arg*
1. make a var argA = arr[0]
2. make a var argB = arr[1] & arr[2]
3. make a var finalArray
4. filter out argA if it equals argB and return the remains
*/
</scirpt>
```
**Thoughts:** Today was good day, I was tired as hell, reading the good book(JS book) trying to figure out my challenge. Happy that I coded and completed my problem.

**Link to tweet:** [Daniel Torres Day 24](https://twitter.com/RoosterMonster/status/957478155022774272)


<h2 align="center">Day 25: Sunday January 28th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I started a new FCC algorithm today, and thought I finished until I realized that it did not want repeated numbers in the process of wanting the index number coming from the 2nd argument. FCC didn't say this in the explanation, but I think that was on purpose to keep me on my toes. Here's what I have so far:
```
<script>
function getIndexToIns(arr, num) {
  var index;
  var wholeArray = arr;
  wholeArray.push(num);
  wholeArray.sort();
  index = wholeArray.indexOf(num);
  
  console.log(index);
}

getIndexToIns([3, 10, 5], 3);

/*
Return the index number of the 2nd argument once it is inserted in the 1st argument and sorted in order.
1. create an empty var index
2. create a var wholeArray = []
3. push arr & num into wholeArray and sorted in order
4. return index of num from wholeArray
*/
</script>
```
**Thoughts:** Today was a good day, I finally realized that FCC is not fully explaining everything in the directions to keep me on my toes. Which makes sense, I will probably come across this in the real world.

**Link to tweet:** [Daniel Torres Day 25](https://twitter.com/RoosterMonster/status/957847911584342016)


<h2 align="center">Day 26: Monday January 29th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finshed my FCC algorithm today with some ease. This was my solution:
```
<script>
function getIndexToIns(arr, num) {
  var index;
  var wholeArray = arr.filter(function(x) {
    return x !== num;
  });
  wholeArray.push(num);
  wholeArray.sort(function(a, b) {
    return a - b;
  });
  index = wholeArray.indexOf(num);
  
  console.log(index);
}

getIndexToIns([2, 5, 10], 15);

/*
Return the index number of the 2nd argument once it is inserted in the 1st argument and sorted in order.
1. create an empty var index
2. create a var wholeArray = []
3. push arr & num into wholeArray and sorted in order
4. return index of num from wholeArray
*/
</script>
```
I started on a new algorithm, last one in my section before it moves on to new challenges. I'm suppose to create a cipher decoder. This is my blueprint so far:
```
<script>

function rot13(str) { // LBH QVQ VG!
  
  return str;
}


rot13("SERR PBQR PNZC");

/*
Create a Cipher decoder based on ROT13(A=N, B=O) (+ 13)
1. Create a var finalString
2. Create a for loop that itterates the str returning the unicode of each letter
3. Add 13 to each unicode and then return that unicode back to the new character
4. Push the new translation into finalString

Tools: charCodeAt(), fromCharCode(), slice()
*/


</script>
```
**Thoughts:** Today was a good day, it was a long tiring day, but I didn't flake.

**Link to tweet:** [Daniel Torres Day 26](https://twitter.com/RoosterMonster/status/958237069096071168)


<h2 align="center">Day 27: Tuesday January 30th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign)

**Today's Progress:** I finshed another FCC algorithm today:satisfied:. It was a pretty neat challenge, building a Caesars Cipher. This was my solution:
```
<script>
var finalString = [];

function rot13(str) { // LBH QVQ VG!
  for(var i =0; i < str.length; i++) {
    var letterUnicode = str.charCodeAt(i);
    
    if(letterUnicode >= 78) {
      finalString.push(String.fromCharCode(letterUnicode - 13));
    } else if (letterUnicode >=65 && letterUnicode <= 77) {
      finalString.push(String.fromCharCode(letterUnicode + 13));
    } else {
      finalString.push(String.fromCharCode(letterUnicode));
    }
  }
  console.log(finalString.join(""));
}

// Change the inputs below to test
rot13("GUR DHVPX OEBJA QBT WHZCRQ BIRE GUR YNML SBK.");

/*
Create a Cipher decoder based on ROT13(A=N, B=O) (+ 13)
1. Create a var finalString
2. Create a for loop that itterates the str returning the unicode of each letter
3. Add 13 to each unicode and then return that unicode back to the new character
4. Push the new translation into finalString

Tools: charCodeAt(), fromCharCode(), slice()
Unicode of Cap letters = 65--90
*/
</script>
```
**Thoughts:** Today was a great day:satisfied:, I found out I'm having twin boys:satisfied::satisfied:, finsihed my last algorithm in my current section. Making a goal to do 200 hrs of FCC in 3 months:sweat_smile:; by 5/30/18. Hopefully find a web dev job during that time too. Also going to try to dive deep into css as well.

**Link to tweet:** [Daniel Torres Day 27](https://twitter.com/RoosterMonster/status/958624514190974976)


<h2 align="center">Day 28: Wednesday January 31th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [PureCSS](https://codepen.io/RoosterMonster/pen/oEXbjW?editors=0100)

**Today's Progress:** I worked on my Random Quote Machine project, doing research and planning out the design. I also worked on some pure CSS illustration to strengthen my CSS game. Learned alot. Provided a link to my 1st CSS art piece above.

**Thoughts:** Today was an ok day, a lot of researching and not much coding with my new project, but I do want it took look nice rather than a terrible design. The pure CSS stuff was pretty fun and I can't wait to be able to do more complex things with it.

**Link to tweet:** [Daniel Torres Day 28](https://twitter.com/RoosterMonster/status/959002464790851585)


<h2 align="center">Day 29: Thursday February 1st, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/gvabLe?editors=1100)

**Today's Progress:** I continued to work on my Random Quote Machine project, finishing the the CSS design. Now it's ready for the API to be thrown in to make the magic work. The design can be seen in the link above.

**Thoughts:** Today was a good day, CSS feels more comfortable than ever, not that I've made art with it. I kept battling myself with pure CSS and bootstrap. I'm starting to fall in love with pure CSS.

**Link to tweet:** [Daniel Torres Day 29](https://twitter.com/RoosterMonster/status/959298530065068032)


<h2 align="center">Day 30: Friday February 2nd, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/gvabLe?editors=1100)

**Today's Progress:** I continued to work on my Random Quote Machine project, struggled with woking with JSON links working in codepen, but figured out the limitations of why it wasn't working. I ended up finding an API that will work, and a damn good funny one; Ron Swonson quote machine coming up. I may try to find a Ron image API as well to complement my project.

**Thoughts:** Today was an ok day, lots of struggling and reading about JSON, AJAX, and API's. I did end up getting an API to work, and may be close to finishing my project.

**Link to tweet:** [Daniel Torres Day 30](https://twitter.com/RoosterMonster/status/959656242821054464)


<h2 align="center">Day 31: Saturday February 3rd, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/gvabLe?editors=1100)

**Today's Progress:** I continued to work on my Random Quote Machine project, I ran into some more issues and still don't quite understand it fully so I read up on it and did some examples, I'm going to need to continue to practice more so I fully understand. I also worked on some CSS practice.

**Thoughts:** Today was tough, exhaustion got the best of me and confusion blocked my understanding.

**Link to tweet:** [Daniel Torres Day 31](https://twitter.com/RoosterMonster/status/960095385602613248)


<h2 align="center">Day 32: Sunday February 4th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/JpXwYV?editors=0110)

**Today's Progress:** Today I took time to create images with pure CSS, learned SCSS & PUG, which is pretty sweet. Created sketch logo for practice. Link above.

**Thoughts:** Today was pretty sweet, learned some new tools that will help with CSS game.

**Link to tweet:** [Daniel Torres Day 32](https://twitter.com/RoosterMonster/status/960393301999288320)


<h2 align="center">Day 33: Monday February 5th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/MQexqp?editors=1100)

**Today's Progress:** Today I took time to create more images with pure CSS, learned Vue.JS and to animate, which is awesome to mess with. Link above.

**Thoughts:** Today was fun, learned some new tools that will help with CSS and javascript game.

**Link to tweet:** [Daniel Torres Day 33](https://twitter.com/RoosterMonster/status/960798629953851392)



<h2 align="center">Day 34: Tuesday February 6th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/oEzmbX)

**Today's Progress:** I returned to my FCC project; Random Quote Machine. I got it to work/look how I wanted it, except for the tweet button. I need to figure how to tweet these quotes. Link is above.

**Thoughts:** Today was good, got more comfortable with AJAX and API's. This tweet button is going to a gooe challenge, looking forward to to it.

**Link to tweet:** [Daniel Torres Day 34](https://twitter.com/RoosterMonster/status/961177811787513858)



<h2 align="center">Day 35: Wednesday February 7th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/oEzmbX?editors=1010)

**Today's Progress:** I finished my FCC project; Random Quote Machine. I got the tweet function to work and even added a bit of animation to the piece. link to project is above.

**Thoughts:** Today was sweet, I understand the Twitter API's a bit more, and it feels impowering to be able to use it with my creation.

**Link to tweet:** [Daniel Torres Day 35](https://twitter.com/RoosterMonster/status/961550396396224512)



<h2 align="center">Day 36: Thursday February 8th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR)

**Today's Progress:** Today I worked on my FCC weather app, did a lot of research, planning and designing. No code written persay today. Was mostly in Figma designing the look. I want to create beautiful apps not just functional.

**Thoughts:** Today was good, did some design and research. I can't wait to start coding it.

**Link to tweet:** [Daniel Torres Day 36](https://twitter.com/RoosterMonster/status/961823358454149121)



<h2 align="center">Day 37: Friday February 9th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR)

**Today's Progress:** Today I worked on my FCC weather app, continued on working on the design. I want to do more designs, but will settle for what I have design for now and focus on the code.

**Thoughts:** Today was ok, woked on design, want to do more, but don't want to lose focus on the main challenge; the code.

**Link to tweet:** [Daniel Torres Day 37](https://twitter.com/RoosterMonster/status/962231317097103360)



<h2 align="center">Day 38: Saturday February 10th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR)

**Today's Progress:** Today I continued to worked on my FCC weather app, worked on the design again. I simplified the design and added more color. Now I must code it.

**Thoughts:** Today was ok, revised the design. I need to code it, that will make me happy.

**Link to tweet:** [Daniel Torres Day 38](https://twitter.com/RoosterMonster/status/962578469140905984)



<h2 align="center">Day 39: Sunday February 11th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR)

**Today's Progress:** Today I continued to work on my FCC weather app, worked on building it with html and css. Try to add  some subtle animations, and struggling  a bit.

**Thoughts:** Today was rough, I struggled with animating some background stuff.

**Link to tweet:** [Daniel Torres Day 39](https://twitter.com/RoosterMonster/status/962921903013769217)



<h2 align="center">Day 40: Monday February 12th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR?editors=1100)

**Today's Progress:** Today I continued to work on my FCC weather app, worked on the html and css. Figured out the subtle background animation. Getting closer to completion.

**Thoughts:** Today was good, I figured out the animation background challenge I was facing.

**Link to tweet:** [Daniel Torres Day 40](https://twitter.com/RoosterMonster/status/963336162906554368)



<h2 align="center">Day 41: Tuesday February 13th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/bLgmaR?editors=1100)

**Today's Progress:** Today I continued to work on my FCC weather app, worked on the html and css. I had to choose another icon API, but it's slowly coming along. 

**Thoughts:** Today was ok, I ran into some subtle detail issues that took a lot of time, but I figured it out.

**Link to tweet:** [Daniel Torres Day 41](https://twitter.com/RoosterMonster/status/963709446055538688)


<h2 align="center">Day 42: Wednesday February 14th, 2018</h2>

**Link to Project:** [FreeCodeCamp](https://www.freecodecamp.org/torresdesign) [CodePen](https://codepen.io/RoosterMonster/pen/PQJJeX?editors=1100)

**Today's Progress:** Today I did some CSS excercise, to strengthen my CSS game, made some pure CSS art. 

**Thoughts:** Today was good, I used HTML PUG and SCSS to do some pure CSS art.

**Link to tweet:** [Daniel Torres Day 42]( https://twitter.com/RoosterMonster/status/963962556233662464 )



<h2 align="center">Day 43: Thursday February 15th, 2018</h2>

**Link to Project:** [CodePen](https://codepen.io/RoosterMonster/pen/PQJJeX?editors=1100)

**Today's Progress:** Today I did some more CSS excercise, to strengthen my CSS game, finished a CSS art. 

**Thoughts:** Today was ok, I used HTML PUG and SCSS to do some pure CSS art.

**Link to tweet:** [Daniel Torres Day 43]( https://twitter.com/RoosterMonster/status/964472387302408193 )


<h2 align="center">Day 44: Friday February 16th, 2018</h2>

**Link to Project:** [CodePen](https://codepen.io/RoosterMonster/pen/NyXxqR?editors=1100)

**Today's Progress:** Today I did some more CSS excercise, finshed another art piece. 

**Thoughts:** Today was good, I used HTML PUG and SCSS to create and finish some pure CSS art.

**Link to tweet:** [Daniel Torres Day 44]( https://twitter.com/RoosterMonster/status/964694966919315456 )

