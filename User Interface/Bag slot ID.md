Bags are numbered on the right, (4) (3) (2) (1) (0)
Slots in bags are numbered like this:
1 2 3 4
5 6 7 8
9 10 .... etc


Use this macro to find bag slot ID:

/run print(GetMouseFocus():GetParent():GetID()..", "..GetMouseFocus():GetID())