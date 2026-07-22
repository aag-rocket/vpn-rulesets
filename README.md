# vpn-rulesets

Custom sing-box rule-sets для Karing VLESS-каскада (RU→DE).

## via-ru-srv

Домены, которым нужен выход через **RU-ноду** (в туннель, перебивает `geoip:ru→direct`).
Используется в группе диверсии `🎯 amxeox → туннель` выше Russia.

- `src/via-ru-srv.json` — исходник (sing-box rule-set, **version 1** для Karing)
- `via-ru-srv.srs` — скомпилированный binary (SRS v1)

Raw URL для Karing rule_set_item:
```
https://raw.githubusercontent.com/aag-rocket/vpn-rulesets/main/via-ru-srv.srs
```

### Обновление
Правишь `src/via-ru-srv.json` → компилишь → push. Karing подтянет по update_interval.
```
sing-box rule-set compile --output via-ru-srv.srs src/via-ru-srv.json
```
