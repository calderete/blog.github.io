---
layout: default
---

# World Object
_has many **pets**_

### Attributes
+ Active

## Pet Object
_has many **Items**_
_belongs to **World**_

### Attributes
+ Pet Level _int_
+ Primary power _int_
+ Primary defense _int_
+ Active _boolean_

## Item Object
_has many **Mods**_
_belongs to **Pet**_

### Attributes
+ Object Level _int_
+ Stat Mod Objects _list of mods_
+ Active _boolean_

## Stat Mod Object
_belongs to **Item**_

### Attributes
+ Item Attribute Modified _example: Primary Power, or Primary Defense_
+ Mod Level _default: 1, this will affect entire roll of mod_
+ Mod Type _elemental types such as fire, stone ect.._
+ Initiative _time to take effect after execution_
+ Ranges _if a defense mod and range is set high it will protect against ranged attacks_
+ Active _boolean_
