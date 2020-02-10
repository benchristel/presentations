# Three Ways Functional Programming Can Make Your Life Better

1. Lists
2. Null values
3. Asynchronous operations

```javascript
function start(value) {
  return {
    and(func) {
      return start(func(value))
    },
    done() {
      return value
    }
  }
}
```

```javascript
function addOne(x) {
  return x + 1
}

function double(x) {
  return 2 * x
}

start(1)
  .and(addOne)
  .and(double)
  .and(addOne)
  .done()
```

# Some code that iterates over a list and builds a new list

```javascript
let input = ["1", "2", "3"]
let output = []
for (let i = 0; i < input.length; i++) {
  let parsed = parseInt(input[i])
  output.push(parsed)
}

// at this point, output == [1, 2, 3]
```

`map` takes a function that works on a single value and upgrades it to work on lists.

```javascript
function map(scalarFunc) {
  return function(list) {
    var results = []
    for (var i = 0; i < list.length; i++) {
      results.push(scalarFunc(list[i]))
    }
    return results
  }
}
```

# 

```javascript
function safelyAddOne(x) {
  if (x === null) {
    return null
  } else {
    return x + 1
  }
}
```

maybeMap takes a function that works on a value and upgrades it to work on values that might be null

```javascript
let addOne = x => x + 1

let safelyAddOne = ifPresent(addOne)
```

promiseMap takes a function that works on a value and upgrades it to work on promises that yield that type of value

```javascript
start(httpGet('google.com'))
  .and(then(parseXml))
  .and(then(findH1Elements))
  .and(then(map(toUpperCase)))
  .and(then(reduce(joinBy(', '))))
  .done()
```

If your network is one of the unreliable ones, you can do:

```javascript
start(httpGet('google.com'))
  .and(then(safely(parseXml)))
  .and(then(safely(findH1Elements)))
  .and(then(safely(map(toUpperCase))))
  .and(then(safely(reduce(joinBy(', ')))))
  .done()
```

Why are these things important?

You can now write and unit-test the bulk of your logic pretending that:

- values can't be null
- you only have scalars, not lists of things
- everything is synchronous
