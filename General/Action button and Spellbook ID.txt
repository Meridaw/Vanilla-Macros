Mouseover a action bar button  and use this macro to get the ID

/run local a=GetMouseFocus()message(ActionButton_GetPagedID(a))


Here you can see where the actionID slots in your actionbars are:

ActionBar page 1: slots 1 to 12
ActionBar page 2: slots 13 to 24
ActionBar page 3 (Right ActionBar): slots 25 to 36
ActionBar page 4 (Right ActionBar 2): slots 37 to 48
ActionBar page 5 (Bottom Right ActionBar): slots 49 to 60
ActionBar page 6 (Bottom Left ActionBar): slots 61 to 72



Find SpellBookID (replace SpellName in "SpellName")

/script for id = 1, 180, 1 do local spellName, subSpellName = GetSpellName(id, SpellBookFrame.bookType);if spellName and string.find(spellName, "SpellName", 1, true) then ChatFrame1:AddMessage("ID is "..id, 1.0, 1.0, 0.5); end; end;



If you want to test you have the right spell type this into the chat window (replace X with the number you want to test)

/script DEFAULT_CHAT_FRAME:AddMessage(GetSpellName(X,0)); 



Bags are numbered on the right, (4) (3) (2) (1) (0)
Slots in bags are numbered like this:
1 2 3 4
5 6 7 8
9 10 .... etc


Can also use this macro to find bag slot ID:

/run print(GetMouseFocus():GetParent():GetID()..", "..GetMouseFocus():GetID())



In the inventory, the slots are numbered like this:
1_______10
2_______6
3_______7
15______8
4_______11
5_______12
19______13
9_______14
16 17 18