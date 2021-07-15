# YAML
YAML stands for YAML Ain't Markup Language. It is super set of JSON. Therefore every JSON can convert to YAML but not the way around.

### Feature
```yaml
#Document separator
---

#Map
key : value

#Nested map
parent_key :
  child_key1 : value1
  child_key2 : value2

#Sequence
list_of_sth
 - first_item
 - second_item
 - thrid_item

- Mutiline newline : |
   this is consider and newline
   and "Newline" character is preserve


- Folded string : >
   this is consider as folded string
   newline'll be replaced by space 
```