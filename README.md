# recon-vpn-setup
Bug Bounty Recon VPN - tools install 

## Att

```
apt-get update && apt-get update
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

## Instalando Coisas Básicas

```
apt-get install nmap dirb 
```
