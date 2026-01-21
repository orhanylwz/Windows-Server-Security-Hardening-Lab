Active Directory management and GPO security hardening project on Windows Server 2022.
# Windows Server 2022 Active Directory & Security Hardening Lab

Bu proje, kurumsal bir ağ altyapısının **Sıfır Güven (Zero Trust)** ve **En Az Yetki (Least Privilege)** prensiplerine uygun olarak nasıl yapılandırılacağını ve siber güvenlik standartlarına göre nasıl sıkılaştırılacağını (Hardening) göstermektedir.

## Uygulanan Teknik Senaryolar

### 1. Kimlik ve Erişim Yönetimi (IAM)
* **Kullanıcı Yaşam Döngüsü:** Yeni personel alım süreçlerinde Role-Based Access Control (RBAC) uygulanarak admin yetkilendirmeleri yapıldı.
* **Hesap Güvenliği:** Olası Brute-Force saldırıları sonrası kilitlenen hesapların güvenli kurtarma ve şifre sıfırlama süreçleri simüle edildi.
* **Gelişmiş Denetim:** "Advanced Features" ve "Attribute Editor" kullanılarak nesnelerin teknik metaverileri ve adli inceleme detayları analiz edildi.

### 2. Servis Hesabı Güvenliği (Hardening)
* Kritik servis hesapları için **Logon Hours** kısıtlaması uygulanarak, saldırı yüzeyi (Attack Surface) sadece mesai saatleriyle sınırlandırıldı.

### 3. Group Policy (GPO) Güvenlik Politikaları
* **Veri Sızıntısı Önleme (DLP):** USB ve harici depolama birimlerine erişim merkezi olarak engellendi.
* **Yetki Kısıtlaması:** Son kullanıcıların kritik sistem ayarlarına erişmesini önlemek için Denetim Masası kısıtlandı.
* **Yasal Uyarı Mekanizması:** Interactive Logon mesajları ile kurumsal erişim sınırları ve yasal uyarılar sisteme entegre edildi.

### 4. Doğrulama ve Uyumluluk
* Uygulanan tüm politikaların sistem geneline başarıyla dağıtıldığı `gpupdate /force` komutu ile doğrulandı.

## 💻 Kullanılan Teknolojiler
* Windows Server 2022 (Domain Controller)
* Active Directory Domain Services (AD DS)
* Group Policy Management (GPO)
* VMware Workstation
