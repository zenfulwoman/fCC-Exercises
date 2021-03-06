#Bonfire: Roman Numeral Converter
<a href="http://freecodecamp.com/challenges/Bonfire:%20Roman%20Numeral%20Converter?solution=function%20convert(num)%20%7B%0A%20%20var%20roman%20%3D%20%5B%27M%27%2C%20%27CM%27%2C%20%27D%27%2C%20%27CD%27%2C%20%27C%27%2C%20%27XC%27%2C%20%27L%27%2C%20%27XL%27%2C%20%27X%27%2C%20%27IX%27%2C%20%27V%27%2C%20%27IV%27%2C%20%27I%27%5D%3B%0A%20%20var%20arabic%20%3D%20%5B1000%2C%20900%2C%20500%2C%20400%2C%20100%2C%2090%2C%2050%2C%2040%2C%2010%2C%209%2C%205%2C%204%2C%201%5D%3B%0A%0A%20%20if(num%20%3E%203999%20%7C%7C%20num%20%3C%200)%20return%3B%0A%20%20%0A%20%20%2F%2FStep%20through%20the%20roman%20array%2C%20adding%20the%20roman%20numeral%20for%20the%20current%20index%20location%20x%20times.%0A%20%20%2F%2FCalculate%20x%20by%20rounding%20down%20the%20quotient%20of%20the%20number%20passed%20to%20the%20function%20(num)%20and%20the%0A%20%20%2F%2F%20arabic%20alue%20at%20the%20same%20index%20location.%20Update%20num%20each%20time%20the%20quotient%20is%20greater%20than%200.%0A%20%20var%20answer%20%3D%20roman.reduce(function%20(previousValue%2C%20currentValue%2C%20index)%20%7B%0A%20%20%20%20var%20x%20%3D%20Math.floor(num%20%2F%20arabic%5Bindex%5D)%3B%0A%20%20%20%20num%20-%3D%20arabic%5Bindex%5D%20*%20x%3B%0A%20%20%20%20return%20previousValue%20%2B%20currentValue.repeat(x)%3B%0A%20%20%7D%2C%20%27%27)%3B%0A%20%20return%20answer%3B%0A%7D%0A%0Aconvert(36)%3B" target="_blank">Click here</a> to see the solution on the freeCodeCamp website.


####Instructions:
<p class="wrappable negative-10">Convert the given number into a roman numeral.</p><p class="wrappable negative-10">All <a href="http://www.mathsisfun.com/roman-numerals.html" target="_blank">roman numerals</a> answers should be provided in upper-case.</p><p class="wrappable negative-10">Remember to use <a href="//github.com/FreeCodeCamp/freecodecamp/wiki/How-to-get-help-when-you-get-stuck" target="_blank">Read-Search-Ask</a> if you get stuck. Try to pair program. Write your own code.</p><div class="negative-30-bottom"><div id="MDN-links"><p class="negative-10">Here are some helpful links:</p><div class="negative-10"><ul><li><a href="http://www.mathsisfun.com/roman-numerals.html" target="_blank">Roman Numerals</a></li></ul></div><div class="negative-10"><ul><li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice" target="_blank">Array.splice()</a></li></ul></div><div class="negative-10"><ul><li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf" target="_blank">Array.indexOf()</a></li></ul></div><div class="negative-10"><ul><li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join" target="_blank">Array.join()</a></li></ul></div></div></div>


####Answer:
```javascript
function convert(num) {
  var roman = ['M', 'CM', 'D', 'CD', 'C', 'XC', 'L', 'XL', 'X', 'IX', 'V', 'IV', 'I'];
  var arabic = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];

  if(num > 3999 || num < 0) return;
  
  //Step through the roman array, adding the roman numeral for the current index location x times.
  //Calculate x by rounding down the quotient of the number passed to the function (num) and the
  // arabic alue at the same index location. Update num each time the quotient is greater than 0.
  var answer = roman.reduce(function (previousValue, currentValue, index) {
    var x = Math.floor(num / arabic[index]);
    num -= arabic[index] * x;
    return previousValue + currentValue.repeat(x);
  }, '');
  return answer;
}

convert(36);
```