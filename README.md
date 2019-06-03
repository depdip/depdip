# 1 ile 1000 arası sayıyı tahmin etme oyunu..


import time
import random

hak_sayisi = 10
rastgele_sayi = random.randint(1,1000)

while True:
    tahmin = int (input ( "Lütfen Bir Sayı Giriniz"))

    if tahmin < rastgele_sayi:
        print("Lütfen Bekleyiniz")
        time.sleep(1)
        print("Biraz Daha Yüksek Sayi")
        print("Kalan Tahmin Sayınız",hak_sayisi)
        hak_sayisi -= 1

    elif tahmin > rastgele_sayi:
        print("Lütfen Bekleyiniz:")
        time.sleep(1)
        print("Biraz Daha Düşük Sayi")
        print("Kalan Tahmin Sayınız:",hak_sayisi)
        hak_sayisi -= 1

    else:
        print("Lütfen Bekleyiniz")
        time.sleep(1)
        print("Tebrikrel Doğru Bilginiz!")
        break

    if hak_sayisi == 0:
        print("Üzgünüm Haklarınız Bitti Uygulamayı Tekrardan Başlatmak İçin Reseyleyiniz")
        break

