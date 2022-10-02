# Transformersdə invest etmə. 
* Ümumiyyətlə daha öncəkində dediyim kimi əmin olun ki,cert papkasını yaddaşda saxlamısınız. Biz indi öz köhnə cüzdanımızı bir kənara qoyub, yeni cüzdan yaradacağıq. Onunla da token alıb, birinci adresə invest edəcəyik. Birinci cüzdan A, ikinci cüzdana B adı verək
* Birinci aktiv sessiyaya daxil oluruq və 0 basmaqla proqramı saxlayırıq. 
```bash
cd $HOME/tfsc && screen -r tfsc
```
* Daha sonra açarın olduğu cert papkasının (A cüzdanı) adını dəyişmək lazımdır. 
```bash
mv cert bak_cert
```
* Proqramı başladırıq. Başladandan sonra bizə yeni cert papkası (B cüzdanı) verəcək. 
```bash
./ttfs_v0.8.0_76a6414_devnet -m
```
* B cüzdanı adresinizi kopyalayın və Discorda daxil olub faucetdən "!faucet adresiniz" yazıb token istəyirik .Sizə ən geci 5-10 dəqiqə ərzində 5001 token gələcək. 
* Tokenlər gələndən sonra onları B cüzdanından, A cüzdanına delegate etmək lazımdır. Noda qayıdıb 4 yazırsınız ardınca bunları edirsiniz. Bura bir az qarışıqdır. Edərkən diqqətli olun
```bash 
AddrList:
<Burada artıq sizin B cüzdan adresiniz yazacaq> [default]
Please enter your addr:
<Buraya B cüzdan adresinizi təkrarən yazın>
```
Daha sonra, 
```bash 
Please enter the addr you want to invest to:
<A cüzdan adresinizi bura yazın>
Please enter the amount to invest:
5000
Please enter invest type: (0: NetLicence) 
0
```
* Daha sonra siz "succesfully packaged" yazısını görəcəksiniz. Bu o deməkdir ki, invest uğurla reallaşdı. 
* İndi bizə köhnə A cüzdanını yenidən aktiv cüzdan etmək lazımdır. Bunun üçün sıfır basıb enter edib nodu saxlayırıq. 0.Exit, sonra isə
```bash 
 mv cert cert_invest
```
```bash 
mv bak_cert cert
```
* Yenidən nodu başladırıq 
```bash 
./ttfs_v0.8.0_76a6414_devnet -m
```
* və sessiyadan bunlarla çıxırıq. CTRL+A+D 

* Hər ehtimala ikinci yaratdığımız papkanı da (adı artıq "cert_invest" olaraq görünəcək) backup edib saxlayın. 
