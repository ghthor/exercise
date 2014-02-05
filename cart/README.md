# Shopping Cart Total Exercise

This exercise will have you develop a program that will calculate a shopping cart total.
The program will know the costs of each item in the shopping care and will add them up to produce the total.

## Input

The program should expect an unknown amount of space seperated values to be passed to it's standard input pipe.
An example input file could be

### cart.txt

```
10 4 4 4 10 1 4 3 8 9
```

This input mean the cart contains these items.

- 2x ID(10)
- 4x ID(4)
- 1x ID(1)
- 1x ID(3)
- 1x ID(8)
- 1x ID(9)

You program will lookup the price values for each of these ID's and add it up for a cart total.

## Output

Once the total is calculated, you program should write the value to standard out and terminate.
This value should be formatted as a float and should only have 2 decimal places, since it is money.

### Usage Pattern

```
>$ your-program < cart.txt
13.11
>$
```

In this usage pattern we're using the terminal's redirection pipe to pipe the contents of cart.txt into your-program's standard input.
You program is expected to function using this usage pattern.
The output in the terminal should look like the above example.

## Errors

If an from the input ID doesn't exist your program should terminate with an exit value of 1.
An exit value of 0 commonly means there were no errors.
A non 0 exit value signifies that the program executed, but something wasn't right.
