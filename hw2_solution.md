# Part 1
```sh
sed -E 's/^>[^A-Z]*([A-Z])[^_]*_([^0-9_]*).*_([0-9]+)_([A-Z]{3})[A-Z]*/>\1._\2_\3_\4/' hw2_data.txt > reformatted.txt
```
# Use regular expressions that are general and use capture groups to reformat your data. For example:
Find: `^>[^A-Z]*([A-Z])[^_]*_([^0-9_]*).*_([0-9]+)_([A-Z]{3})[A-Z]*`
Replace: `>\1._\2_\3_\4`

# Part 2

```sh
grep ">" hw2_data.txt | sed -E 's/^>[^A-Z]*([A-Z])[^_]*_([^0-9_]*).*_([0-9]+)_([A-Z]{3})[A-Z]*/\3:\4/' > reformatted2.txt
```
