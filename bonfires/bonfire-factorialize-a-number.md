#Bonfire: Factorialize a Number
<a href="http://freecodecamp.com/challenges/Bonfire:%20Factorialize%20a%20Number?solution=function%20factorialize(num)%20%7B%0A%20%20if%20(num%20%3C%200)%20%7B%0A%20%20%20%20return%20-1%3B%0A%20%20%7D%0A%20%20else%20if%20(num%20%3D%3D%200)%20%7B%0A%20%20%20%20return%201%3B%0A%20%20%7D%0A%20%20%0A%20%20var%20tmp%20%3D%20num%0A%20%20for(var%20i%20%3D%20tmp%20-%201%3B%20i%20%3E%201%3B%20i--)%20%7B%0A%20%20%20%20num%20%3D%20num%20*%20i%3B%0A%20%20%7D%3B%0A%20%20return%20num%3B%0A%7D%0A%0Afactorialize(5%2C%20%27%27)%3B%0A" target="_blank">Click here</a> to see the solution on the freeCodeCamp website.


####Instructions:
<p class="wrappable negative-10">Return the factorial of the provided integer.</p><p class="wrappable negative-10">If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.</p><p class="wrappable negative-10">Factorials are often represented with the shorthand notation <code>n!</code></p><p class="wrappable negative-10">For example: <code>5! = 1 * 2 * 3 * 4 * 5 = 120</code></p><p class="wrappable negative-10">Remember to use <a href="//github.com/FreeCodeCamp/freecodecamp/wiki/How-to-get-help-when-you-get-stuck" target="_blank">Read-Search-Ask</a> if you get stuck. Write your own code.</p><div class="negative-30-bottom"><div id="MDN-links"><p class="negative-10">Here are some helpful links:</p><div class="negative-10"><ul><li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators" target="_blank">Arithmetic Operators</a></li></ul></div></div></div>


####Answer:
```javascript
function factorialize(num) {
  if (num < 0) {
    return -1;
  }
  else if (num == 0) {
    return 1;
  }
  
  var tmp = num
  for(var i = tmp - 1; i > 1; i--) {
    num = num * i;
  };
  return num;
}

factorialize(5, '');

```