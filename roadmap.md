# SDR Mastery Program v1.0
## RF temellerinden ölçülebilir SDR sistemleri ve teknik yayınlara

**Katılımcı:** Haktan Ayrıbaş  
**Hazırlanma tarihi:** 3 Ekim 2026  
**Başlangıç oturumu:** 3–4 Ekim 2026  
**52 haftalık çalışma dönemi:** 5 Ekim 2026 – 3 Ekim 2027  
**Çalışma bütçesi:** haftada yaklaşık 8 saat; yılda yaklaşık 416 saat  
**Durum:** Plan hazır; başlangıç değerlendirmesi ve laboratuvarlar henüz yapılmadı.

## 1. Amaç ve gerçekçi başarı tanımı

Amaç, bir RF/SDR problemini sinyal, donanım, DSP, yazılım ve ölçüm katmanlarında inceleyebilmek; tasarım kararlarını hesap ve deneyle savunabilmek; çalışmalarını başkalarının tekrarlayabileceği biçimde yayımlamaktır.

Bir yıllık program, her teknik soruya cevap verebilme veya ülke çapında bilirkişi sayılma garantisi değildir. İlk yılın somut hedefi güçlü mühendislik temeli ve denetlenebilir portföydür. Tanınan uzmanlık; sonraki yıllarda belirli bir alanda derinleşme, saha deneyimi, bağımsız doğrulama, açık kaynak katkıları ve teknik yayınlarla gelişir. Resmî bilirkişilik ise bu programdan ayrı bir yeterlilik ve başvuru konusudur.

İlk yılın sonunda beklenen yetkinlikler:

- RF güç, kayıp, kazanç, gürültü ve basit link budget hesaplarını açıklamak.
- IQ, örnekleme, aliasing, filtreleme ve spektral kestirimi kodla ve grafikle göstermek.
- BPSK/QPSK alıcı zincirini kurmak; zamanlama ve taşıyıcı hatalarını teşhis etmek.
- SDR RF zincirini okumak ve cihaz sınırlarını ölçüm sonuçlarından ayırmak.
- GNU Radio, Python ve temel C++ bloklarıyla tekrarlanabilir deneyler yapmak.
- Kendi veya paylaşımı uygun IQ kayıtlarını analiz etmek; çıkarımın belirsizliğini belirtmek.
- LoRa PHY ve bir uydu alım çalışmasını teknik rapora dönüştürmek.
- Fixed-point ve temel FPGA DSP zincirini simülasyonla göstermek.
- Bir konuda 20 dakikalık teknik konuşma yapmak ve bilmediği soruda doğrulama yöntemi önermek.

## 2. Başlangıç varsayımları

Embedded/C++, Linux ve mekatronik geçmişin avantajdır. Matematik, Python DSP, RF ölçüm ve GNU Radio seviyen kısa bir başlangıç değerlendirmesiyle belirlenecek. Önceki konuşmalarda adı geçen cihazlar ve çalışmaların mevcut durumu teyit edilmeden tamamlanmış kabul edilmeyecek.

| Kaynak | Plandaki yaklaşım |
|---|---|
| WM1302/Raspberry Pi gateway ve LoRa uç düğümleri | Mevcut proje bağlamı; çalışan durum ve erişim başlangıçta kaydedilecek |
| PlutoSDR | Kullanım/edinme durumu doğrulanacak; ilk haftalar için satın alma ön koşulu yok |
| GNU Radio | Kurulum ve deney seviyesi doğrulanacak; takvim gerekli temel çalışmaları içeriyor |
| Önceki IQ kayıtları | Erişim ve metaveri varsa kullanılacak; yoksa sentetik kayıt üretilecek |
| QO-100 alım zinciri | Anten/LNB/besleme ve erişim uygun olduğunda gerçek ölçüm; aksi hâlde açık kayıt veya simülasyon |
| FPGA/çok kanallı SDR | İlk yıl simülasyon yeterli; pahalı yeni cihaz satın alımı planın şartı değil |

İlk ay için bilgisayar ve Python yeterlidir. RF donanımı, ölçüm ihtiyacı ortaya çıktığında kullanılacak. Windows, macOS veya Linux seçimi mevcut bilgisayara göre yapılabilir; çalışan ortamın sürümleri deney kayıtlarında sabitlenecek.

## 3. Haftalık çalışma düzeni

| Oturum | Süre | Çıktı |
|---|---:|---|
| Pazartesi: teori ve okuma | 60 dk | Bir sayfalık kavram notu |
| Salı: matematik ve elde hesap | 60 dk | Çözümlü 3–5 soru |
| Çarşamba: Python deneyi | 90 dk | Tekrarlanabilir script/notebook ve grafik |
| Perşembe: hafif tekrar | 30 dk | Yanlışlar ve açık sorular listesi |
| Cuma: GNU Radio veya RF laboratuvarı | 90 dk | Flowgraph/kayıt ve deney günlüğü |
| Cumartesi: proje ve dokümantasyon | 120 dk | Haftalık teknik rapor |
| Pazar: sözlü değerlendirme ve takip | 30 dk | Puanlama ve gelecek haftanın kararı |
| **Toplam** | **8 saat** | |

Günler yer değiştirebilir. Yoğun haftada 3 saatlik asgari program: 45 dk teori, 75 dk tek deney, 45 dk rapor, 15 dk değerlendirme. Eksik hafta telafi kuyruğuna alınır; sırf takvime uymak için temel konular atlanmaz. Her dördüncü hafta yeni içerik yükü azaltılarak proje ve tekrar yapılır.

Takip, haftalık rapor üzerinden yürür. Bu belge kendi başına e-posta, hatırlatıcı veya otomatik haftalık ders gönderimi kurmaz.

## 4. On iki aylık çerçeve

| Blok | Hafta | Tarih | Odak | Ana teslim |
|---|---:|---|---|---|
| 1 | 1–4 | 5 Eki – 1 Kas 2026 | RF dili, güç, link budget, mimari | P1: RF hesap ve sinyal zinciri dosyası |
| 2 | 5–8 | 2–29 Kas 2026 | Kompleks sinyal, IQ, örnekleme | P2: IQ ve aliasing deney atlası |
| 3 | 9–13 | 30 Kas 2026 – 3 Oca 2027 | FFT, PSD, gürültü, filtre, multirate | P3: Spektrum analiz aracı |
| 4 | 14–17 | 4–31 Oca 2027 | AM/FM/SSB, dijital modülasyon | P4: Modülasyon karşılaştırma laboratuvarı |
| 5 | 18–21 | 1–28 Şub 2027 | Eşleşmiş filtre, senkronizasyon, BER | P5: QPSK modem simülasyonu |
| 6 | 22–26 | 1 Mar – 4 Nis 2027 | GNU Radio, mesaj/tag, Python/C++ blok | P6: Tekrarlanabilir GNU Radio modülü |
| 7 | 27–30 | 5 Nis – 2 May 2027 | Pluto ve alıcı karakterizasyonu | P7: SDR karakterizasyon raporu |
| 8 | 31–34 | 3–30 May 2027 | LoRa CSS ve gateway ilişkisi | P8: LoRa PHY analiz dosyası |
| 9 | 35–39 | 31 May – 4 Tem 2027 | Bilinmeyen sinyal, protokol, uydu | P9: IQ vaka incelemesi; P10: Uydu alım çalışması |
| 10 | 40–43 | 5 Tem – 1 Ağu 2027 | Fixed-point ve FPGA DSP | P11: DDC simülasyonu |
| 11 | 44–47 | 2–29 Ağu 2027 | Koherens, beamforming, radar, RFML | Dört ileri konu deneyi ve uzmanlık seçimi |
| 12 | 48–52 | 30 Ağu – 3 Eki 2027 | Bitirme projesi, tekrar, yayın | P12: Kapsamlı rapor, repo ve sunum |

Haftalık takvim aşağıda verilmiştir. Bloklar takvim aylarıyla tam örtüşmez.

## 5. Elli iki haftalık program

Her satırdaki çıktı, bir deney raporu veya açıkça adlandırılmış tekrar teslimidir. Donanım olmayan haftalarda sentetik IQ kullanılabilir; simülasyon sonuçları gerçek ölçüm gibi sunulmaz.

| Hf. | Başlangıç | Konu | Laboratuvar / teslim | Geçiş sorusu |
|---:|---|---|---|---|
| 1 | 5 Eki 2026 | Frekans, dalga boyu, faz, dB/dBm | Güç dönüşümleri ve link budget; iki sinüs grafiği | 3 dB güç ve genlikte ne değiştirir? |
| 2 | 12 Eki | Empedans, yansıma, anten, polarizasyon | 50 Ω senaryoları; kablo kaybı ve anten yönü analizi | dBi neden alıcı güç birimi değildir? |
| 3 | 19 Eki | Yayılım, FSPL, Fresnel, multipath | Mesafe/frekans taraması; varsayımlı LoRa link budget | FSPL modeli nerede yetersiz kalır? |
| 4 | 26 Eki | Mixer, LNA, filtre, Zero/Low-IF | P1: SDR RX/TX blok diyagramı ve RF tekrar sınavı | RF merkez frekansı ve örnekleme hızı nasıl ayrılır? |
| 5 | 2 Kas | Kompleks sayılar, Euler, fazör | Dönen fazör ve gerçek/kompleks sinüs | Negatif frekans temsil olarak ne anlatır? |
| 6 | 9 Kas | IQ ve kompleks baseband | +f/−f tonlar; frekans kaydırma | Tek gerçek kanalın IQ'ya göre kaybı nedir? |
| 7 | 16 Kas | Örnekleme, aliasing, bant geçiren örnekleme | Nyquist sınırı ve aliasing taraması | 120 MHz ton, 100 MS/s gerçek örneklemede nereye katlanır? |
| 8 | 23 Kas | Kuantalama, ENOB, clipping | P2: Bit sayısı ve clipping karşılaştırması | ADC bit sayısı neden tek başına alıcı performansı değildir? |
| 9 | 30 Kas | DFT/FFT, pencere, leakage | Aynı kaydın farklı N ve pencerelerle analizi | Bin aralığı ile etkin çözünürlük neden aynı değildir? |
| 10 | 7 Ara | PSD, ENBW, güç normalizasyonu | White-noise PSD ve pencere karşılaştırması | FFT grafiğindeki birimin dBFS mi dBm mi olduğunu nasıl anlarsın? |
| 11 | 14 Ara | SNR, termal gürültü, NF | Bant genişliği/NF taraması; Friis kaskat hesabı | Gürültü hesabında hangi sıcaklık ve bant varsayılır? |
| 12 | 21 Ara | FIR/IIR, frekans/faz cevabı | Aynı gereksinimle iki filtre; geçici rejim | Grup gecikmesi demodülasyonu nasıl etkiler? |
| 13 | 28 Ara | Decimation/interpolation/polyphase | P3: Filtreli resampling ve spektrum analiz aracı | Örnek atlamadan önce neden filtre gerekir? |
| 14 | 4 Oca 2027 | AM, FM, SSB | Sentetik verici/alıcı; bant genişliği karşılaştırması | FM demodülasyonu faz değişiminden nasıl çıkar? |
| 15 | 11 Oca | OOK, FSK, GMSK | Gürültü altında üç modülasyonun zaman/frekans grafiği | Görüntüden modülasyonu kesin belirleyebilir misin? |
| 16 | 18 Oca | BPSK/QPSK/QAM, sembol/bit hızı | Mapper/demapper ve constellation | QPSK'da bit hızı ile baud ilişkisi nedir? |
| 17 | 25 Oca | OFDM, CP, PAPR | P4: Basit OFDM simülasyonu ve modülasyon atlası | CP hangi koşulda ISI'yi azaltır? |
| 18 | 1 Şub | Pulse shaping, RRC, matched filter | Eye diagram; farklı roll-off/SPS | RRC verici ve alıcı birlikte ne üretir? |
| 19 | 8 Şub | Timing recovery | Zamanlama hatası ekle; kurtarma zinciri | Constellation iyi görünürken BER neden kötü olabilir? |
| 20 | 15 Şub | CFO, Costas/PLL, phase ambiguity | Frekans/faz hatası ve taşıyıcı kurtarma | Bir PLL'nin kilitlendiğini nasıl sınarsın? |
| 21 | 22 Şub | BER, Eb/N0, frame sync | P5: QPSK BER eğrisi ve paket senkronizasyonu | SNR'den Eb/N0'a geçişte hangi hız/bant tanımı var? |
| 22 | 1 Mar | GRC, stream/vector, scheduler | Çalışan temel zincir; throughput ölçümü | Throttle hangi zincirde kullanılır? |
| 23 | 8 Mar | Stream tags, messages, PDU | Paket uzunluğu tag'i ve PDU dönüşümü | Paket sınırı stream'de nasıl taşınır? |
| 24 | 15 Mar | Python custom block | Ölçüm veya paket algılama bloğu | work fonksiyonunda tüketim/üretim ilişkisi nedir? |
| 25 | 22 Mar | C++ OOT module | Küçük DSP/ölçüm bloğu ve anlamlı test | Blok türü seçiminde rate ilişkisi neden önemli? |
| 26 | 29 Mar | Buffer, performans, tekrar üretme | P6: Python/C++ karşılaştırması ve kurulum belgesi | Kayıp sample ile RF hatasını nasıl ayırırsın? |
| 27 | 5 Nis | Pluto RFIC/Zynq/libiio zinciri | Donanım envanteri, RX script, metaverili kayıt | RFIC filtresi, FPGA ve host filtresi nerede? |
| 28 | 12 Nis | Gain, AGC, clipping, DC/IQ hatası | Sabit gain/AGC ve DC yakınındaki sinyal analizi | AGC ölçüm karşılaştırmasını neden zorlaştırır? |
| 29 | 19 Nis | Clock/CFO, image, nonlinearities | Tek/iki ton karakterizasyonu veya kontrollü simülasyon | Görülen spur'un kaynağını nasıl ayırırsın? |
| 30 | 26 Nis | Kalibrasyon, belirsizlik, ölçüm sınırı | P7: Tekrarlı ölçüm, hata bütçesi ve rapor | Referanssız SDR'den mutlak dBm iddiası çıkar mı? |
| 31 | 3 May | LoRa CSS, SF, BW, sembol süresi | Chirp üretimi ve dechirp/FFT | SF artınca sembol süresi neden artar? |
| 32 | 10 May | LoRa senkronizasyon, CFO, timing | Sentetik preamble ve hata taraması | FFT tepesinin kayması neyi gösterir? |
| 33 | 17 May | LoRa PHY / LoRaWAN ayrımı | Kendi node kaydı veya sentetik IQ; gateway log ilişkisi | PHY gözlemi hangi MAC bilgilerini vermez? |
| 34 | 24 May | LoRa ölçüm ve deney tasarımı | P8: Kontrollü SF/BW/SNR deney matrisi | SF karşılaştırmasında hangi değişkenleri sabitlersin? |
| 35 | 31 May | Bilinmeyen sinyal metodolojisi | Spektrum, spectrogram, otokorelasyon, hipotez tablosu | Bir yorumun kanıt ve varsayımını nasıl ayırırsın? |
| 36 | 7 Haz | Symbol-rate kestirimi, cyclostationarity | Sentetik sinyallerde kestirim ve hata analizi | Periyodik tepe gerçekten sembol hızı mı? |
| 37 | 14 Haz | Framing/protokol çözümleme | P9: Kendi/açık kayıtta paket sınırı ve bit analizi | Preamble, payload ve checksum nasıl sınanır? |
| 38 | 21 Haz | Uydu RF zinciri, Doppler, LNB | QO-100 alım planı veya açık LEO kaydı | RF, LNB IF ve baseband frekansı nasıl izlenir? |
| 39 | 28 Haz | Uydu alımı ve frekans kararlılığı | P10: Alım/kayıt veya Doppler simülasyon raporu | Drift'i Doppler'den ayırmak için hangi referans gerekir? |
| 40 | 5 Tem | Fixed-point, ölçek, overflow | Float/fixed-point karşılaştırması | Bit genişliği seçimini hangi hata bütçesi belirler? |
| 41 | 12 Tem | NCO, CORDIC, DDC/DUC | DDC modellemesi ve frekans doğrulaması | NCO tuning word nasıl frekansa dönüşür? |
| 42 | 19 Tem | CIC/FIR, word growth, latency | CIC droop ve compensation filtresi | CIC neden çarpansız çalışabilir? |
| 43 | 26 Tem | FPGA akışı, DMA ve doğrulama | P11: DDC doğrulaması; isteğe bağlı RTL simülasyonu | Host aktarım kapasitesi DSP kararını nasıl etkiler? |
| 44 | 2 Ağu | Çok SDR: zaman/frekans/faz | Koherens simülasyonu; referans bağlantı taslağı | PPS ve 10 MHz tek başına faz koherensi sağlar mı? |
| 45 | 9 Ağu | Beamforming, DoA, MUSIC | Sentetik dizi ve açısal hata taraması | Kalibrasyon/multipath yön kestirimini nasıl bozar? |
| 46 | 16 Ağu | FMCW, Doppler, passive radar | Simülasyonda range-Doppler haritası | Menzil çözünürlüğünü hangi bant belirler? |
| 47 | 23 Ağu | RFML, cognitive radio, SDR vizyonu | Küçük modulation-classification deneyi; araştırma haritası | Train/test sızıntısı RFML sonucunu nasıl şişirir? |
| 48 | 30 Ağu | Bitirme projesi: kapsam ve kaynak | Problem, baseline, deney matrisi ve başarı ölçütü | Proje hangi tek soruya cevap veriyor? |
| 49 | 6 Eyl | Bitirme projesi: uygulama | Çalışan baseline ve ilk sonuçlar | Baseline tekrarlanabiliyor mu? |
| 50 | 13 Eyl | Bitirme projesi: doğrulama | Tekrarlar, hata senaryoları, belirsizlik | Sonuç hangi koşullarda geçersizleşir? |
| 51 | 20 Eyl | Bitirme projesi: teknik yayın | P12: Teknik rapor, repo ve 20 dk sunum | Başka biri ölçümü yeniden üretebilir mi? |
| 52 | 27 Eyl | Final değerlendirmesi | Sözlü sınav, bağımsız vaka, ikinci yıl kararı | Bilmediğin bir arızada ilk üç ölçümün ne olur? |

## 6. İlerleme kriterleri

Her haftaya 100 üzerinden puan verilir. Bu kişisel takip ölçeğidir; dışarıdan verilmiş sertifika veya mesleki unvan değildir.

| Alan | Puan | Beklenen kanıt |
|---|---:|---|
| Kavramsal açıklama | 20 | Konuyu not okumadan 3–5 dk anlatma |
| Hesap / model | 20 | Birim, varsayım ve ara adımları doğru hesap |
| Deney / doğrulama | 30 | Tekrarlanabilir çalışma; beklenen ve gözlenen sonuç |
| Dokümantasyon | 20 | Kod, parametre, grafik, kaynak, sınırlılıklar |
| Teknik soru-cevap | 10 | En az 5 sorunun 4'ünü gerekçeyle yanıtlama |

**Geçiş koşulu:** en az 75/100; hesap ve deney alanlarının her birinde en az %60; açık kritik kavram hatası olmaması. Eksik kavramlar 30–60 dakikalık telafi ve kısa yeniden değerlendirmeyle kapatılır.

Dört büyük kapı:

1. **Hafta 13:** IQ, aliasing, FFT/PSD ve filtreleme. Bir sentetik sinyali oluşturup ölçekleri doğru açıklayabilmek.
2. **Hafta 26:** QPSK ve GNU Radio. Hata eklenmiş zinciri teşhis etmek; kodu temiz ortamda çalıştırmak.
3. **Hafta 39:** SDR ölçümü, LoRa, uydu ve kayıt analizi. Ölçümle tahmini ayıran iki vaka raporu sunmak.
4. **Hafta 52:** Sistem tasarımı ve yayın. Bitirme projesini savunmak; bilinmeyen soruda test planı kurmak.

## 7. Proje portföyü ve yayın yükü

Asgari hedef: **24 kısa deney raporu, 6 kapsamlı proje, 6 teknik yazı ve 1 bitirme sunumu.** Genişletilmiş hedef: **36 deney raporu, 12 proje, 12 teknik yazı.** Haftalık notların hepsinin uzun blog yazısına çevrilmesi gerekmiyor. Kalite ve tekrar üretme, sayıdan önce gelir.

| Proje | Asgari / genişletilmiş | Ölçülebilir çıktı |
|---|---|---|
| P1 RF hesapları | Asgari | Birimli hesaplar ve RX/TX zinciri |
| P2 IQ/aliasing atlası | Genişletilmiş; P3'e katılabilir | +f/−f ve aliasing örnekleri |
| P3 Spektrum analiz aracı | Asgari | Pencere/FFT/PSD doğrulaması |
| P4 Modülasyon atlası | Genişletilmiş; P5'e katılabilir | AM/FM/FSK/PSK/OFDM görselleri |
| P5 QPSK modem | Asgari | BER eğrisi; CFO/timing kurtarma |
| P6 GNU Radio modülü | Genişletilmiş; P5'i güçlendirebilir | Python/C++ blok ve kurulum |
| P7 SDR karakterizasyonu | Asgari | Kazanç, clipping, CFO, ölçüm sınırları |
| P8 LoRa PHY analizi | Asgari | Chirp/dechirp ve kontrollü karşılaştırma |
| P9 IQ vaka incelemesi | Genişletilmiş | Kanıt/hipotez tablosu ve paket analizi |
| P10 Uydu alım çalışması | Genişletilmiş | Zincir, kayıt, frekans kararlılığı |
| P11 DDC simülasyonu | Genişletilmiş | Float/fixed-point hata ve kaynak hesabı |
| P12 Bitirme projesi | Asgari | Baseline, tekrarlar, rapor ve sunum |

İlk yılın bitirme projesi için varsayılan öneri: **“LoRa sinyallerinde CFO, SNR ve zamanlama etkilerinin SDR ile incelenmesi.”** Bu, gateway/LoRa bağlamını DSP ve RF ölçümüyle birleştirir. Donanım durumu veya ilgine göre QO-100 alım kararlılığı ya da tekrarlanabilir spectrum-monitoring zinciri seçilebilir. Başarı ölçütleri 48. haftada deney düzenine göre sayısallaştırılacak.

## 8. Dokümantasyon ve yayın sistemi

Ana teknik kaynak GitHub reposu olarak planlanır: `SDR-Mastery-Program`. Bu belge repo açmaz veya internette yayın yapmaz. GitHub'da yayımlanacak içerik, gerçek deney sonuçları tamamlandıktan sonra paylaşılır.

Önerilen dizinler:

- `README.md`: amaç, başlangıç, ilerleme ve deney dizini.
- `roadmap.md`: bu ana plan.
- `progress/weekly-log.md`: haftalık takip.
- `weeks/week-01/` … `weeks/week-52/`: kısa çalışma notları.
- `labs/`: numaralı deney raporları ve görseller.
- `projects/`: kapsamlı proje kodu, raporu ve çalıştırma yönergeleri.
- `flowgraphs/`: GNU Radio `.grc` dosyaları.
- `python/`: script/notebook ve bağımlılıklar.
- `data/`: küçük paylaşılabilir örnekler ve metaveri; büyük IQ dosyaları için ayrı erişim yöntemi.
- `publications/`: blog taslakları ve sunumlar.
- `references/`: kaynak listesi ve kısa okuma notları; telifli kitap/PDF kopyaları değil.

**Dil tercihi varsayımı:** öğrenme notları Türkçe; kod, değişkenler ve repo özeti İngilizce; ana yazılar önce Türkçe, gerekirse İngilizce uyarlama. Aynı anda her şeyi iki dilde yazmak çalışma yükünü artırır.

Yayın döngüsü: deney → teknik rapor → tekrarlama → teknik doğruluk incelemesi → GitHub → seçilmiş blog yazısı → kısa LinkedIn özeti. Ayda bir güçlü yazı genişletilmiş hedeftir; iki ayda bir yazı asgari hedeftir.

İlk altı yazı önerisi:

1. SDR'de dB ve dBm: aynı sayı neden farklı anlam taşır?
2. IQ ve negatif frekans: kompleks baseband'i deneyle anlamak.
3. FFT bin aralığı, pencere ve RBW: spektrumu doğru okumak.
4. QPSK alıcısında carrier ve timing recovery.
5. PlutoSDR ile neyi ölçebilirim, hangi sonuca referans gerekir?
6. LoRa chirp'inden dechirp/FFT analizine.

Yayın öncesi kontrol: çalıştırma adımları eksiksiz mi; grafik eksen/birimleri açık mı; iddia veriyle destekli mi; simülasyon ve ölçüm ayrılmış mı; kaynaklar doğru mu; cihaz/ortam sürümleri kayıtlı mı; paylaşılacak veri uygun mu; hata ve sınırlılıklar yazılı mı?

## 9. Deney raporu şablonu

Her deneyde aşağıdaki başlıklar kullanılır. Henüz alınmamış ölçümlere “yapılmadı” yazılır; beklenen sonuç, ölçüm alanına geçirilmez.

1. Başlık, deney ID, tarih, yazar, durum.
2. Amaç: cevaplanacak tek soru.
3. Hipotez ve başarı ölçütü.
4. Teori: ilgili denklem, birim ve varsayımlar.
5. Donanım: model, bağlantı, attenuator/kablo ve referanslar.
6. Yazılım: sürüm, bağımlılık ve commit kimliği.
7. Düzenek: RF merkez frekansı, Fs, gain/AGC, filtre bantları, veri tipi, kayıt süresi.
8. Prosedür: başkasının tekrarlayabileceği adımlar.
9. Beklenen sonuç: deney öncesi tahmin.
10. Ölçümler: ham veri bağlantısı ve metaveri; kalibrasyon durumu.
11. Analiz: grafik, hesap, hata/belirsizlik, alternatif açıklamalar.
12. Sorunlar ve yapılan değişiklikler.
13. Sonuç: hipotez desteklendi mi, ne bilinmiyor?
14. Artık cevaplayabilmem gereken sorular.
15. Kaynakça ve sonraki deney.

IQ dosyası için asgari metaveri: RF merkez frekansı, kompleks örnekleme hızı, sayı formatı/endianness, tarih/süre, gain/AGC, donanım, filtreler ve kayıt kaynağı. SigMF uygun bir seçenektir. Kayıt boyutu yaklaşık `Fs × saniye × kompleks örnek başına byte` ile hesaplanır; örneğin complex64 için örnek başına 8 byte vardır.

## 10. Teknik doğruluk ilkeleri

- FFT bin aralığı `Fs/N`'dir. Etkin spektral çözünürlük/RBW, pencere ve ölçüm tanımına bağlıdır; zero-padding yeni fiziksel çözünürlük yaratmaz.
- Yaklaşık −174 dBm/Hz termal gürültü yoğunluğu yaklaşık 290 K içindir. Bant ve NF eklenirken tanımlar açık yazılır.
- Güç oranı için `10 log10(P2/P1)`; aynı empedansta genlik oranı için `20 log10(A2/A1)` kullanılır.
- dBFS, otomatik olarak dBm değildir. Mutlak RF güç ölçümü için referans ve kalibrasyon gerekir.
- Ortak saat/PPS, her kurulumda otomatik ve sabit faz koherensi sağlamaz. LO, başlangıç, gecikme ve kalibrasyon da incelenir.
- LoRa fiziksel katman ile LoRaWAN ağ/MAC katmanı ayrılır. WM1302 gateway genel amaçlı IQ SDR gibi varsayılmaz.
- Pluto'nun resmî destek sınırları ile modifikasyonla elde edilen çalışma aralığı birbirine karıştırılmaz.
- QO-100 RF, LNB IF ve SDR baseband frekansları ayrı kaydedilir; uyduya RF yayın, alım projesinin varsayılan parçası değildir.
- Gerçek RF verici deneylerinde bağlantı kaybı/attenuation ve cihaz giriş sınırı önceden hesaplanır. TX doğrudan RX'e bağlanmaz. İlk deneyler simülasyon veya uygun kapalı kablo düzeninde yapılır.

## 11. Kaynak omurgası

3 Ekim 2026 tarihinde erişilebilirliği kontrol edilen başlangıç kaynakları:

| Kaynak | Kullanım |
|---|---|
| [PySDR — Marc Lichtman](https://pysdr.org/) | Python ile IQ, örnekleme, DSP ve SDR çalışmaları |
| [PySDR — IQ Sampling](https://pysdr.org/content/sampling) | Hafta 5–8 için ana okuma |
| [PySDR — IQ Files and SigMF](https://pysdr.org/content/iq_files) | Kayıt formatı ve metaveri |
| [GNU Radio Tutorials](https://wiki.gnuradio.org/index.php?title=Tutorials) | Temel flowgraph ve ileri blok çalışmaları |
| [ADI — Basic internals of Pluto](https://wiki.analog.com/university/tools/pluto/users/understanding) | RFIC ve host zincirini inceleme |
| [ADI — Pluto for Developers](https://wiki.analog.com/university/tools/pluto/developers) | libiio, yazılım ve donanım geliştirme |
| [AD9363 ürün ve veri sayfası](https://www.analog.com/en/products/ad9363.html) | RF transceiver sınırları ve mimari |
| [Software-Defined Radio for Engineers — ADI](https://www.analog.com/media/en/training-seminars/design-handbooks/Software-Defined-Radio-for-Engineers-2018/SDR4Engineers.pdf) | Sistem düzeyinde SDR kitabı |

İleri kitaplar, gerektiğinde bölüm bazında: Richard Lyons, *Understanding Digital Signal Processing*; Fred Harris, *Multirate Signal Processing for Communication Systems*; Proakis/Salehi, *Digital Communications*; Bernard Sklar, *Digital Communications*; David Pozar, *Microwave Engineering*. Başlangıç için tüm kitapları satın almak veya baştan sona okumak gerekmiyor. Bölüm numaraları kullanılan baskıya göre seçilecek.

Her araştırma notunda: problem, temel varsayım, yöntem, baseline, veri, metrik, sınırlılık ve bizim deneyimize aktarılabilecek tek fikir yazılır. Hafta 47'de spectrum monitoring, SATCOM/NTN, RFML, Open RAN ve cognitive radio için bu biçimde bir araştırma haritası hazırlanır; hepsinde uzmanlaşma iddiası kurulmaz.

## 12. Başlangıç oturumu — 3–4 Ekim 2026

Yaklaşık 45–60 dakika:

- [ ] Kullanılacak bilgisayar/işletim sistemi ve haftalık çalışma saatlerini kaydet.
- [ ] Elindeki SDR, anten, kablo, attenuator ve LoRa cihazlarını listele; çalışıyor/bilinmiyor durumunu yaz.
- [ ] Python, NumPy, SciPy ve matplotlib durumunu kontrol et; donanım sürücüsüyle zaman kaybetmeden sentetik deney yapabilecek ortamı seç.
- [ ] Repo için önerilen adı ve dil yaklaşımını not et. Repo açılana kadar dosyalar yerel çalışabilir.
- [ ] Aşağıdaki soruları kaynaksız cevapla; bilmediğine “bilmiyorum” yaz.

Başlangıç soruları:

1. 1 mW kaç dBm? 1 W kaç dBm?
2. Bir güç 10 kat artarsa kaç dB artar?
3. 868 MHz için yaklaşık dalga boyu nedir?
4. IQ iki ayrı RF frekansı mı, bir kompleks temsil mi?
5. RF merkez frekansı ile kompleks Fs neden aynı olmak zorunda değil?
6. Fs = 2 MS/s ve N = 2048 için FFT bin aralığı nedir?
7. Faz farkı ile frekans farkını zaman grafiğinde nasıl ayırırsın?
8. SDR spektrumundaki sayıyı doğrudan dBm kabul eder misin?
9. Decimation öncesinde hangi işlemi yaparsın?
10. Bir bilinmeyen IQ dosyasını açmadan hangi metaveriyi istersin?

Bu değerlendirme programdan elemek için değil; hangi haftalara ek süre gerektiğini görmek içindir.

## 13. Hafta 1 — RF Fundamentals I

**Dönem:** 5–11 Ekim 2026. **Donanım gereksinimi:** yok. **Hedef:** frekans/dalga boyu/faz ile güç ve oran birimlerini ayırmak, ilk deney raporunu tamamlamak.

### Kısa ders

Bir sinüs modeli: `x(t) = A cos(2πft + φ)`. A genlik, f frekans, φ başlangıç fazıdır. Aynı frekansta fazı farklı iki sinyal zaman ekseninde kaymış görünür; frekans farkı varsa aralarındaki faz farkı zamanla değişir.

Serbest uzayda dalga boyu: `λ = c/f`, yaklaşık `c = 3 × 10^8 m/s`. Örneğin 868 MHz için yaklaşık 0,346 m. Kablodaki dalga boyu hız faktörüne göre daha kısadır.

`P_dBm = 10 log10(P_mW)`; `P_mW = 10^(P_dBm/10)`. dB bir orandır; dBm 1 mW referanslı mutlak güç seviyesidir. dBi izotropik antene göre kazançtır; doğrudan güç birimi değildir.

### Günlük görevler

| Gün | Görev | Tamamlanma kanıtı |
|---|---|---|
| Pazartesi | Sinüs, frekans, faz ve λ konusunu çalış | 433/868/2400 MHz için üç dalga boyu |
| Salı | dB/dBm ve güç-genlik ayrımı; aşağıdaki hesaplar | Ara adımlı çözüm sayfası |
| Çarşamba | Python'da 1 kHz iki sinüs oluştur; faz farkını 0°, 90°, 180° seç | Birimli zaman ekseni ve üç grafik |
| Perşembe | Frekanslardan birini 1,1 kHz yap; faz/frekans farkını açıkla | Beş cümlelik yorum |
| Cuma | dBm↔mW dönüşüm fonksiyonları yaz; link budget hesapla | Script ve en az üç elle doğrulanmış örnek |
| Cumartesi | LAB-001 raporu ve “dB/dBm öğrenirken yaptığım hatalar” notu | Şablona uygun rapor; ölçüm yerine hesap/simülasyon etiketi |
| Pazar | Beş soruyu notsuz cevapla ve ilerleme satırını doldur | Puan ve tek telafi maddesi |

### LAB-001 — Güç ve link budget

Hesaplar:

1. 1 mW, 10 mW, 100 mW ve 1 W değerlerini dBm'e çevir.
2. 3 dBm, 13 dBm ve 20 dBm değerlerini mW'a çevir.
3. Güç iki katına çıktığında dB artışını hesapla.
4. Aynı empedansta gerilim iki katına çıktığında güç oranını ve dB artışını hesapla.
5. TX = 20 dBm; TX anteni = 6 dBi; RX anteni = 3 dBi; path loss = 105 dB; toplam kablo kaybı = 2 dB. RX gücünü hesapla.
6. Bu örnekte RX hassasiyetinin −100 dBm olduğunu varsay: nominal marj kaç dB? Bu sayı sahada güvenilir bağlantı garantisi verir mi?

Doğrulama anahtarı; önce kendin çöz:

- 1/10/100/1000 mW → 0/10/20/30 dBm.
- 3/13/20 dBm → yaklaşık 1,995/19,953/100 mW.
- Güç ×2 → yaklaşık +3,010 dB.
- Aynı empedansta gerilim ×2 → güç ×4 → yaklaşık +6,021 dB.
- RX = 20 + 6 + 3 − 105 − 2 = **−78 dBm**.
- Nominal marj = −78 − (−100) = **22 dB**. Yayılım/fading, girişim, polarizasyon ve gerçek donanım koşulları ayrıca değerlendirilir.

### LAB-002 — Faz ve frekans

Örnekleme hızı 100 kS/s, süre 20 ms, genlik 1 olarak başla. Önce 1 kHz iki sinüsü çiz; ikincinin fazını değiştir. Sonra ikinci sinyali 1,1 kHz yap. Grafiklerde sadece ilk birkaç milisaniyeyi de göster. Zaman adımının `1/Fs` olduğunu açıkla. Bu hafta FFT gerekmez.

Teslimler: `week-01/theory.md`, `labs/LAB-001-db-dbm.md`, `labs/LAB-002-phase-frequency.md`, çalıştırılabilir Python script'i ve grafikler. Bu isimler önerilen repo hedefleridir; bu plan hazırlanırken deney yapılmış sayılmaz.

### Hafta sonu sözlü soruları

- 20 dBm ile 20 dB arasındaki fark nedir?
- Güçte +3 dB neden gerilimde iki kat anlamına gelmez?
- Anten kazancı enerjiyi nereden elde eder?
- Frekans artınca serbest uzaydaki dalga boyuna ne olur?
- Faz farkı ve frekans farkı arasındaki farkı deney grafiğinden nasıl anlarsın?

## 14. İlerleme kaydı

Her hafta aşağıdaki satır çoğaltılır. Saat ve puanlar gerçek çalışma sonrasında girilir.

| Hafta | Durum | Gerçek saat | Teori /20 | Hesap /20 | Deney /30 | Rapor /20 | Soru /10 | Kanıt bağlantısı | Açık sorun | Sonraki karar |
|---:|---|---:|---:|---:|---:|---:|---:|---|---|---|
| 1 | Başlamadı | — | — | — | — | — | — | — | Başlangıç envanteri | LAB-001 ile başla |

Durumlar: başlamadı / çalışılıyor / inceleme bekliyor / telafi / tamamlandı. Yayın durumu ayrıca taslak / doğrulandı / yayımlandı olarak izlenir. Öğrenme puanı ile paylaşım sayısı birbirinin yerine kullanılmaz.

Haftalık geri bildirim mesajı şablonu:

> Hafta: …; ayırdığım süre: …; tamamladıklarım: …; kod/rapor: …; zorlandığım konu: …; cevaplayamadığım soru: …; gelecek hafta uygun saatim: …

Bu mesajla sıradaki haftanın ders, hesap ve laboratuvarı mevcut duruma göre uyarlanabilir.

## 15. İkinci yıl yönü

İlk yılın sonunda tek ana uzmanlık alanı seçilir. Mevcut ilgi ve cihaz bağlamına göre **LoRa/spectrum monitoring + SATCOM alım sistemleri** güçlü adaylardır. FPGA, koherent çok kanallı alıcı veya RFML bu ana alanı destekleyen derinleşme konusu olabilir.

İkinci yıl başarı kanıtları: daha gerçekçi saha ölçümleri, bağımsız tekrar üretme, bir açık kaynak katkısı, teknik seminer ve araştırma raporu. Akademik yayın sayısı önceden garanti edilmez; özgün soru ve yeterli kanıt oluşursa değerlendirilir.

**Şimdi yapılacak ilk iş:** başlangıç envanterini doldur, LAB-001'in altı hesabını çöz ve çözümlerini kontrol anahtarına bakmadan kaydet.
