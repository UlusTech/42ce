# C Piscine — Shell 00

(AI ile oluşturuldu, orjinal versiyon: [subject.md](./subject.md))

> Bu belge, 42'deki C Piscine'in Shell modülü 00'a ait konu içeriğini barındırmaktadır.
> **Sürüm:** 5.0

---

## İçindekiler

- [C Piscine — Shell 00](#c-piscine--shell-00)
  - [İçindekiler](#i̇çindekiler)
  - [I. Talimatlar](#i-talimatlar)
  - [II. Yapay Zeka Talimatları](#ii-yapay-zeka-talimatları)
    - [Bağlam](#bağlam)
    - [Ana Mesaj](#ana-mesaj)
    - [Öğrenci Kuralları](#öğrenci-kuralları)
    - [Aşama Çıktıları](#aşama-çıktıları)
    - [Yorumlar ve Örnek](#yorumlar-ve-örnek)
  - [III. Önsöz](#iii-önsöz)
  - [IV. Alıştırma 00: Z](#iv-alıştırma-00-z)
  - [V. Alıştırma 01: testShell00](#v-alıştırma-01-testshell00)
  - [VI. Alıştırma 02: Oh yeah, mooore](#vi-alıştırma-02-oh-yeah-mooore)
  - [VII. Alıştırma 03: SSH me](#vii-alıştırma-03-ssh-me)
  - [VIII. Alıştırma 04: midLS](#viii-alıştırma-04-midls)
  - [IX. Alıştırma 05: GiT commit](#ix-alıştırma-05-git-commit)
    - [Kilometre Taşına Ulaştınız, Devam Edin](#kilometre-taşına-ulaştınız-devam-edin)
  - [X. Alıştırma 06: gitignore](#x-alıştırma-06-gitignore)
  - [XI. Alıştırma 07: diff](#xi-alıştırma-07-diff)
  - [XII. Alıştırma 08: clean](#xii-alıştırma-08-clean)
  - [XIII. Alıştırma 09: Illusions, not tricks, Michael](#xiii-alıştırma-09-illusions-not-tricks-michael)
  - [XIV. Teslim ve Akran Değerlendirmesi](#xiv-teslim-ve-akran-değerlendirmesi)

---

## I. Talimatlar

- Bu alıştırmalar, kolaydan zora doğru sıralanmıştır. Daha kolay bir alıştırma tam olarak çalışmıyorsa, daha zor bir alıştırmayı başarıyla tamamlamış olmanız değerlendirmeye **alınmaz**.
- Dosya ve dizinlerin üzerinde gerekli izinlere sahip olduğunuzdan emin olun.
- Her alıştırma için **teslim prosedürlerine** uymanız zorunludur.
- Alıştırmalarınız sınıf arkadaşlarınız tarafından kontrol edilip notlandırılacaktır.
- Bunun yanı sıra, alıştırmalarınız **Moulinette** adlı bir program tarafından da kontrol edilecek ve notlandırılacaktır.
- **Moulinette**, değerlendirmesinde son derece titiz ve katıdır. Tamamen otomatiktir ve onunla müzakere etmenin hiçbir yolu yoktur. Sürprizlerle karşılaşmamak için olabildiğince dikkatli olun.
- Shell alıştırmaları `/bin/sh` ile çalıştırılabilir olmalıdır.
- Dizininizde, ödevde belirtilenlerin dışında **hiçbir ek dosya bırakmamalısınız**.
- Bir sorunuz mu var? Sağınızdaki arkadaşınıza sorun. O da bilmiyorsa, solunuzdakine deneyin.
- Başvuru kaynağınız **Google / man / İnternet / ...**'dir.
- Örnekleri dikkatlice inceleyin. Ödevde açıkça belirtilmeyen ayrıntılar içerebilirler.

---

## II. Yapay Zeka Talimatları

### Bağlam

C Piscine yoğun bir süreçtir. Bu, 42'deki ilk büyük meydan okumanızdır — problem çözme, özerklik ve topluluk ruhuna derinlemesine bir dalış.

Bu aşamada temel amacınız, mücadele, tekrar ve özellikle **akran öğrenmesi** yoluyla sağlam bir temel oluşturmaktır.

Yapay zeka çağında kısayollar bulmak kolaydır. Ancak yapay zeka kullanımınızın sizi gerçekten geliştirip geliştirmediğini — ya da gerçek becerilerin gelişmesinin önünde bir engel oluşturup oluşturmadığını — sorgulamak önemlidir.

Piscine aynı zamanda insani bir deneyimdir — ve şimdilik hiçbir şey bunu yerine geçemez. Yapay zeka bile.

Yapay zeka hakkındaki tutumumuza — bir öğrenme aracı olarak, BİT müfredatının bir parçası olarak ve iş dünyasında giderek artan bir beklenti olarak — daha kapsamlı bir genel bakış için lütfen intranetteki özel SSS bölümüne başvurun.

### Ana Mesaj

- Kısayol kullanmadan sağlam temeller oluşturun.
- Teknik ve temel becerileri gerçekten geliştirin.
- Gerçek akran öğrenmesini deneyimleyin; öğrenmeyi ve yeni sorunları çözmeyi öğrenin.
- Öğrenme yolculuğu, sonuçtan daha önemlidir.
- Yapay zekayla ilişkili riskleri öğrenin; yaygın tuzaklardan kaçınmak için etkili kontrol pratikleri ve önlemler geliştirin.

### Öğrenci Kuralları

- Özellikle yapay zekaya başvurmadan önce, verilen görevlere kendi muhakemenizi uygulayın.
- Yapay zekadan doğrudan cevap istemeyin.
- 42'nin yapay zekaya yaklaşımını öğrenin.

### Aşama Çıktıları

Bu temel aşamanın sonunda aşağıdaki kazanımları elde etmiş olacaksınız:

- Doğru teknik ve kodlama temelleri.
- Yapay zekanın bu aşamada neden ve nasıl tehlikeli olabileceğinin farkındalığı.

### Yorumlar ve Örnek

- Evet, yapay zekanın var olduğunu biliyoruz — ve evet, projelerinizi çözebilir. Ancak burada öğrenmek için buradasınız; yapay zekanın sorunu çözebildiğini kanıtlamak için değil. Sadece yapay zekanın verilen problemi çözebildiğini göstermek için zamanınızı (ya da bizim zamanımızı) harcamayın.
- 42'de öğrenmek cevabı bilmekle ilgili değildir — cevabı bulma yeteneğini geliştirmekle ilgilidir. Yapay zeka size doğrudan cevabı verir, ancak bu kendi muhakemenizi oluşturmanızı engeller. Muhakeme ise zaman, çaba ve başarısızlık gerektirir. Başarıya giden yolun kolay olması beklenemez.
- Sınavlarda yapay zekanın kullanılamayacağını unutmayın — internet yok, akıllı telefon yok, vs. Öğrenme sürecinizde yapay zekaya çok fazla güvenip güvenmediğinizi hızla anlayacaksınız.
- Akran öğrenmesi, sizi farklı fikir ve yaklaşımlara açar; kişilerarası becerilerinizi ve farklı düşünme yeteneğinizi geliştirir. Bu, bir botla sohbet etmekten çok daha değerlidir. Çekinmeyin — konuşun, soru sorun ve birlikte öğrenin!
- Evet, yapay zeka müfredatın bir parçası olacak — hem bir öğrenme aracı hem de başlı başına bir konu olarak. Hatta kendi yapay zeka yazılımınızı oluşturma fırsatı da bulacaksınız. Kademeli yaklaşımımız hakkında daha fazla bilgi edinmek için intranetteki belgelere göz atın.

**✓ İyi Uygulama:**
> Yeni bir konsept üzerinde takılıp kaldım. Yakınımdaki birine nasıl yaklaştıklarını soruyorum. 10 dakika konuşuyoruz — ve aniden her şey yerine oturuyor. Anladım.

**✗ Kötü Uygulama:**
> Gizlice yapay zeka kullanıyorum, doğru gibi görünen bir kodu kopyalıyorum. Akran değerlendirmesinde hiçbir şeyi açıklayamıyorum. Başarısız oluyorum. Sınavda — yapay zeka yok — yine takılıp kalıyorum. Yine başarısız oluyorum.

---

## III. Önsöz

Aşağıda *City Hunter*'ın tema şarkısı olan *"Moonlight Shadow"*'un sözleri yer almaktadır:

```text
The last time ever she saw him
Carried away by a moonlight shadow
He passed on worried and warning
Carried away by a moonlight shadow.
Lost in a riddle that Saturday night
Far away on the other side.
He was caught in the middle of a desperate fight
And she couldn't find how to push through

The trees that whisper in the evening
Carried away by a moonlight shadow
Sing a song of sorrow and grieving
Carried away by a moonlight shadow
All she saw was a silhouette of a gun
Far away on the other side.
He was shot six times by a man on the run
And she couldn't find how to push through

[Chorus]
I stay, I pray
See you in Heaven far away...
I stay, I pray
See you in Heaven one day.

Four A.M. in the morning
Carried away by a moonlight shadow
I watched your vision forming
Carried away by a moonlight shadow
A star was glowing in the silvery night
Far away on the other side
Will you come to talk to me this night
But she couldn't find how to push through

[Chorus]
Far away on the other side.
Caught in the middle of a hundred and five
The night was heavy and the air was alive
But she couldn't find how to push through
Carried away by a moonlight shadow
Carried away by a moonlight shadow
Far away on the other side.
```

*Ne yazık ki bu konunun City Hunter ile hiçbir ilgisi yoktur.*

---

## IV. Alıştırma 00: Z

| | Alıştırma 00 |
| --- | --- |
| **Alt Başlık** | Yalnızca en iyiler Z'yi nasıl görüntüleyeceğini bilir |
| **Teslim dizini** | `ex00/` |
| **Teslim edilecek dosyalar** | `z` |
| **İzin verilen fonksiyonlar** | Yok |

`cat` komutu kullanıldığında `"Z"` ve ardından bir satır sonu döndüren `z` adında bir dosya oluşturun.

```sh
?>cat z
Z
?>
```

> 💡 Google senin dostun.

---

## V. Alıştırma 01: testShell00

| | Alıştırma 01 |
| --- | --- |
| **Alt Başlık** | Nitelikler nedir ki zaten? |
| **Teslim dizini** | `ex01/` |
| **Teslim edilecek dosyalar** | `testShell00.tar` |
| **İzin verilen fonksiyonlar** | Yok |

- Teslim dizininizde `testShell00` adında bir dosya oluşturun.
- Çıktının aşağıdaki gibi görünmesini sağlayın (`"total 1"` satırı hariç):

```sh
%> ls -l
total 1
-r--r-xr-x 1 XX XX 40 Jun 1 23:42 testShell00
%>
```

- Önceki adımları tamamladıktan sonra, teslim edilecek dosyayı oluşturmak için şu komutu çalıştırın:

```sh
%> tar -cf testShell00.tar testShell00
```

> ⚠️ `"XX"` yerine ne görüntülendiğini umursamayın.  
> ⚠️ Dosyanın zaman damgasındaki saat yerine yıl da kabul edilecektir.
> 💡 Sağınızdaki arkadaşınızla kontrol ettiniz mi?

---

## VI. Alıştırma 02: Oh yeah, mooore

| | Alıştırma 02 |
| --- | --- |
| **Alt Başlık** | Oh yeah, mooore... |
| **Teslim dizini** | `ex02/` |
| **Teslim edilecek dosyalar** | `exo2.tar` |
| **İzin verilen fonksiyonlar** | Yok |

Aşağıdaki dosya ve dizinleri oluşturun. `ls -l` komutunu çalıştırdığınızda çıktının şöyle görünmesi için özelliklerini ayarlayın:

```sh
%> ls -l
total XX
drwx--xr-x 2 XX XX XX Jun 1 20:47 test0
-rwx--xr-- 1 XX XX  4 Jun 1 21:46 test1
dr-x---r-- 2 XX XX XX Jun 1 22:45 test2
-r-----r-- 2 XX XX  1 Jun 1 23:44 test3
-rw-r----x 1 XX XX  2 Jun 1 23:43 test4
-r-----r-- 2 XX XX  1 Jun 1 23:44 test5
lrwxrwxrwx 1 XX XX  5 Jun 1 22:20 test6 -> test0
%>
```

Tamamladıktan sonra, teslim edilecek dosyayı oluşturmak için şu komutu çalıştırın:

```sh
%> tar -cf exo2.tar *
```

> ⚠️ `"XX"` yerine ne görüntülendiğini umursamayın.  
> ⚠️ Dosyanın zaman damgasındaki saat yerine yıl da kabul edilecektir.
> 💡 Kümenizdeki herkesten yardım istemekten çekinmeyin!

---

## VII. Alıştırma 03: SSH me

| | Alıştırma 03 |
| --- | --- |
| **Alt Başlık** | SSH Anahtarı |
| **Teslim dizini** | `ex03/` |
| **Teslim edilecek dosyalar** | `id_rsa_pub` |
| **İzin verilen fonksiyonlar** | Yok |

- Kendi SSH anahtarınızı oluşturun. Tamamlandıktan sonra:
  - Açık anahtarınızı `id_rsa_pub` adlı bir dosyada deponuza ekleyin.
  - İntranet üzerindeki SSH anahtarınızı güncelleyin. Bu, depoyu git sunucumuza push etmenizi sağlayacaktır.

> ⚠️ Dosya adı rastgele seçilmedi.  
> ⚠️ Açık anahtar ile özel anahtar arasındaki farkı anladığınızdan emin olun.
> 💡 Solunuzdaki arkadaşınızla kontrol ettiniz mi?

---

## VIII. Alıştırma 04: midLS

| | Alıştırma 04 |
| --- | --- |
| **Alt Başlık** | midLS |
| **Teslim dizini** | `ex04/` |
| **Teslim edilecek dosyalar** | `midLS` |
| **İzin verilen fonksiyonlar** | Yok |

- `midLS` adlı bir dosyaya, bulunduğunuz dizindeki tüm dosya ve dizinleri listeleyen komutu yazın (nokta ile başlayan gizli dosyalar ve çift nokta dahil, nokta ile başlayan her şey hariç).
- Çıktı, değiştirilme tarihine göre sıralanmalı ve girişler virgül ile boşlukla ayrılmalıdır.
- Dizin adları eğik çizgi (`/`) ile bitmelidir.

> ⚠️ Yalnızca isteneni yapın, fazlasını değil!
> 💡 RTFM! (Kılavuzu oku!)  
> 💡 Düzenli olarak git push yapın.

---

## IX. Alıştırma 05: GiT commit

| | Alıştırma 05 |
| --- | --- |
| **Alt Başlık** | GiT commit? |
| **Teslim dizini** | `ex05/` |
| **Teslim edilecek dosyalar** | `git_commit.sh` |
| **İzin verilen fonksiyonlar** | Yok |

Git deponuzdaki son 5 commit'in id'lerini görüntüleyen bir shell betiği oluşturun.

```sh
%> bash git_commit.sh | cat -e
baa23b54f0adb7bf42623d6d0a6ed4587e11412a$
2f52d74b1387fa80eea844969e8dc5483b531ac1$
905f53d98656771334f53f59bb984fc29774701f$
5ddc8474f4f15b3fcb72d08fcb333e19c3a27078$
e94d0b448c03ec633f16d84d63beaef9ae7e7be8$
%>
```

- Betiğiniz kendi ortamımızda test edilecektir.

> 💡 RTFM! (Kılavuzu oku!)  
> 💡 İlk yeniden deneme süresi kısadır; ilerlemenizi takip etmek için ara değerlendirmeyi tetikleyin!

---

### Kilometre Taşına Ulaştınız, Devam Edin

Bu projenin zorunlu alıştırmalarını tamamladınız. Artık bir seçiminiz var:

- Daha fazlasını keşfetmek için **isteğe bağlı alıştırmalar** ile devam edin.
- **Bir sonraki projeye** geçin.

Her iki yol da size yararlı kavramlar kazandıracaktır. Karar vermeden önce şunları göz önünde bulundurun:

- İlk sınavınız ve hafta sonu rush'ı C programlamaya odaklanacaktır. Bu nedenle önceden bu alanda deneyim kazanmak faydalı olabilir.
- Piscine'deki performansınız birden fazla faktöre göre değerlendirilir:
  - Proje tamamlama bunlardan biridir.
  - Piscine projelerinin tamamındaki genel ilerlemeniz ise bir diğeridir. Sonuçlarınızı en üst düzeye çıkarmak için akıllıca seçin.
- Piscine'in sonuna kadar aynı projeyi birkaç gün veya hafta içinde yeniden deneyebilirsiniz.
- Akranlarınızla aynı tempoyu korumak, daha iyi bir işbirliğini destekler.

---

## X. Alıştırma 06: gitignore

| | Alıştırma 06 |
| --- | --- |
| **Alt Başlık** | GiT |
| **Teslim dizini** | `ex06/` |
| **Teslim edilecek dosyalar** | `git_ignore.sh` |
| **İzin verilen fonksiyonlar** | Yok |

Git deponuz tarafından yok sayılan mevcut dosyaları listeleyen kısa bir shell betiği yazın.

Örnek çıktı:

```sh
%> bash git_ignore.sh | cat -e
.DS_Store$
mywork.c~$
%>
```

- Betiğiniz kendi ortamımızda test edilecektir.

> 💡 RTFM! (Kılavuzu oku!)  
> 💡 Başkalarından ilham alın, ama işinizi onlara yaptırmayın!

---

## XI. Alıştırma 07: diff

| | Alıştırma 07 |
| --- | --- |
| **Teslim dizini** | `ex07/` |
| **Teslim edilecek dosyalar** | `b` |
| **İzin verilen fonksiyonlar** | Yok |

Aşağıdaki koşulları sağlayacak şekilde `b` adında bir dosya oluşturun:

```sh
%>cat -e a
STARWARS$
Episode IV, A NEW HOPE It is a period of civil war.$
$
Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire.$
During the battle, Rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR,$
an armored space station with enough power to destroy an entire planet.$
$
Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy...$
$
%>diff a b > sw.diff
```

> 💡 `man patch`  
> 💡 Hiçbir kaynağa körce güvenmeyin; sonuçlarınızı her zaman kendiniz test edin, doğrulayın ve geçerli kılın!

---

## XII. Alıştırma 08: clean

| | Alıştırma 08 |
| --- | --- |
| **Teslim dizini** | `ex08/` |
| **Teslim edilecek dosyalar** | `clean` |
| **İzin verilen fonksiyonlar** | Yok |

`clean` adlı bir dosyaya, aşağıdakileri gerçekleştiren tek bir komut yazın:

- Bulunduğunuz dizin ve alt dizinlerinde `~` (tilde) ile biten ya da `#` (diyez) ile başlayıp biten tüm dosyaları arar.
- Bulunan dosyaları görüntüler ve siler.

Yalnızca tek bir komuta izin verilir; `';'`, `'&&'` veya başka zincirleme yöntemleri yasaktır.

> 💡 `man find`  
> 💡 İşbirliği başarının anahtarıdır!

---

## XIII. Alıştırma 09: Illusions, not tricks, Michael

| | Alıştırma 09 |
| --- | --- |
| **Alt Başlık** | Illusions, not tricks, Michael... |
| **Teslim dizini** | `ex09/` |
| **Teslim edilecek dosyalar** | `ft_magic` |
| **İzin verilen fonksiyonlar** | Yok |

`file` komutunun `42 file` türündeki dosyaları — 42. baytta `"42"` dizesini içeren dosyalar olarak tanımlanmış — algılamasını sağlayacak şekilde düzgün biçimlendirilmiş, `ft_magic` adında bir **magic dosyası** oluşturun.

> 💡 `man file`  
> 💡 Başarısızlık, öğrenme yolculuğunuzun bir parçasıdır.

---

## XIV. Teslim ve Akran Değerlendirmesi

Ödevinizi her zamanki gibi Git deponuza gönderin. Savunma sırasında yalnızca deponuzdaki çalışmalar değerlendirilecektir. Dosya adlarının doğru olduğundan emin olmak için iki kez kontrol edin.

> ⚠️ Yalnızca proje talimatlarında açıkça belirtilen dosyaları teslim etmelisiniz.
