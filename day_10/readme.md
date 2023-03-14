# Write a function to remove array element based on object property?
* How to remove array element based on object property?


<h2>Challenges (0/3 done)</h2>


  - [X] removeArrayElement("money") returns the array without the money object
  - [X] removeArrayElement("id") returns the array without the id object
  - [X] removeArrayElement("cStatus") returns the array without the cStatus object

```
const array = [
    { field: "id", operator: "eq" },
    { field: "cStatus", operator: "eq" },
    { field: "money", operator: "eq" },
];

const filterField = "money"

function removeArrayElement(filterField) {
    // write your solution here
    var arr = array.filter(function (obj) {
        return obj.field !== filterField;
    });

    return arr;
}

console.log(`filtered array: ${removeArrayElement(filterField)}`)


```

