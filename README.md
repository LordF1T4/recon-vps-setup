# recon-vps-setup
Bug Bounty Recon VPS - tools install 

## Repositórios kali no ubuntu / Update

```
sudo su
```
> Adicionar ao /etc/apt/sources.list
```
printf "#Repositórios do Kali\ndeb http://http.kali.org/kali kali-rolling main non-free contrib\ndeb-src http://http.kali.org/kali kali-rolling main non-free contrib\n" >> /etc/apt/sources.list
```
> Adicionar a chave e atualizar
```
apt-key adv --recv-keys --keyserver keyserver.ubuntu.com ED444FF07D8D0BF6 
apt-get update && apt-get update && apt-get install net-tools -y
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

> Conferir última versão do Go em https://golang.org/doc/install

```
cd ~ && wget https://golang.org/dl/go1.16.4.linux-amd64.tar.gz && tar xvf go1.16.4.linux-amd64.tar.gz && rm -r go1.16.4.linux-amd64.tar.gz
```
```
chown -R root:root ./go && mv go /usr/local
```
```
echo 'export PATH=$PATH:/usr/local/go/bin' >>~/.profile && source ~/.profile && go version
```

## Instalando Ferramentas

```
apt-get install nmap dirb dnsenum wafw00f whois sqlmap wpscan -y
```
```

```
