# recon-vps-setup
Bug Bounty Recon VPS - tools install 

## Repositórios kali no ubuntu / Update

```
sudo su
```
> Adicionar ao /etc/apt/sources.list
- deb http://http.kali.org/kali kali-rolling main non-free contrib
- deb-src http://http.kali.org/kali kali-rolling main non-free contrib

```
apt-key adv --recv-keys --keyserver keyserver.ubuntu.com ED444FF07D8D0BF6 
apt-get update && apt-get update && apt-get install net-tools
```

## Criação de Diretórios

```
mkdir downloads && mkdir tools && mkdir tests && mkdir hackerOne && mkdir bugCrowd
```

## Instalação do Python

```
apt-get install python3 python3-pip -y
```
 
## Instalação do Go

> Selecione a versão  que você deseja instalar

```  
VERSAO_GO=1.1
cd ~
curl -O "https://dl.google.com/go/go${VERSAO_GO}.linux-amd64.tar.gz"
```
```
tar xvf "go${VERSAO_GO}.linux-amd64.tar.gz"
```
```
chown -R root:root /usr/local/go
sudo mv go /usr/local
```
> sudo nano ~/.profile
```    
export GOROOT=$HOME/go
export GOPATH=$HOME/work
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
```
> salva e sai
```
source ~/.profile
go version
```

## Instalando Ferramentas

```
apt-get install nmap dirb dnsenum wafw00f whois sqlmap wpscan -y
```
```

```
