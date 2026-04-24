# C Piscine Shell 00

Ana olarak [subject PDF'i](https://cdn.intra.42.fr/pdf/pdf/197002/en.subject.pdf) üzerinden gideceğiz.
AI ile PDF'i markdown'a çevirdim,[subject.md](./subject.md) ve [subject.tr.md](./subject.tr.md) dosyalarını inceleyebilirsiniz.

Bu projeyi yapabilmek için kernel ve shell mantığını iyice kavraman lazım.
Ayrıca git kullanmamız gerekmesi de seni git öğrenmeye itiyor.

Kernel ve shell ile başlayalım:

Kernel çekirdek anlamına geliyor.
Bu çekirdek yazılım CPU yani işlemci, RAM yani anabellek/hafıza ile uğraşan yazılım.
Yani bilgisayar tarafından ne ne zaman çalıştırılacak ve hafızada nereye konulacak gibi konulara uğraşan yazılım kerneldir.

Kernel tek başına çokta anlamlı bir şey değildir, senin kullanman için vardır. "İşletim sistemi" devletin yapısına benzer yani; vatandaş olmazsa, devlet memuru olmazsa var olmasının anlamı yoktur.
Bu nedenle kernelin yazılımlar/programlar/uygulamalar (hepsi aynı şey sayılır) kullansın diye özellikleri vardır. Mesela bir program dosya sisteminden yani depolama alanından bir dosyayı almak istediğinde işletim sistemine söyler. Buna da Syscall yani sistem çağırması deriz; kerneldeki fonksiyonları kullanmaktır bu durum.

Bu kernel baya çıplak bir arkadaş. Şu devre kartları gibi düşün. Yani günün sonunda işletim sistemi ile bir şey yapmak istiyorsan bildiğin o devrelerdeki pinler ile uğraşır gibi uğraşman lazım.

Shell bunu çözüyor. Shell; işletim sisteminin çevresinde, onu kaplayan bir sistem. Zaten shell kabuk demek (Çekirdeğin kabuğu olur).
Normalde shell olmasa her yapmak istediğin iş için gider elle kod yazar sonra bilgisayarda bunu çalıştırırdın, ama shell genel bir kullanım arayüzü gibi bişey. Bu sayede shell ile dosyalara bakabiliyorsun, bir şeyler yapabiliyorsun.

Çoğu shell benzerdir. Unix-like diye bir konsept var, zamanında Unix diye bir işletim sistemindeki komutlar aynı isimlerle kullanılmaya devam ediyor. Bu standartın adı "POSIX shell" diye geçer. O dosya boyutları bayt bit falan mevzuları vs hepsi POSIXten geliyor. Zorunlu mu? Değil, ama sistemler benzer olursa işler verimli oluyor.

[Chapter 1](./subject.tr.md#i-talimatlar) hakkında:

- Egzersizler kolaydan zora doğru gidiyor.
- Birinde hata yaptığın zaman o egzersiden itibaren geri kalanıların hepsi görmezden geliniyor. Yani evoya gelen de hata bulduğunda evoyu durduruyor (hata bulunduğu gibi bırakmaya gerek yok, ama sonraki egzersizler uygun olsa bile "uygun" işaretleyemiyorsun, yani sistem hata yaptığında kapanıyor).
- Bazı dosya veya klasörlerde düzenleme, okuma veya çalıştırma yetkin olmayabilir. Çalışırken bunu gözden geçirmeyi unutma. Yetkilerinin olduğu bir klasörde çalış. Ben masaüstünü kullanmanı öneririm.
- Egzersizi yaptığında proje klasöründe, alakadar egersiz klasöründe gerekli dosyaları vermen gerek bunu unutma. Bununla birlikte tüm egzersizleri teker teker commitlemeni tavsiye ederim.
- Yaptığın herşey havuzdaki başka kişiler tarafından kontrol edilecek ve sonrasında "Moulinette" adında bir test programı otomatik kontorllerini yapacak.
- Moulinette baya kesin sınırları olan bir sistem. Tamamen otomatik ve hiç bir "aması" yoktur. Evoda elemek gerek o yüzden hataları.
- Bilgisayarınızda `/bin/sh` konumunda bir program var. Tüm shell egzersizleri bu program tarafından çalıştırabilir olmalı. Terminale `/bin/sh DOSYA-ADI` yazarak test edebilirsin. Bunu gerektiren bir egzersiz olan [ex04](./subject.tr.md#viii-alıştırma-04-midls) ile bir örnek: `/bin/sh midLS`
- Egzersiz klaösründe sadece teslim edilmesi istenen dosya(lar) bulunmalı. Kesinlikle başka hiç bir ek dosya olmamalı.
- Konuları araştırmak için Google kullan, AI overview'a bak ama sadece onu okuyup sakın geçme. Komutlarda da komutun başına man (manuel'in kısaltması) yazarak komut açıklamasını alabilirsin.
- Örnekleri dikkatlice incele, bazı gereksinimler açık açık yazmıyor olabilir. Dosya boyutları, tarihleri vb.

[Chapter 2](./subject.tr.md#ii-yapay-zeka-talimatları) hakkında:

AI kullanma. Bana sorarsan vibecoding yani AI ile proje yapma falan koca bir saçmalık. Claude.ai kendi sistemlerini AI ile yapıyor. <https://status.claude.com/> sitesinde de görebilirsin, ayda 40 saate kadar kapalı kalabiliyorlar. Dil modelleri (LLM) sana bir şey öğretemez, iyi kod yazamaz. Bunlara güvenilmez.

Tek seferlik işler için, googleda arayıp bulamayacağın spesifik konularda sorular için gidilebilecek bir sistemdir dil modelleri.

Mantığı ve zekası olmayan bu arkadaşlara kıçını dayayacağına azcık dişini sık, zaten bunlar aşırı karmaşık şeyler değil.

Eğer AI kullanırsan bu işlerde, gerekli nöral bağlantıları kuramazsın. Bu da zaten çalmak ile aynı nedenden kaynaklı; uğraşarak yaparsan beynin o veriyi daha iyi işlemeye başlar, daha sonradan verdiğin kararlarda etki göstermesini sağlar. Bu nöral bağları kuramazsan sıçarsın.

AI kullanma, elle yaz. AI'a açıklar sorunları, sorular. Sakın kod veya sonuç alma AI'dan.

Alırsan senin enayiliğin, işe bile giremezsin, mülakat bile geçemezsin. Bırak büyük hayalleri yani, AI ile bi bok olamazsın. Ha olan varsa, sen oluyorsan; bu sistemin hatası. AI yalanı, balonu patlayınca kıçının üstüne oturursun.
