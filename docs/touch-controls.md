# Dokunmatik Kontroller

Bu sürümde oyun klavyeye bağımlı olmadan tablet/telefon ekranından oynanabilecek hale getirilir.

## Hedef

Sahnede üç büyük kontrol butonu bulunur:

- Sol Buton: Almila sola gider
- Sağ Buton: Almila sağa gider
- Zıpla Buton: Almila zıplar

## Tasarım

Butonlar sahnenin alt kısmına yerleştirilir:

- Sol: sol alt
- Sağ: sol altın biraz sağı
- Zıpla: sağ alt

Bu düzen mobil oyunlardaki klasik kontrol hissine yakındır.

## Scratch mantığı

Buton sprite'ları şu mantıkla çalışır:

```
forever
  if mouse down and touching mouse-pointer
    broadcast TouchLeft / TouchRight / TouchJump
    wait 0.05 seconds
```

Almila sprite'ı bu mesajları dinler:

```
when I receive TouchLeft
  change x by -8

when I receive TouchRight
  change x by 8

when I receive TouchJump
  repeat 7
    change y by 10
  repeat 7
    change y by -10
```

## Not

Scratch tarayıcıda dokunmatik girişi çoğu durumda mouse-pointer gibi işler. Bu yüzden butonlar hem tıklama hem dokunma için tasarlanmıştır.
