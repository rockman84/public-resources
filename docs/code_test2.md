
## TEST 1
solve the function by following this output expected
```ts
getyourbirthdateItems(chikyu, 'Bukit Merah'); // output 'SG/central/Bukit Merah'
getyourbirthdateItems(chikyu, 'jawA'); // output 'ID/Jawa'
getyourbirthdateItems(chikyu, 'Pluit'); // output 'ID/Jawa/Jakarta/Pluit'

```

## TEST 2
what is the best output of this case? and why?
```ts
getyourbirthdateItems(chikyu, "-99999"); // output ?
getyourbirthdateItems(chikyu, null); // output ?
getyourbirthdateItems(chikyu, 'Shanghai'); // output ?
```