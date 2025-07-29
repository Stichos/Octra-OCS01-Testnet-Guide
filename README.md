Octra OCS01-Testnet Rehberi

Bu Github Rehberinde OCS01 testnetini nasıl yapacağınızı göstericem.

Hangi Sistemlerde Çalışır?
•Linux (Ubuntu, Fedora vb.)
•macOS
•Windows (WSL ya da Rust kuruluysa doğrudan)

İlk başta Rust indiricez varsa bu adımı atlayın.
`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`

`source $HOME/.cargo/env`

Rust yüklendikten sonra terminali yeniden başlat.

Projeyi İndir & Derle

`git clone https://github.com/octra-labs/ocs01-test.git`

`cd ocs01-test`

`cargo build --release`

Derleme tamamlandığında ./target/release/ocs01-test dosyası oluşmuş olacak.

Gerekli Dosyaları Hazırla
Projeyi çalıştırmak için birkaç ek dosyaya ihtiyacın olacak:

`cp EI/exec_interface.json . `

Aynı dizine wallet.json dosyasını da eklemen gerekiyor. Bu dosya, testnet cüzdan bilgilerini içeriyor.
❗ ocs01-test, exec_interface.json ve wallet.json aynı klasörde olmalı.

wallet.jsondaki bilgileri kendi B64 formatındaki private key ve adresinle değiştirmeyi unutma.

OCS01 arayüzünü başlatıyoruz:

`./target/release/ocs01-test`

Açılan menüden:
•Kontrat verilerini görüntüleyebilirsin
•Fonksiyonları test edebilirsin (örneğin token gönderme, veri okuma vb.)

Tüm işlemler testnet üzerinde gerçekleşir.

Faucet: https://faucet.octra.network
Eğer tokenın yoksa X de Octra postumun altına cüzdan adresinle yorum atabilirsin.

Dikkat Edilmesi Gerekenler
•exec_interface.json dosyası belirli bir test kontratı için hazırlanmıştır:
octBUHw585BrAMPMLQvGuWx4vqEsybYH9N7a3WNj1WBwrDn

Değiştirmene gerek yok, olduğu gibi kullan.

Neden Tesneti yapıyorum ?

•Tek ve faal olan tek ZHE L1 olduklarını söylüyolar.İddialı bir söylem erkenden içerde olmaya çalışıyorum.
•Geri bildirimlerinle projeye katkı sağlayabilirsin.
•Olası bir airdrop için işlemlerimizi erkenden yapıyoruz.

Octra Discorduna girin ve projeye katkıda bulunmaya çalışın.

4M$ yatırımları var.

<img width="2048" height="1034" alt="image" src="https://github.com/user-attachments/assets/7d22e70c-b1fe-419f-94a7-9f88c7a9359d" />
