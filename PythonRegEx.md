source: https://www.freecodecamp.org/news/python-regex-tutorial-how-to-use-regex-inside-lambda-expression/

## How to use RegEx inside the Expression of a Lambda Function
`lambda x: re.method(pattern, x)`

## How to use RegEx inside the Expression of a Lambda Function with the filter() Function
```
import re

fruits = ['apple', 'mango', 'banana', 'cherry', 'apricot', 'raspberry', 'avocado']
filtered_fruits = filter(lambda fruit: re.match('^a', fruit), fruits)
print(list(filtered_fruits))
```

## How to use RegEx inside the Expression of a Lambda Function with the map() Function
```
import re

fruits2 = ['opple', 'bonono', 'cherry', 'dote', 'berry']
modified_fruits = map(lambda fruit: re.sub('o', 'a', fruit), fruits2)
print(list(modified_fruits))
```

## How to use RegEx inside the Expression of a Lambda Function with the sort() Method
```
import re

fruits = [ 'banana', 'fig', 'grapefruit']
fruits.sort(key=lambda x: len(re.findall('[aeiou]', x)))
print(fruits) #['fig', 'banana', 'grapefruit']
```
### Reverse:
```
import re

fruits = [ 'banana', 'fig', 'grapefruit']
fruits.sort(key=lambda x: len(re.findall('[aeiou]', x)), reverse=True)
print(fruits) # ['grapefruit', 'banana', 'fig']
```


