## Toggle Action Bars
hides or shows all the extra action bars
```
/run local s,t="SHOW_MULTI_ACTIONBAR_","HIDE_MULTI_ACTIONBAR_" local x=not getglobal(s.."1") for i=1,4 do setglobal(s..i,x) setglobal(t..i,not x) end MultiActionBar_Update()
```


## Enables all action bars
shows all the extra action bars
```
/run local x=not SHOW_MULTI_ACTIONBAR_1 SHOW_MULTI_ACTIONBAR_1=x SHOW_MULTI_ACTIONBAR_2=x SHOW_MULTI_ACTIONBAR_3=x SHOW_MULTI_ACTIONBAR_4=x UIOptionsFrame:Show() UIOptionsFrame:Hide() ToggleGameMenu();
```