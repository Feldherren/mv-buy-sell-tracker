# Bought and Sold Item Tracker v1.0.0, by Feldherren (rpaliwoda AT googlemail.com)
 
## Changelog
1.0.0: initial commit

## Description
 
Tracks items bought and sold to shops, under specified labels.
To use, prior to using a Shop Processing event command, use the
TRACKSHOP [label] plugin command and provide some kind of label
to identify this shop with. All purchases made until the 
UNTRACKSHOP or TRACKSHOP [label] commands are used again (the
latter with a different label).

Data for a given label can be reset with the 
RESETTRACKEDSHOP [label] command.

Stored data can be retrieved to specified variables with the
GETTRACKEDDATA command.

## Plugin commands:
### TRACKSHOP [label]
Sets the plugin to track all items bought and sold under the label supplied.
The label may be a string.
### UNTRACKSHOP
Stops tracking items bought and sold.
### RESETTRACKEDSHOP [label]
Resets tracked items for label.
### GETTRACKEDDATA [label] [item|weapon|armor] [bought|sold] [id] [variable]
Outputs the number of copies of an item, weapon or armour that have been 
bought or sold whilst tracking was active with the specified label to the
specified variable.