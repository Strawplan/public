# Removing Smart Quotes

- To remove smart quotes use:
```
#!

sqo=$(echo -ne '\u2018')
sqc=$(echo -ne '\u2019')

sed -i "s/${sqo}/\'/g" "${1}"
sed -i "s/${sqc}/\'/g" "${1}"

dqo=$(echo -ne '\u201C')
dqc=$(echo -ne '\u201D')

sed -i "s/${dqo}/\"/g" "${1}"
sed -i "s/${dqc}/\"/g" "${1}"
```

