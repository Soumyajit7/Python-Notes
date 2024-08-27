The `random` library in Python is used to generate pseudo-random numbers for various distributions and perform random operations. Here are some of the key functions and their uses:

### Basic Functions
1. **`random()`**:
    - Returns a random float number between 0.0 and 1.0.
    ```python
    import random
    print(random.random())  # Output: e.g., 0.37444887175646646
    ```

2. **`seed(a=None, version=2)`**:
    - Initializes the random number generator. If `a` is omitted or `None`, the current system time is used.
    ```python
    random.seed(10)
    print(random.random())  # Output: e.g., 0.5714025946899135
    ```

3. **`getstate()` and `setstate(state)`**:
    - `getstate()` returns the current internal state of the random number generator.
    - `setstate(state)` restores the internal state.
    ```python
    state = random.getstate()
    random.setstate(state)
    ```

### Integer Functions
1. **`randint(a, b)`**:
    - Returns a random integer between `a` and `b` (inclusive).
    ```python
    print(random.randint(1, 10))  # Output: e.g., 7
    ```

2. **`randrange(start, stop[, step])`**:
    - Returns a randomly selected element from `range(start, stop, step)`.
    ```python
    print(random.randrange(1, 10, 2))  # Output: e.g., 3
    ```

3. **`getrandbits(k)`**:
    - Returns a random integer with `k` random bits.
    ```python
    print(random.getrandbits(4))  # Output: e.g., 9
    ```

### Sequence Functions
1. **`choice(seq)`**:
    - Returns a random element from the non-empty sequence `seq`.
    ```python
    print(random.choice(['apple', 'banana', 'cherry']))  # Output: e.g., 'banana'
    ```

2. **`choices(population, weights=None, *, cum_weights=None, k=1)`**:
    - Returns a list of `k` elements chosen from the population with optional weights.
    ```python
    print(random.choices(['apple', 'banana', 'cherry'], k=2))  # Output: e.g., ['cherry', 'apple']
    ```

3. **`shuffle(x[, random])`**:
    - Shuffles the sequence `x` in place.
    ```python
    fruits = ['apple', 'banana', 'cherry']
    random.shuffle(fruits)
    print(fruits)  # Output: e.g., ['cherry', 'apple', 'banana']
    ```

4. **`sample(population, k)`**:
    - Returns a list of `k` unique elements chosen from the population.
    ```python
    print(random.sample(['apple', 'banana', 'cherry'], 2))  # Output: e.g., ['banana', 'cherry']
    ```

### Real-valued Distributions
1. **`uniform(a, b)`**:
    - Returns a random float number between `a` and `b`.
    ```python
    print(random.uniform(1.0, 10.0))  # Output: e.g., 7.123456789
    ```

2. **`triangular(low, high, mode)`**:
    - Returns a random float number between `low` and `high` with the specified mode.
    ```python
    print(random.triangular(1.0, 10.0, 5.0))  # Output: e.g., 4.567890123
    ```

3. **`betavariate(alpha, beta)`**:
    - Returns a random float number between 0 and 1 based on the Beta distribution.
    ```python
    print(random.betavariate(2, 5))  # Output: e.g., 0.345678901
    ```

4. **`expovariate(lambd)`**:
    - Returns a random float number based on the Exponential distribution.
    ```python
    print(random.expovariate(1.5))  # Output: e.g., 0.456789012
    ```

5. **`gammavariate(alpha, beta)`**:
    - Returns a random float number based on the Gamma distribution.
    ```python
    print(random.gammavariate(2, 2))  # Output: e.g., 3.456789012
    ```

6. **`gauss(mu, sigma)`**:
    - Returns a random float number based on the Gaussian distribution.
    ```python
    print(random.gauss(0, 1))  # Output: e.g., -0.123456789
    ```

7. **`lognormvariate(mu, sigma)`**:
    - Returns a random float number based on a log-normal distribution.
    ```python
    print(random.lognormvariate(0, 1))  # Output: e.g., 1.234567890
    ```

8. **`normalvariate(mu, sigma)`**:
    - Returns a random float number based on the normal distribution.
    ```python
    print(random.normalvariate(0, 1))  # Output: e.g., 0.123456789
    ```

9. **`vonmisesvariate(mu, kappa)`**:
    - Returns a random float number based on the von Mises distribution.
    ```python
    print(random.vonmisesvariate(0, 1))  # Output: e.g., 0.234567890
    ```

10. **`paretovariate(alpha)`**:
    - Returns a random float number based on the Pareto distribution.
    ```python
    print(random.paretovariate(1))  # Output: e.g., 1.345678901
    ```

11. **`weibullvariate(alpha, beta)`**:
    - Returns a random float number based on the Weibull distribution.
    ```python
    print(random.weibullvariate(1, 1.5))  # Output: e.g., 0.567890123
    ```