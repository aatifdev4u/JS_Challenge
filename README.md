# JS_Challenge
## 1.Converting as array of object to object?
###### Input 
```
const peopleArray = [
  { id: 123, name: "dave", age: 23 },
  { id: 456, name: "chris", age: 23 },
  { id: 789, name: "bob", age: 23 },
  { id: 101, name: "tom", age: 23 },
  { id: 102, name: "tim", age: 23 }
]
```
###### Expected Output
```
const peopleObject = {
  "123": { id: 123, name: "dave", age: 23 },
  "456": { id: 456, name: "chris", age: 23 },
  "789": { id: 789, name: "bob", age: 23 },
  "101": { id: 101, name: "tom", age: 23 },
  "102": { id: 102, name: "tim", age: 23 }
}
```

###### Soln 
```
const arrayToObject = (array) => {
	array.reduce((object, item)=>
		object[item.id] = item;
		return object;
	, {})
}

const peopleObject =  arrayToObject(peopleArray);
```
## 3.Using the reduce() method, how would you sum up the population of every country except China?
###### Input 
```
let data = [
  {
    country: 'China',
    pop: 1409517397,
  },
  {
    country: 'India',
    pop: 1339180127,
  },
  {
    country: 'USA',
    pop: 324459463,
  },
  {
    country: 'Indonesia',
    pop: 263991379,
  }
]
```
###### Expected Output
```

```

###### Soln 
```
const totalPopluation = data.reduce((acc, cv) => {
	return cv.country === 'China' ? acc : acc + cv.pop;
}, 0);
```
## 3. Counting instances of values in an object?
###### Input 
```
var names = ['Alice', 'Bob', 'Tiff', 'Bruce', 'Alice'];
```
###### Expected Output
```
// countedNames is:
// { 'Alice': 2, 'Bob': 1, 'Tiff': 1, 'Bruce': 1 }
```

###### Soln 
```
var countedNames = names.reduce(function (allNames, name) { 
  if (name in allNames) {
    allNames[name]++;
  }
  else {
    allNames[name] = 1;
  }
  return allNames;
}, {});
```
## 4. Grouping objects by a property?
###### Input 
```
var people = [
  { name: 'Alice', age: 21 },
  { name: 'Max', age: 20 },
  { name: 'Jane', age: 20 }
];
```
###### Expected Output
```
 groupedPeople is:
 { 
   20: [
    { name: 'Max', age: 20 }, 
     { name: 'Jane', age: 20 }
   ], 
   21: [{ name: 'Alice', age: 21 }] 
 }
```

###### Soln 
```
function groupBy(objectArray, property) {
  return objectArray.reduce(function (acc, obj) {
    var key = obj[property];
    if (!acc[key]) {
      acc[key] = [];
    }
    acc[key].push(obj);
    return acc;
  }, {});
}

var groupedPeople = groupBy(people, 'age');

```
## 5.Flatten an array of arrays?
###### Input 
```
[[0, 1], [2, 3], [4, 5]]
```
###### Expected Output
```
[0, 1, 2, 3, 4, 5]
```

###### Soln 
```
var flattened = [[0, 1], [2, 3], [4, 5]].reduce(
  function(accumulator, currentValue) {
    return accumulator.concat(currentValue);
  },
  []
);
```
## 6.
###### Input 
```

```
###### Expected Output
```

```

###### Soln 
```

```
## 7.
###### Input 
```

```
###### Expected Output
```

```

###### Soln 
```

```
