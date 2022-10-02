<h1 align="center"> Transformers node qurulumu  8.0 </h1>

* Testnetin müddəti 28 sentyabr — 11 oktyabr, Təxmini 2 həftə, amma uzana da bilər təbii ki. 

```bash
Prosessor: 8 nüvəli 2.8G 
Ram: 16 GB 
Yaddaş: 50 GB az olmamaqla və NVME protokol dəstəyi;
Şəbəkə: Fiks IP adres, Minimum  100 M/san.
```

Əgər daha öncə qurmusunuzsa "ttfsc_x.y.z_devnet" , "ttfsc_x.y.z_testnet" , "config.json" faylını və "data.DB" papkasını silirik. Cert papkasına əl vurmuruq. Onu backup edib bir yerdə saxlayın.
```bash
* aktiv sessiyaya daxil oluruq
```bash
cd $HOME/tfsc && screen -r tfsc
```
* daxil olub certdən başqa bütün papkaları silirik
```bash
rm -rf $HOME/tfsc/data.db $HOME/tfsc/config.json $HOME/tfsc/ttfs_v0.7.0_61ec7b1_devnet
```

* ttfs_v0.8.0_76a6414_devnet sonuncu versiyanı yükləyirik

```bash
wget -q uscloudmedia.s3.us-west-2.amazonaws.com/transformers/test/ttfs_v0.8.0_76a6414_devnet
```
* fayla icazə veririk. 

```bash
chmod +x ttfs_v0.8.0_76a6414_devnet
```
*  Proqramı başladırıq, ilk başladıqda config.json faylı yaradılacaq. 
```bash
./ttfs_v0.8.0_76a6414_devnet -c
```
* Proqramı saxlayırıq. ctrl+c

* Proqramı başladırıq. Menu görüntüsü ilə.
```bash
./ttfs_v0.8.0_76a6414_devnet -m
```

<h1 align="center">  Əgər ilk dəfə qurursunuzsa bu addımları edin. Ümumiyyətlə məsləhət görərdim ki, köhnəni əllə silib sıfırdan bununla qurasınız. </h1>

* Yenilənmə edirik 
```bash
sudo apt update && sudo apt upgrade -y
```
* Lazım olan utilitiləri yükləyirik
```bash
sudo apt install screen -y
```
* Proqram üçün ayrıca direktoriya yaradıb ona daxil oluruq. 
```bash
mkdir $HOME/tfsc && cd tfsc
```
* Proqramın sonuncu versiyasını yükləyirik ttfs_v0.8.0_76a6414_devnet
```bash
wget -q uscloudmedia.s3.us-west-2.amazonaws.com/transformers/test/ttfs_v0.8.0_76a6414_devnet
```
* Fayla icazə veririk.
```bash
chmod +x ttfs_v0.8.0_76a6414_devnet
```
* Proqramı başladırıq. config.json yaradılacaq.
```bash
./ttfs_v0.8.0_76a6414_devnet -c
```
* Screenlə sessiya yaradırıq.
```bash
screen -S tfsc
```
* Proqramın olduğu yerdən ip icazə veririk. 
```bash
PUB_IP=$(wget -qO- eth0.me);wget -qO- pastebin.com/raw/MfS126mf|sed 's#\"ip\": \"pub_ip\"#\"ip\": '\"${PUB_IP}\"'#' > config.json
```
* Proqramı menu görüntüsü ilə başladırıq. cert papkası yaradılacaq. Onu sonra yaddaşda saxlayırıq. 
```bash
./ttfs_v0.8.0_76a6414_devnet -m
```


Bundan sonra node sinxronizasiya olmağa başlayır. 
* Blok sayına 7+enter basmaqla baxmaq olar. HƏm də adresiniz çıxır, onu kopyalayıb götürün. 

* Sinxron olandan bir müddət sonra komanda özü sizə token yollayacaq. 
* 10 token yollayacaqlar onu gözləyib 9.9-unu stake edirsiniz. Stake etmək üçün 2 yazıb enter vurun, 9.9 yazıb enter vurun.
* HƏr gün girib 1 dəfə claim edin heç olmasa. Yenilikləri izləyin, tez-tez yenilənmə gəlir adətən. Bir də əsas olaraq CERT papkasını back up edin. config fayl onun içindədir. 

# Token məsələsi 
* Token məsələsi bir az dəyişib. İndi Discordda faucet bölməsində "!faucet adresiniz" yazmaqla 5001 ədəd token alacaqsınız. Ondan sonra stake edərkən, 5000 ədəd edəcəksiniz. Gündə iki dəfə girib claim edin. Gecə vaxtı bonuslar sıfırlanır

Telegram kanalımız. https://t.me/drtestnet
Proyektin discordu: https://discord.gg/e2sMMbzTt2
