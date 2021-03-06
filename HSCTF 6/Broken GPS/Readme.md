# Broken GPS

## __Decription__

Ella is following a broken GPS. The GPS tells her to move in the opposite direction than the one she should be travelling in to get to her destination, and she follows her GPS exactly. For instance, every time she is supposed to move west, the GPS tells her to move east and she does so. Eventually she ends up in a totally different place than her intended location. What is the shortest distance between these two points? Assume that she moves one unit every time a direction is specified. For instance, if the GPS tells her to move "north," she moves one unit north. If the GPS tells her to move "northwest," then she moves one unit north and one unit west.

__Input Format:__

You will receive a text file with N directions provided to her by the GPS (the ones that she will be following) (1<=N<=1000). The first line in the file will be N, and each consequent line will contain a single direction: “north,” “south,” “east,” “west,” “northwest,” “northeast,” “southwest,” or “southeast.”

__Output Format:__

Round your answer to the nearest whole number and then divide by 26. Discard the quotient (mod 26). Each possible remainder corresponds to a letter in the alphabet. (0=a, 1=b… 25=z).
Find the letter for each test case and string them together. The result is the flag. (For instance, a, b, c becomes “abc”). Remember to use the flag format and keep all letters lowercase!

## __Solution__

This challenge is like a programming challenge.

I set the initial position at x=0, y=0.

Parsing the whole files, whenever it encounters 'east' in the text, add 1 to x. The 'west's take 1 from x. 'south' and 'north' are the same for y.

```
for line in f:
    if 'east' in line:
        x += 1
    if 'west' in line:
        x -= 1
    if 'north' in line:
        y += 1
    if 'south' in line:
        y -= 1
```

Finally, calculate 2\*sqrt(x^2+y^2), round it to interger and divide it by 26.

Repeating the process for the 10 files give us the answer

```
garminesuckz
```

The flag is ```hsctf{garminesuckz}```
