# Shopping Cart Total Exercise

This exercise will have you develop a program that will calculate a shopping cart total.
The program will know the costs of each item in the shopping care and will add them up to produce the total.

## Input

The program should expect an unknown amount of space seperated values to be passed to it's standard input pipe.
An example input file could be

##### cart.txt

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
The price key is in `price-key.txt`.
The format of this file is as follows.

```
{id} {price} {dash seperated name}
```

See `price-key.txt`.

```
1 5.00 bananna
2 0.56 ranch-packet
3 5.45 frozen-pizza
4 25.00 single-barrel-malt-whiskey
5 9.87 12-pack-tecate
6 0.99 gum
7 4.95 bacon
8 1.59 cotton-balls
9 3.33 6-satan-wings
```

Each line has 3 space seperated values.

The first value is the item's ID.
The second value is the price of a single ID's worth of that item.
The third value is a dash seperate textual identifier.

Using this key with the following input.

```
1 1 1 6
```

The total would be 5.00 + 5.00 + 5.00 + 0.99 = 15.99

You can embed this key in your program or read it from the the `price-key.txt` file.
Whatever you do, you have to link these prices with the ID's to perform the calculation.

## Output

Once the total is calculated, you program should write the value to standard out and terminate.
This value should be formatted as a float and should only have 2 decimal places.
The reason for this is because the output is representing a monetary total.

### Valid Outputs

```
3.28
0.98
5.00
.56
7584.38
```

### Invalid Outputs

```
$3.28
5
.56869586
7584.383494
```

## Usage Pattern

```
>$ your-program < cart.txt
13.11
>$
```

In this usage pattern we're using the terminal's file redirection to pipe the contents of cart.txt into your-program's standard input.
You program is expected to function using this usage pattern.
The output in the terminal should look like the above example.

## Errors

If an from the input ID doesn't exist your program should terminate with an exit value of 1.
An exit value of 0 commonly means there were no errors.
A non 0 exit value signifies that the program executed, but something wasn't right.
