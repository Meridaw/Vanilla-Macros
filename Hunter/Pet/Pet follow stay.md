## One button pet follow/stay
```
/run local _,_,_,_,x = GetPetActionInfo(2); if x then PetWait() else PetFollow() end
```