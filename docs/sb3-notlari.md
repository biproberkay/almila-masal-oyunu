# Scratch SB3 Notları

## SB3 yapısı

.sb3 dosyası aslında ZIP arşividir.

İçerik:
- project.json
- SVG / PNG sprite dosyaları
- Ses dosyaları

## Kritik kurallar

- project.json root seviyede olmalı
- JSON hatasız olmalı
- Sprite id ve referanslar tutarlı olmalı

## Temas (collision) problemi

Scratch'te en stabil yöntem:

Teması hedef objenin içinde kontrol etmek

Örnek:

Star sprite:

```
when green flag clicked
forever
  if touching [Almila]
    change score by 1
    hide
```

## Seviye sistemi

Değişken:

```
level = 1
```

Geçiş:

```
if score > 5
  change level by 1
  switch backdrop
```

## Not

SB3 üretimi otomatikleştirilebilir (ileride tool yazılabilir).
