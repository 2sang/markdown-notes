DOM related notes
=================
#### javascript node
javascript nodes are unique. It cannot be copied dynamically by assigning multiple times.
#### cloneNode()
Painted nodes(such as 'canvas'), and inner texts are not cloned. 
If you need deep copy of the element, give "true" to first parameter.
