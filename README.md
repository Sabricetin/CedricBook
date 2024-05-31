
# Karakter Listesi Uygulaması

Bu Swift kodu, bir `UITableView` kullanarak belirli karakterleri listeleyen ve kullanıcıların bu karakterleri seçerek detaylarını görüntüleyebileceği bir iOS uygulaması oluşturuyor. Kod, temel olarak bir `UIViewController` sınıfını genişletir ve `UITableViewDelegate` ve `UITableViewDataSource` protokollerini uygular.

## Özellikler

- **Veri Kaynakları:**
  - `characters`: Karakterlerin isimlerini, açıklamalarını ve görüntülerini tutar.
  - `selectedCharacter`: Seçilen karakterin adı, açıklaması ve görüntüsü.

## View Did Load

- `tableView` için `delegate` ve `dataSource` atanır.
- `characters` dizisi karakter verileriyle doldurulur.

## UITableViewDataSource

- `tableView(_:numberOfRowsInSection:)`: Satır sayısını `characters` dizisinin eleman sayısı olarak döner.
- `tableView(_:cellForRowAt:)`: Her bir hücreyi karakter adıyla doldurur.

## UITableViewDelegate

- `tableView(_:didSelectRowAt:)`: Bir satır seçildiğinde, seçilen karakter atanır ve detaylar sayfasına geçiş yapılır (`performSegue`). `prepare(for:sender:)` yöntemiyle geçiş işlemi sırasında seçilen karakterin adı, açıklaması ve görüntüsü, hedef ViewController'a (`DetailsViewController`) aktarılır.

## Ekran Görüntüleri


![Simulator Screen Recording - iPhone 15 Pro - 2024-05-31 at 03 15 30](https://github.com/Sabricetin/CedricBook/assets/114506296/8949f3c3-00f4-432e-825f-8507246dafaf)

## Kullanım

- Ana ekranda karakterlerin listesini göreceksiniz.
- Bir karaktere tıklayarak detaylarını görüntüleyebilirsiniz.

