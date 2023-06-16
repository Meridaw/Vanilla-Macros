## Switches between actionbar page 1 and 2
```
/run if (CURRENT_ACTIONBAR_PAGE == 1) then CURRENT_ACTIONBAR_PAGE = 2; else CURRENT_ACTIONBAR_PAGE = 1; end; ChangeActionBarPage();
```


## Change actionbar
```
/run if (CURRENT_ACTIONBAR_PAGE == 1) then CURRENT_ACTIONBAR_PAGE = 2; ChangeActionBarPage();  elseif(CURRENT_ACTIONBAR_PAGE == 2) then CURRENT_ACTIONBAR_PAGE = 1; ChangeActionBarPage(); end;
```