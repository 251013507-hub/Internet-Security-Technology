# Spor dalları
sporlar = ["Basketbol", "Futbol", "Handball", "Voleybol", "Yüzme"]

# Öğrenci sayıları ve isimleri tutulacak listeler
ogrenci_sayilari = []
ogrenci_isimleri = {spor: [] for spor in sporlar}

# İsim → spor eşleştirmesi için sözlük
isimden_spora = {}

print("Toplam 1060 öğrenci vardır.")
print("Bu öğrencilerin spor dallarına dağılımını giriniz:\n")

# Kullanıcıdan 5 spor dalı için değer alıyoruz
for spor in sporlar:
    while True:
        try:
            sayi = int(input(f"{spor} yapan öğrenci sayısı: "))
            if sayi < 0:
                print("Öğrenci sayısı negatif olamaz. Lütfen pozitif bir sayı girin.")
                continue
            break
        except ValueError:
            print("Geçersiz giriş! Lütfen bir sayı girin.")
    ogrenci_sayilari.append(sayi)

    print(f"{spor} yapan öğrencilerin isimlerini giriniz:")
    for i in range(sayi):
        isim = input(f"  {i+1}. öğrenci adı: ")
        ogrenci_isimleri[spor].append(isim)

        # İsim → Spor ekleme
        isimden_spora[isim] = spor

# Sonuçları yazdır
print("\n--- Spor Dağılım Listesi ---")
for i, (spor, sayi) in enumerate(zip(sporlar, ogrenci_sayilari), start=1):
    print(f"{i}. {spor} = {sayi} öğrenci")
    print("   Öğrenciler:", ", ".join(ogrenci_isimleri[spor]))
    print()

# Toplam kontrol
print(f"Girilen toplam öğrenci sayısı: {sum(ogrenci_sayilari)}")


# -------------------------------------------------
#  📌 Yeni özellik: SPOR ADINA GÖRE ARAMA
# -------------------------------------------------
print("\n--- Spor Adına Göre Öğrenci Arama ---")
while True:
    spor_sorgu = input("Öğrencilerini görmek istediğiniz spor dalı (çıkmak için 'q'): ")

    if spor_sorgu.lower() == "q":
        break

    if spor_sorgu in ogrenci_isimleri:
        print(f"\n{spor_sorgu} yapan öğrenciler ({len(ogrenci_isimleri[spor_sorgu])} kişi):")
        print(", ".join(ogrenci_isimleri[spor_sorgu]), "\n")
    else:
        print("Bu spor dalı bulunamadı.\n")


# -------------------------------------------------
#  Mevcut özellik: Öğrencinin yaptığı sporu bulma
# -------------------------------------------------
print("\n--- Öğrenci Spor Sorgulama ---")
while True:
    sorgu = input("Sporunu öğrenmek istediğiniz öğrencinin adı (çıkmak için 'q'): ")

    if sorgu.lower() == "q":
        break

    if sorgu in isimden_spora:
        print(f"{sorgu} → {isimden_spora[sorgu]}\n")
    else:
        print("Bu isim listede bulunamadı.\n")
