# Recursive funtions

function to draw a number of stars to the screen. Note the returns. One is to loop the other(inner) is to return the full string.

```
function drawStars(num, str=""){
  if(num<0) return str;
  
  return drawStars(num - 1, str + "*");
}
```
