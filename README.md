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

        We can use memoization and cache
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
```

```
```

```
```

```
```

```
```
