Mouseover a action bar button and use this macro to get the ID

/run local a=GetMouseFocus()message(ActionButton_GetPagedID(a))


Here you can see where the actionID slots in your actionbars are:

ActionBar page 1: slots 1 to 12
ActionBar page 2: slots 13 to 24
ActionBar page 3 (Right ActionBar): slots 25 to 36
ActionBar page 4 (Right ActionBar 2): slots 37 to 48
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72