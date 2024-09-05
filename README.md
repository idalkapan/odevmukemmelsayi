# odevmukemmelsayi

def mukemmel_sayi_mi(n):   #verilen sayının mükemmel sayı olup olmadığını kontrol eden bir fonks.tanımlaması
    top = 0
    for i in range(1, n):
        if n % i == 0:
            top += i       #sayının mukemmel sayı olması için kendisinden farklı tam bölenlerinin toplamı kendisine eşit olmalı.
    if top == n:
        return True
    else:
        return False

mukemmel_sayi = []                              #girilen mukemmel sayıları tutacak bir liste oluşturdum.
a = int(input("Lütfen sayı giriniz (çıkmak için '0' giriniz): "))   #kullanıcıdan girilecek sayıyı alır.

while a != 0:                              #0 girene kadar döngü devam eder.
    if mukemmel_sayi_mi(a):               #kullanıcının girdiği sayı mukemmel mi diye kontrol ederiz.
        print(f"{a} mükemmel sayıdır.")   #eger sayı mukemmelse ekrana yazdırılır.
        mukemmel_sayi.append( a)         #mukemmel sayı listesine girilen sayı eklenir.
       
    else:
        print(f"{ a} mükemmel sayı değildir.")   #sayı mukemmel değilse bu ifade yazılır.

    a = int(input(" Başka sayı girmek ister misiniz (çıkmak için '0' gir): ")) #kullanıcı başka sayı girmek isterse girer.
    
if len(mukemmel_sayi) > 0:                           #muk sayılistesinde en az bir sayı varsa bu kısım çalışır.
    ort = sum(mukemmel_sayi) / len(mukemmel_sayi)    #mukemmel syıların ortalaması hesaplanır.
    print(f"Girdiğiniz mükemmel sayıların ortalaması {ort}, toplam {len(mukemmel_sayi)} adet mükemmel sayı girdiniz.")
else:                                                #mukemmel sayı listesinde sayı yoksa bu kısım çalışır.
    print("Mükemmel sayı girilmedi.")
    
