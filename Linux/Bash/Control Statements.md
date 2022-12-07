# If
```bash
email=me@example.com
if [[ "$email" =~ [a-z]+@[a-z]{2,}\.(com|net|org) ]]; then
    echo "Valid email!"
else
	echo "Invalid email!"
fi
```

# For
```bash
for v in {1..3}
for ((v=1; v <= 3; v++))
do
	echo "$v"
done
```

```bash
for v in file1 file2
for v in $(ls)
for v in ./*.md
do
	cat "$v"
done
```

# While
```bash
while [ true ]
do
	echo "loop..."
	break
done
```