# spheron-node

*DePin gpu ionet benzeri bir sistem , hızlı bir drop alabiliriz.*

*Ne kadar yüksek sistem o kadar iyi kazanç puan demek.*

*Minumum 8gb ram 4 Gpu 160gb disk alarak kurabilirsiniz.*

![image](https://github.com/user-attachments/assets/e965545f-cd74-4f74-ab78-c425cb260c23)


Kodlar

```
# Paket listesini güncelle ve mevcut paketleri yükselt
sudo apt update -y && sudo apt upgrade -y

# Docker ile ilgili paketleri kaldır
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

# Paket listesini güncelle
sudo apt-get update

# Gerekli paketleri kur
sudo apt-get install ca-certificates curl gnupg

# Anahtar zinciri dizini oluştur
sudo install -m 0755 -d /etc/apt/keyrings

# Docker GPG anahtarını indir ve anahtar zincirine ekle
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

# Anahtar dosyasına okuma izinleri ver
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Docker deposunu kaynak listesine ekle
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Paket listesini tekrar güncelle ve mevcut paketleri yükselt
sudo apt update -y && sudo apt upgrade -y

# Docker'ı ve ilgili bileşenlerini kur
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Docker Compose'a çalıştırma izinleri ver
sudo chmod +x /usr/local/bin/docker-compose

# Docker sürümünü kontrol et
docker --version
```

Devamı 


```
chmod +x /root/fizzup.sh

./fizzup.sh
```


Log kontrol için

```
docker compose -f ~/.spheron/fizz/docker-compose.yml logs -f

```

