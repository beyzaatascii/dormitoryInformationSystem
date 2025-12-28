# 🎓 Öğrenci Yönetimi ve Etkinlik Planlama Sistemi

Bu proje, bir öğrenci yurdunun idari süreçlerini ve bu süreçlere bağlı etkinlik organizasyonlarını dijitalleştirmek amacıyla geliştirilmiş, **Nesne Yönelimli Programlama (OOP)** ve **Temel Veri Yapıları** prensiplerine dayalı bir Python uygulamasıdır.

---

## 🏗️ Mimari Yapı ve Tasarım

Proje iki ana bağımsız modülden oluşmaktadır. Her modül, kendine has veri yapıları kullanarak performansı ve veri tutarlılığını maksimize eder.

### 1. 🏠 Yurt Otomasyon Modülü (`Dorm_Automation`)
Bu modül, bir öğrenci yurdunun giriş-çıkış, izin ve finansal takip süreçlerini yönetir.



* **LIFO (Stack) Mantığı:** Öğrenci kayıtları ve çıkış işlemleri `students_stack` adlı bir liste üzerinde Stack veri yapısı kullanılarak yönetilir.
* **Kalıtım (Inheritance):** `Sorgula` sınıfı, `Dorm_Automation` sınıfından miras alarak ücret ve izin durumlarını kontrol eden spesifik metodlar sunar.
* **Özellikler:**
    * Öğrenci ekleme ve son eklenen kaydı geri alma (pop).
    * İzin günü takibi ve otomatik azaltma işlemleri.
    * Yemek ve ücret ödeme durumlarının takibi ve raporlanması.

### 2. 🎟️ Etkinlik Planlama Modülü (`EventPlanningSystem`)
Öğrencilerin sosyal faaliyetlere katılımını organize eden ve biletleme süreçlerini yöneten modüldür.



* **FIFO (Queue) Mantığı:** Rezervasyon talepleri, `collections.deque` kullanılarak bir kuyruk (queue) yapısında saklanır. Bu sayede "ilk gelen ilk hizmeti alır" prensibi uygulanır.
* **Dinamik Kaynak Yönetimi:** Etkinlik bazlı bilet limitleri ve ulaşım için otobüs kapasiteleri dinamik olarak güncellenebilir.
* **Özellikler:**
    * Sınırlı kontenjanlı etkinlik tanımlama.
    * Rezervasyon taleplerini sıraya alma ve sırayla onaylama (`process_reservations`).
    * Öğrenci bazlı bilet sahipliği sorgulama.

---

## 🛠️ Teknik Yetkinlikler

* **Veri Yapıları:** Stack (Yığın) ve Queue (Kuyruk) yapıları ile veri akış yönetimi.
* **OOP Prensipleri:** Sınıf yapıları, yapıcı metodlar (`__init__`), ve sınıflar arası kalıtım.
* **Dinamik Veri Yönetimi:** Python sözlükleri (dictionaries) ile karmaşık öğrenci ve etkinlik verilerinin saklanması.

---

## 🚀 Kurulum ve Kullanım

### Ön Koşullar
* Bilgisayarınızda **Python 3.x** kurulu olmalıdır.

### Çalıştırma
1.  Projeyi klonlayın:
    ```bash
    git clone [https://github.com/beyzaatascii/student-management-system.git](https://github.com/beyzaatascii/student-management-system.git)
    ```
2.  Proje klasörüne gidin:
    ```bash
    cd student-management-system
    ```
3.  Uygulamayı başlatın:
    ```bash
    python main.py
    ```

---

## 📋 Örnek Menü Etkileşimi
Program başlatıldığında kullanıcıyı şu seçenekler karşılar:
1.  **Yurt İşlemleri:** Öğrenci kayıt, izin güncelleme, ödeme sorgulama.
2.  **Etkinlik İşlemleri:** Yeni etkinlik açma, bilet rezerve etme, kuyruk işleme.

---


