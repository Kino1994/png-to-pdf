```
n=1; for file in *.png; do mv "$file" "$n.png"; ((n++)); done

for i in $(seq 1 $(ls -l *.png | wc -l)); do
  convert "$i.png" "$i.pdf"  # Replace with your command for .ptk conversion
done

pdftk $(ls -1v *.pdf) cat output merged_output.pdf
```
