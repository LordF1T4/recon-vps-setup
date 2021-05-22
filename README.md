# recon-vpn-setup
Instalação das tools para Recon VPN 

# Att
> apt-get update && apt-get update
 
# Instalação do Go

selecione a versão  que você deseja instalar, no nosso exemplo estamos utilizando a versão 1.13
> VERSAO_GO=1.13
> cd ~
> curl -O "https://dl.google.com/go/go${VERSAO_GO}.linux-amd64.tar.gz"
> tar xvf "go${VERSAO_GO}.linux-amd64.tar.gz"
> chown -R root:root /usr/local/go
> sudo mv go /usr/local
> sudo nano ~/.profile
> export GOROOT=$HOME/go
> export GOPATH=$HOME/work
> export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
> source ~/.profile
> go version


