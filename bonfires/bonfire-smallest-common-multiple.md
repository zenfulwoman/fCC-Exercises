#Bonfire: Smallest Common Multiple
<a href="http://freecodecamp.com/challenges/Bonfire:%20Smallest%20Common%20Multiple?solution=function%20smallestCommons(arr)%20%7B%0A%0A%20%20%2F%2Fif%20no%20arguments%2C%20return%200%0A%20%20if%20(!arr)%20%7B%0A%20%20%20%20return%200%3B%0A%20%20%7D%0A%0A%20%20%2F%2Ffind%20the%20largest%20argument%0A%20%20if%20(arr%5B1%5D%20%3E%20arr%5B0%5D)%20%7B%0A%20%20%20%20var%20min%20%3D%20Number(arr%5B0%5D)%3B%0A%20%20%20%20var%20max%20%3D%20Number(arr%5B1%5D)%3B%0A%20%20%7D%20else%20%7B%0A%20%20%20%20var%20min%20%3D%20Number(arr%5B1%5D)%3B%0A%20%20%20%20var%20max%20%3D%20Number(arr%5B0%5D)%3B%0A%20%20%7D%0A%0A%20%20%2F%2FCalculate%20the%20Greatest%20Common%20Divisor%0A%20%20function%20calcGcd(first%2C%20next)%20%7B%0A%0A%20%20%20%20%2F%2FEculidean%20algorithm%0A%20%20%20%20while%20(r!%3D%3D%200)%20%7B%0A%20%20%20%20%20%20var%20r%20%3D%20next%20%25%20first%3B%0A%20%20%20%20%20%20var%20next%20%3D%20first%3B%0A%20%20%20%20%20%20var%20first%20%3D%20r%3B%0A%20%20%20%20%20%20gcd%20%3D%20next%3B%0A%20%20%20%20%7D%0A%20%20%7D%0A%0A%20%20%2F%2Fcalculate%20the%20Least%20Common%20Multiple%20for%20all%20numbers%20in%20the%20range%20of%20the%20first%20and%20second%20arguments.%0A%20%20var%20lcm%20%3D%20min%0A%0A%20%20for(var%20i%3Dmin%3Bi%3Cmax%3Bi%2B%2B)%20%7B%0A%20%20%20%20var%20first%20%3D%20lcm%0A%20%20%20%20var%20next%20%3D%20(i%2B1)%0A%20%20%20%20calcGcd(first%2C%20next)%0A%20%20%20%20var%20lcm%20%3D%20((first*next)%2Fgcd)%0A%20%20%7D%0A%20%20return%20lcm%3B%0A%7D%0A%0AsmallestCommons(%5B1%2C13%5D)%3B" target="_blank">Click here</a> to see the solution on the freeCodeCamp website.


####Instructions:
<p class="wrappable negative-10">Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.</p><p class="wrappable negative-10">The range will be an array of two numbers that will not necessarily be in numerical order.</p><p class="wrappable negative-10">e.g. for 1 and 3 - find the smallest common multiple of both 1 and 3 that is evenly divisible by all numbers <em>between</em> 1 and 3.</p><p class="wrappable negative-10">Remember to use <a href="//github.com/FreeCodeCamp/freecodecamp/wiki/How-to-get-help-when-you-get-stuck" target="_blank">Read-Search-Ask</a> if you get stuck. Try to pair program. Write your own code.</p><div class="negative-30-bottom"><div id="MDN-links"><p class="negative-10">Here are some helpful links:</p><div class="negative-10"><ul><li><a href="https://www.mathsisfun.com/least-common-multiple.html" target="_blank">Smallest Common Multiple</a></li></ul></div></div></div>


####Answer:
```javascript
function smallestCommons(arr) {

  //if no arguments, return 0
  if (!arr) {
    return 0;
  }

  //find the largest argument
  if (arr[1] > arr[0]) {
    var min = Number(arr[0]);
    var max = Number(arr[1]);
  } else {
    var min = Number(arr[1]);
    var max = Number(arr[0]);
  }

  //Calculate the Greatest Common Divisor
  function calcGcd(first, next) {

    //Eculidean algorithm
    while (r!== 0) {
      var r = next % first;
      var next = first;
      var first = r;
      gcd = next;
    }
  }

  //calculate the Least Common Multiple for all numbers in the range of the first and second arguments.
  var lcm = min

  for(var i=min;i<max;i++) {
    var first = lcm
    var next = (i+1)
    calcGcd(first, next)
    var lcm = ((first*next)/gcd)
  }
  return lcm;
}

smallestCommons([1,13]);
```