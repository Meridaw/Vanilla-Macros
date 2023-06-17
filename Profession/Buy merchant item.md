## Buys 40 Arcane Powder
```
/run local function buy (n,q) for i=1,100 do if n==GetMerchantItemInfo(i) then BuyMerchantItem(i,q) end end end buy ("Arcane Powder",40);
```