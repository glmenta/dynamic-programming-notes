### Dynamic Programming => Optimization Technique;

    => Basically just a buzz-word; "cache" => dynamic programming
    => Break down a big problem into sub problem => store their solutions to use for later in case we need it

### Memoization
```
    Caching => way to store values so we can use them later on;
        => Like a backpack; we hold items that we can grab stuff from later

    Ex: instead of doing:
        fxn addTo80(n) {
            return n + 80
        }

        addTo80(5), addTo80(10).... etc.

        We can use memoization and cache:
        let cache = {};
        fxn memoizedAddTo80(n) {
            if (n in cache) {
                return cache[n];
            } else {
                cache[n] = n + 80;
                return cache[n]
            }
        }

        memoizedAddTo80(5) => we do key:Value pair for it inside our cache
            => so now we can just access that value later;'

        memoization => caching the return value of fxn based on its parameters
            => if parameter does not change, then it is "memoized" b/c it uses the cache we used before
            => remember a solution for a sub-problem

        We can use closures to avoid global scope issues:

        fxn memoizedAddTo80(n) {
            let cache = {};
            return fxn(n) {
                if (n in cache) {
                    return cache[n];
                } else {
                    cache[n] = n + 80;
                    return cache[n]
                }
            }
        }

        const memoized = memoizedAddTo80();
        memoized()
```

### fib() dynamic approach
```
fxn fib(n){
    if (n < 2) {
        return n
    }
    return fib(n-1) + fib(n-2)
}

=> Above fxn is not very efficient; we can use dynamic approach to increase efficiency => less calculations

Dynamic Programming => Divide & Conquer + Memoization

Steps:
1. Can it be divided into subproblems
2. Find recursive solution
3. Are there repetitive subproblems
4. Memoize subproblems

=> Approach fib() with above steps

fxn memoizedFib() {
    let cache = {};
    return fxn fib(n) {
        if (n in cache) {
            return cache[n];
        } else {
            if (n < 2) {
                return n;
            } else {
                cache[n] = fib(n - 1) + fib(n - 2)
                return cache[n];
            }
        }
    }
}

// decreased time complexity to O(n); increased space complexity as a trade-off;

```

```
```

```
```

```
```
