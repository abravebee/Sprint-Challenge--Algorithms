*Exercise I*
a) O(n) - Linear Time
    If the loop stops when a => n^3, then it should run linearly according to n.
    
    n = 1 will run once because 
    first loop: `a = 0 + 1 * 1 = 1`
    break: `1 = 1 * 1 * 1`

    n = 2 will run twice because 
    first loop: `a = 0 + 2 * 2 = 4`
    continue: `4 < 2 * 2 * 2`
    second loop: `a = 4 + 2 * 2 = 8`
    break: `8 = 2 * 2 * 2`
    
    n = 3 will run three times because
    first loop: `a = 0 + 3 * 3 = 9`
    continue: `9 < 3 * 3 * 3`
    second loop: `a = 9 + 3 * 3 = 18`
    continue: `18 < 3 * 3 * 3`
    third loop: `a = 18 + 3 * 3 = 27`
    break: `27 = 3 * 3 * 3`

    Etcetera!

b) O(n^4) - Quadratic Time
    There are three nested loops relying on n, and a fourth relying on k, which grows along with n, so this exponential growth seems to be to the 4th power as opposed to the 3rd.

c) O(n) - Linear Time
    It's going to recursively call itself for the amount of bunnies input, until there are 0.

*Exercise II*
Binary search time. Drop first egg from halfway up. If it breaks, drop second egg from remaining floors one-by-one until we find the floor it breaks on. Worst case scenario, this involves dropping the egg half of n, minus the one we already dropped it from.

If it doesn't break, all the floors below are safe, and we go halfway up again. I suppose you could probably use a recursive approach here, since we'd be repeating the steps in the first paragraph until the floor is found.

Binary search is O(log n).