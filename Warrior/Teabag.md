## Teabag macro
```
/run if(_g_g_f == nil)then _g_g_f = CreateFrame("frame"); end function _gg() SitOrStand();end; if(_g_g_b == nil) then _g_g_b = 1; _g_g_f:SetScript("OnUpdate", _gg); else _g_g_b = nil; _g_g_f:SetScript("OnUpdate", nil); end
```