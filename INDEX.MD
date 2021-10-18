```python
 name = "ada lovelace"
print(name.title())#Ada Lovelace
print(name.upper())#ADA LOVELACE
print(name.lower())#ada lovelace
```
`title()` displays each word in titlecase, where each word begins with a capital letter. 
To add a tab to your text, use the character combination `\t`
`\n\t` tells Python to move to a new line

### LISTS
```py
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles)
print(bicycles[0].title())# 'Trek' is capitalized.
```
Index Positions Start at 0, Not 1

for the item at index -1, Python always returns the last item in the list:
#### Modifying Elements in a List
```py
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)#['honda', 'yamaha', 'suzuki']
motorcycles[0] = 'ducati'
print(motorcycles)#['ducati', 'yamaha', 'suzuki']

```
#### Appending Elements to the End of a List
```py
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)#['honda', 'yamaha', 'suzuki']
motorcycles.append('ducati')
print(motorcycles)#['honda', 'yamaha', 'suzuki', 'ducati']

```
### Removing Elements from a List
```py
motorcycles.insert(0, 'ducati')#Inserting Elements into a List 
motorcycles.remove('ducati')#Removing an Item by Value
popped_motorcycle = motorcycles.pop() #Removing an Item Using the pop() Method
del motorcycles[0] #Removing an Item Using the del Statement

```

