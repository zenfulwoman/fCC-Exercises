#Waypoint: Concatenate Strings with concat
<a href="http://freecodecamp.com/challenges/Waypoint:%20Concatenate%20Strings%20with%20concat?solution=var%20array%20%3D%20%5B1%2C2%2C3%5D%3B%0A%0Avar%20concatMe%20%3D%20%5B4%2C5%2C6%5D%3B%0A%2F%2F%20Only%20change%20code%20below%20this%20line.%0Aarray%20%3D%20array.concat(concatMe)%3B%0A%0A%0A%2F%2F%20Only%20change%20code%20above%20this%20line.%0A(function()%20%7Breturn%20array%3B%7D)()%3B%0A" target="_blank">Click here</a> to see the solution on the freeCodeCamp website.


####Instructions:
<p class="wrappable negative-10"><code>.concat()</code> can be used to merge the contents of two arrays into one.</p><p class="wrappable negative-10"><code>array = array.concat(otherArray);</code></p><p class="wrappable negative-10">Use <code>.concat()</code> to concatenate <code>concatMe</code> onto the end of <code>array</code> and assign it back to array.</p><div class="negative-bottom-margin-30"><div id="MDN-links"><p class="negative-10">Here are some helpful links:</p><div class="negative-10"><ul><li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat" target="_blank">Array.concat()</a></li></ul></div></div></div>


####Answer:
```javascript
var array = [1,2,3];

var concatMe = [4,5,6];
// Only change code below this line.
array = array.concat(concatMe);


// Only change code above this line.
(function() {return array;})();

```