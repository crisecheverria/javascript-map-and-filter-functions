# Javascript Map and Filter
Quick example on how replace Loops and use less code with arrays

Take as an example the following array:
```javascript
var frameworks = [
  { name: 'Angular', creator: 'Google' },
  { name: 'ReactJs', creator: 'Facebook' },
  { name: 'VueJs', creator: 'Evan You' }
 ];
```
And if I need to create a new array with only the frameworks creators I have to use a Loop, fo example a For loop:
```javascript
function frameworkCreator(frameworks) {
  const creators = [];
  for (let i = 0; i < frameworks.length; i++) {
    creators.push(frameworks[i].creator);
  }
  return creators;
}
```
Now we just need to call the function recient created
```javascript
function frameworkCreator(frameworks) {
  const creators = [];
  for (let i = 0; i < frameworks.length; i++) {
    creators.push(frameworks[i].creator);
  }
  return creators;
}

var frameworks = [
  { name: 'Angular', creator: 'Google' },
  { name: 'ReactJs', creator: 'Facebook' },
  { name: 'VueJs', creator: 'Evan You' }
 ];

// Print the result in the terminal
console.log(JSON.stringify(frameworkCreator(frameworks)));
```

## Use less code using Map
We can write less code if we use map:
```javascript
function frameworkCreator(frameworks) {
  // New function updated using map
  // Map let us loop trough the array an create a new one
  return frameworks.map(function(framework){
    return framework.creator;
  })
}

// We create a new variable that call the function frameworkCreator and store the new array created by Map.
var creator =  frameworkCreator([
  { name: 'Angular', creator: 'Google' },
  { name: 'ReactJs', creator: 'Facebook' },
  { name: 'VueJs', creator: 'Evan You' }
 ]);

console.log(JSON.stringify(creator));
```
