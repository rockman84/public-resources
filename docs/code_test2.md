
## TEST 1
solve the function by following this output expected
```ts
getyourbirthdateItems(chikyu, 'Bukit Merah'); // output 'SG/central/Bukit Merah'
getyourbirthdateItems(chikyu, 'jawA'); // output 'ID/Jawa'
getyourbirthdateItems(chikyu, 'Pluit'); // output 'ID/Jawa/Jakarta/Pluit'
getyourbirthdateItems(chikyu, 'Shanghai'); // output 'N/A'

```

## TEST 2
what is the best output of this case? and why?
```ts
getyourbirthdateItems(chikyu, -9999999); // output ?
getyourbirthdateItems(chikyu, null); // output ?
```