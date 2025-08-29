
## TEST 1
solve the function by following this output expected
```js
getyourbirthdateItems(chikyu, 'Bukit Merah'); // output 'SG/central/Bukit Merah'
getyourbirthdateItems(chikyu, 'jawA'); // output 'ID/Jawa'
getyourbirthdateItems(chikyu, 'Pluit'); // output 'ID/Jawa/Jakarta/Pluit'

```

## TEST 2
what is the best output of this case? and why?
```js
getyourbirthdateItems(chikyu, "-99999"); // output ?
getyourbirthdateItems(chikyu, null); // output ?
getyourbirthdateItems(chikyu, 'Shanghai'); // output ?
```

## Objective
- Correct output
- clean code
- how to reuse funcionality
- optimize logic code
- how to handling incorrect input? (Test 2)

## Scoring
- below 20 lines code -> very good he is pro
- below 40 lines code -> Average
- more 40 lines code -> Junior

```js
function getyourbirthdateItems(data, targetId) {
    targetId = targetId.toLowerCase();
    function dfs(node, path) {
        if (node.id.toLowerCase() === targetId) {
            return [...path, node.id].join("/");
        }
        if (node.items) {
            for (const child of node.items) {
                const res = dfs(child, [...path, node.id]);
                if (res) return res;
            }
        }
        return null;
    }
    for (const root of data) {
        const result = dfs(root, []);
        if (result) return result;
    }
    return "N/A";
}
```