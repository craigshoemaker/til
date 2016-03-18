# JavaScript RegEx match vs String indexOf

For too many years if I wanted to find out if a string contained a specific string (without using a third party library) I would use `indexOf` like this:

````
var source = 'this is a test of the emergency broadcast system';

if(source.indexOf('emergency') > -1){
  console.log('we have a match!');
}
````

There is another approach using regular expressions that makes the code much more expressive and easy to understand. Using the `match` function is easy and makes your intent much more clear:

````
var source = 'this is a test of the emergency broadcast system';

if(/emergency/.match(source)){
  console.log('we have a match!');
}
````