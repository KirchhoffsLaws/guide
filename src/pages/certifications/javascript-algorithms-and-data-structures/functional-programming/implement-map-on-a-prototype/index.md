---
title: Implement map on a Prototype
---
## Implement map on a Prototype

// the global Array
var s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
  // reference the array object with "this."
  // this.forEach() calls the forEach() method on the array (this. array)
  // forEach(function(element) {some code}) is the basic syntax of the forEach() method. It takes each 'element' (or however you want to
  // call it) in the array, performs {some code} and moves on to the next element in the array.
  // callback is a parameter but also a function that will be passed into the myMap() method we're creating
  // let currVal = callback(x) creates a variable within the scope of our block. It assigns the value of callback(x) (remember callback is
  // a function passed as an argument to myMap()). x is what we call the current element of the array, passed to us by the forEach() method
  // we push the new value into a newArray which was defined for us previously
  
  this.forEach(function(x) {
    let currVal = callback(x);
    newArray.push(currVal);
  })
  // Add your code above this line
  return newArray;

};

var new_s = s.myMap(function(item){
  return item * 2;
});
