# Code-Wars
This is where I'll post my code wars challenges.
<h2>Challange 1</h2>
Name: Check the exam
<ul>
  <li>kyu: 8</li>
  <li>The first input array is the key to the correct answers to an exam, like ["a", "a", "b", "d"]. The second one contains a student's submitted answers.</li>
  <li>The two arrays are not empty and are the same length. Return the score for this array of answers, giving +4 for each correct answer, -1 for each incorrect answer, and +0 for each blank answer, represented as an empty string (in C the space character is used).</li>
  <li>If the score < 0, return 0.</li>
</ul>
<p>For example:</p>

```
checkExam(["a", "a", "b", "b"], ["a", "c", "b", "d"]) → 6 
checkExam(["a", "a", "c", "b"], ["a", "a", "b",  ""]) → 7
checkExam(["a", "a", "b", "c"], ["a", "a", "b", "c"]) → 16
checkExam(["b", "c", "b", "a"], ["",  "a", "a", "c"]) → 0
```

My Solution:

```
function checkExam(array1, array2) {
  let score = 0;
  for(var i=0;i<array1.length;i++){
    if(array2[i]!=""){
       if(array2[i]==array1[i]){
         score = score + 4;
         } else {
        score = score - 1;
        }        
      } 
    }
  if (score<0){
    score = 0;
  }
   return score  
}  
```

<h2>Challange 2</h2>
Name: Square Every Digit
<ul>
  <li>kyu: 7</li>
  <li>Welcome. In this kata, you are asked to square every digit of a number and concatenate them.</li>
  <li>For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.</li>
  <li>Note: The function accepts an integer and returns an integer
</li>
</ul>

My Solution:

```
function squareDigits(num){
  let splitNum = [...num + ''].map(Number);
  var str = '';
  for(var i=0; i < splitNum.length; i++){
    let squared = Math.pow(splitNum[i], 2);
    str += "" + squared;
  }
  return parseInt(str);
}
```

