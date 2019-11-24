# Scrabble

Write a program that will replicate the scoring system in Scrabble. The function should take a single argument (the word, comprised of letters/tiles) and return a score. 

## Letter Values

You'll need these:

```plain
Letter                           Value
A, E, I, O, U, L, N, R, S, T       1
D, G                               2
B, C, M, P                         3
F, H, V, W, Y                      4
K                                  5
J, X                               8
Q, Z                               10
```

So now that you've got those letter values, consider what data structure is good for mapping keys to values?

## Examples
"cabbage" should be scored as worth 14 points:

- 3 points for C
- 1 point for A, twice
- 3 points for B, twice
- 2 points for G
- 1 point for E

And to total:

- `3 + 2 * 1 + 2 * 3 + 2 + 1`
- = `3 + 2 + 6 + 3`
- = `5 + 9`
- = 14

## Double Check
http://www.dvorkin.com/scrabscor.php

// js

// Letter                           Value
// A, E, I, O, U, L, N, R, S, T       1
// D, G                               2
// B, C, M, P                         3
// F, H, V, W, Y                      4
// K                                  5
// J, X                               8
// Q, Z                               10

 function calculate(word) {
const obj = {
  
  1: ["A","E","I","O","U","L","N","R","S","T"],
  2: ["D","G"],
  3: ["B","C","M","P"],
  4: ["F","H","V","W","Y"],
  5: ["K"],
  8: ["J","X"],
  10: ["Q","Z"]
  
}

var cap = word.toUpperCase();
var arr = cap.split("");
   var total =0;
   
// console.log(arr);
   
 for (let i in obj){
   
   for(j=0;j<obj[i].length;j++ ){
//      console.log(arr[j]);
   if(arr[i]==obj[i][j]){
     //console.log("hi");
   total += Number(i) ;

}
  }
   }
  
   console.log(total);
}




calculate ("cabbage");

