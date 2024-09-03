# DSL Torch Language

---

**Available file in Torch language**

---

```torch
// calc factorial
func factorial(n) {
  let num = 1
  let i = 1
  while( i <= n ) {
    num = num * i
    i = i + 1
  }
  return num
}

// calc fibonacci sum
func calcFibonacciSum(n) {
  let a = 0
  let b = 1
  let fibSum = 0

  if (n == 0) {
    return a
  }
  if (n == 1) {
    return fibSum
  }
  let i = 2
  while (i <= (n + 1)) {
    fibSum = fibSum + b
    let temp = a
    a = b
    b = temp + b
    i = i + 1
  }
  return fibSum
}

// test function
func test(res, expected) {
  let ans = 0

  if(res == expected) {
    ans = 1
    return ans
  }

  return ans
}

let fib = calcFibonacciSum(5) // fibonacci
let fac = factorial(6) // factorial

test(fac + fib, 720 + 12)
