# OpsLevelTechDocs


# code blocks


# bash

```bash
#!/bin/bash
function greeting() {

str="Hello, $name"
echo $str

}

echo "Enter your name"
read name

val=$(greeting)
echo "Return value of the function is $val"
```



# HTML
```html
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

# Go
```go
package main

import "fmt"

func MapKeys[K comparable, V any](m map[K]V) []K {
    r := make([]K, 0, len(m))
    for k := range m {
        r = append(r, k)
    }
    return r
}

type List[T any] struct {
    head, tail *element[T]
}

type element[T any] struct {
    next *element[T]
    val  T
}

func (lst *List[T]) Push(v T) {
    if lst.tail == nil {
        lst.head = &element[T]{val: v}
        lst.tail = lst.head
    } else {
        lst.tail.next = &element[T]{val: v}
        lst.tail = lst.tail.next
    }
}

func (lst *List[T]) GetAll() []T {
    var elems []T
    for e := lst.head; e != nil; e = e.next {
        elems = append(elems, e.val)
    }
    return elems
}

func main() {
    var m = map[int]string{1: "2", 2: "4", 4: "8"}

    fmt.Println("keys:", MapKeys(m))

    _ = MapKeys[int, string](m)

    lst := List[int]{}
    lst.Push(10)
    lst.Push(13)
    lst.Push(23)
    fmt.Println("list:", lst.GetAll())
}
```


# GraphQL

```GraphQL
{
   students{
      id
      firstName
      college {
         id
         name
         location
         rating
      }
   }
}
```


# Javascript


```Javascript
console.log('4-fizzbuzz-algorithms');

/* 
<h3>Write a function which checks given input/parameter:</h3>

<ul>
  <li>If input/parameter is divisible by 3 print => Fizz</li>
  <li>If input/parameter is divisible by 5 print => Buzz</li>
  <li>If input/parameter is divisible by 3 or 5 print => FizzBuzz</li>
  <li>If input/parameter is NOT divisible by 3 or 5 print => given Input Number/Value</li>
  <li>If input/parameter is other than Number/Value print => 'Nan - Not a Number! Please Input Number' </li>
</ul>
*/

function isfizzBuzz(arg){
  if(typeof arg !== 'number'){
    return ('Nan - Not a Number! Please Input Number');
  }

  if((arg % 3 === 0) && (arg % 5 === 0)) {
    return 'FizzBuzz';
  }

  if(arg % 3 === 0) {
    return 'Fizz';
  }

  if(arg % 5 === 0) {
    return 'Buzz';
  }

  else {
    return 'Some odd number entered: ' + arg;
  }

}

let checkFizzBuzz1 = isfizzBuzz('one');
console.log(checkFizzBuzz1);

let checkFizzBuzz2 = isfizzBuzz(true);
console.log(checkFizzBuzz2);

let checkFizzBuzz3 = isfizzBuzz(9);
console.log(checkFizzBuzz3);

let checkFizzBuzz4 = isfizzBuzz(10);
console.log(checkFizzBuzz4);

let checkFizzBuzz5 = isfizzBuzz(30);
console.log(checkFizzBuzz5);

let checkFizzBuzz6 = isfizzBuzz(11);
console.log(checkFizzBuzz6);
```




# CSS

```css
body{
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

h1, th{
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}

table{
  /* border: 2px solid #696969;
  border-collapse: collapse; */
  font-size: 18px;
}

th{
  width: 20%;
}

th, td{
  padding: 10px;
  border: 2px solid #696969;
  text-align: center;
}

#freeSquare{
  background-color: coral;
}
```
