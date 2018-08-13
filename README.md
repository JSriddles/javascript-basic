# javascript-basic
Basic javascript riddles

## answers should be in native javascript
No typescript/jquery/etc. required

### level easy
1. Implement a function `sum` which can be used in 2 ways:
```
sum(5,6);       // should return 11
sum(5)(6);      // should return 11
```

### level medium
1. See the following `html` page
    - What will be printed to the console if Button 1 is clicked, and why?
    - How would you solve this issue?
```
<!DOCTYPE html>
<html>
<head>
    <title>Buttons fun stuff</title>
</head>
<body>
    <button>Button 1</button>
    <button>Button 2</button>
    <button>Button 3</button>
    <script>
        const nodes = document.querySelectorAll('button');
        for (var i = 0; i < nodes.length ; i++ ) {
            nodes[i].addEventListener('click' , function() {
                console.log('button ' + i +  ' clicked');
            });
        }
    </script>
</body>
</html>
```

2. what should we assign to `level` so this code will return `true`?
```
const levels = {
  'easy': 1,
  'medium': .1,
  'hard': .001
}

const level = ???;

function foo() {
    if(!levels[level]){
      level = 'medium';
    }

    random = Math.random();

    if(random < levels[level]){
      return false;
    }
    else if(random > levels[level]){
      return false;
    }
    else if(random == levels[level]){
      return false;
    }

    return true;
}
```

### level hard
1. Implement a function `math` which accept up to 3 parameters:
```
function math(a, b, type) {
    // TODO: implement
}
```

math can be used in serveral ways (expecte return value appear after the `//`)
```
console.log(math(1,2, { type: 'add' })); // 3
console.log(math(1,2, { type: 'sub' })); // -1
console.log(math(1,2, { type: 'foo' })); // 0
console.log(math(1,2, { typo: 'sub' })); // 3
console.log(math(1,2, {  })); // 3
console.log(math(1,2)); // 3
console.log(math(1)); // 1
console.log(math()); // 0
```
Note that:
```
// ('foo' is not a valid type)
console.log(math(1,2, { type: 'foo' }));

// ('typo' is not a valid property)
console.log(math(1,2, { typo: 'sub' }));
 ```

