# bootcamp-project-metro-simulation
# Metro Ağı Simülasyonu

Bu proje, bir metro ağı içindeki istasyonlar arasında en az aktarmalı ve en hızlı rotayı bulmaya yönelik bir Python uygulamasıdır. Uygulama, **BFS (Breadth-First Search)** ve **A* (A-star)** algoritmalarını kullanarak en uygun yolları hesaplar.

## Kullanılan Teknolojiler ve Kütüphaneler
Bu projede aşağıdaki Python kütüphaneleri kullanılmıştır:
- **collections**: `defaultdict` ve `deque` kullanılarak veri yapıları yönetildi.
- **heapq**: Öncelikli kuyruk (priority queue) oluşturmak için kullanıldı.
- **typing**: Tip belirteçleri eklenerek kodun daha okunaklı olması sağlandı.

## Algoritmaların Çalışma Mantığı

### BFS (En Az Aktarmalı Rota)
- BFS, genişlik öncelikli arama algoritmasıdır.
- İlk olarak başlangıç istasyonu kuyruğa alınır.
- Her istasyondan komşularına giderek en kısa (aktarma sayısı açısından) yolu bulur.
- En kısa yolu bulduğunda algoritma durur ve rota döndürülür.
- **Avantajı:** En az aktarma sayısı olan yolu garanti eder.

### A* (En Hızlı Rota)
- A* algoritması, Dijkstra'ya benzer ancak daha akıllı seçimler yapar.
- Öncelikli kuyruk (heapq) kullanarak en düşük maliyetli yolu seçer.
- İstasyonları en kısa sürede ulaşılabilecek şekilde sıralayarak hedefe en hızlı ulaşımı sağlar.
- **Avantajı:** Süre açısından en optimal rotayı bulur.

## Örnek Kullanım ve Test Sonuçları
Aşağıda bazı test senaryoları verilmiştir:

1. **AŞTİ'den OSB'ye En Az Aktarma**
   ```bash
   En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
   ```

2. **AŞTİ'den OSB'ye En Hızlı Rota**
   ```bash
   En hızlı rota (15 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
   ```

3. **Batıkent'ten Keçiören'e En Az Aktarma**
   ```bash
   En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
   ```

4. **Keçiören'den AŞTİ'ye En Hızlı Rota**
   ```bash
   En hızlı rota (14 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
   ```

## Projeyi Geliştirme Fikirleri
Bu projeye eklenebilecek bazı geliştirmeler:
- **Gerçek zamanlı trafik verisi** eklenerek yoğunluk bazlı optimizasyon yapılabilir.
- **Farklı hat türleri** (otobüs, tramvay vb.) entegre edilebilir.
- **Grafik arayüz** eklenerek kullanıcı dostu hale getirilebilir.
- **Heuristic geliştirme** yapılarak A* algoritması daha verimli hale getirilebilir.



Bu proje, en kısa ve en hızlı metro rotalarını belirlemeye yönelik optimize edilmiş bir algoritma uygulamasıdır. 


