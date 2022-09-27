<h1 align="center"> Transformers node qurulumu  </h1>

* Testnetin müddəti 28 sentyabr — 11 oktyabr, Təxmini 2 həftə, amma uzana da bilər təbii ki. 

```bash
Prosessor: 8 nüvəli 2.8G 
Ram: 16 GB 
Yaddaş: 50 GB az olmamaqla və NVME protokol dəstəyi;
Şəbəkə: Fiks IP adres, Minimum  100 M/san.
```

Əgər daha öncə qurmusunuzsa "ttfsc_x.y.z_devnet" , "ttfsc_x.y.z_testnet" , "config.json" faylını və "data.DB" papkasını silirik. Cert papkasına əl vurmuruq. 
Əgər heç qurmamısınızsa, elə buradan başlayırıq. 
```bash
tmux new -s nodeadi
```
```bash
mkdir tfsc 
```
```bash
cd tfsc
```

* ttfsc_v0.6.0_a318309_devnet sonuncu versiyanı yükləyirik

```bash
wget -q fastcdn.uscloudmedia.com/transformers/test/ttfsc_v0.6.0_a318309_devnet
```
* fayla icazə veririk. 

```bash
chmod +x ttfsc_v0.6.0_a318309_devnet
```
*  Proqramı başladırıq, ilk başladıqda config.json faylı yaradılacaq. 
```bash
./ttfsc_v0.6.0_a318309_devnet
```
* Proqramı saxlayırıq. ctrl+c

* Proqram olduğu yerdən, bu skripti yazın. Avtomatik olaraq sizin IP-nizi config.json faylına yükləyəcək.
```bash
PUB_IP=$(wget -qO- eth0.me);wget -qO- pastebin.com/raw/MfS126mf|sed 's#\"ip\": \"pub_ip\"#\"ip\": '\"${PUB_IP}\"'#' > config.json
```
* Proqramı başladırıq. Menu görüntüsü ilə.
```bash
./ttfsc_v0.6.0_a318309_devnet -m
```
Bundan sonra node sinxronizasiya olmağa başlayır. 
* Blok sayına 7+enter basmaqla baxmaq olar. HƏm də adresiniz çıxır, onu kopyalayıb götürün. 

* Sinxron olandan bir müddət sonra komanda özü sizə token yollayacaq. 
* 10 token yollayacaqlar onu gözləyib 9.9-unu stake edirsiniz. Stake etmək üçün 2 yazıb enter vurun, 9.9 yazıb enter vurun. 
* HƏr gün girib 1 dəfə claim edin heç olmasa. Yenilikləri izləyin, tez-tez yenilənmə gəlir adətən. Bir də əsas olaraq CERT papkasını back up edin. config fayl onun içindədir. 

Telegram kanalımız. https://t.me/drtestnet
Proyektin discordu: https://discord.gg/e2sMMbzTt2
