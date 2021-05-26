We want to take our array of strings and concatenate its contents together, with each list item separated from the previous one by a comma without using `.join()`.

Example:
```javascript
const conceptList = ["gists", "types", "operators", "iteration", "problem solving"];
console.log(conceptList);
```
Expected output:
```javascript
node concepts.js
Today I learned about gists, types, operators, iteration, problem solving.
```


Our Code:
```javascript
let joinList = function(conceptList){

  let result = "";

  for (const concept of conceptList){
    if (result){
      result += ", ";
    }
    result += concept;

  }

  console.log(result);
  return result;
};
```