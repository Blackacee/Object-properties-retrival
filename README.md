# Object-properties-retrival

//Ex 1 : Simple data
var x = { a : 10 , b : 3} , props = [];
for(prop in x){
 props.push(prop);
}
console.log(props); //["a","b"]
//Ex 2 : Data with enumerable properties in prototype chain
var x = { a : 10 , __proto__ : { b : 10 }} , props = [];
for(prop in x){
 props.push(prop);
}
console.log(props); //["a","b"]
//Ex 3 : Data with non enumerable properties
var x = { a : 10 } , props = [];
Object.defineProperty(x, "b", {value : 5, enumerable : false});
for(prop in x){
 props.push(prop);
}
console.log(props); //["a"]
