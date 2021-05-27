# recon-vps-setup
Bug Bounty Recon VPS - tools install 

## Repositórios kali no ubuntu / Update
> Rodar tudo como root!
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
## Mantendo sessão ssh da ec2 ativa
```
echo 'ClientAliveInterval 60' >> /etc/ssh/sshd_config && service ssh restart
```
### Criação de Diretórios
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
> Setando o Path:
```
echo '# Setando GoPath' >>~/.bashrc && echo 'export GOROOT=/usr/local/go' >>~/.bashrc && echo 'export GOPATH=/root/go' >>~/.bashrc &&
echo 'export PATH=$PATH:/usr/local/go/bin:/root/go/bin' >>~/.bashrc && echo '' >>~/.bashrc && echo '# Meus Aliases' >>~/.bashrc && echo "alias lista='wc -l *'" >>~/.bashrc && source ~/.bashrc && go version
```

### Instalando Ferramentas pelo apt-get
```
apt-get install nmap dirb dnsenum wafw00f whois sqlmap wpscan sublist3r -y
```
### SecretFinder - Busca dados sensíveis nos .js
```
git clone https://github.com/m4ll0k/SecretFinder.git && cd SecretFinder && pip3 install -r requirements.txt
```
### LinkFinder - Busca Endpoints nos .js
```
git clone https://github.com/GerbenJavado/LinkFinder.git && cd LinkFinder && python3 setup.py install
```
### github-search - Faz busca no GitHub
```
git clone https://github.com/gwen001/github-search.git && cd github-search && pip3 install -r requirements3.txt
```
## Todas ferramentas abaixo (1liner):
```
go get -v github.com/projectdiscovery/subfinder/cmd/subfinder && go get -u github.com/tomnomnom/assetfinder && go get -v github.com/OWASP/Amass/v3/... && go get github.com/tomnomnom/waybackurls && go get github.com/003random/getJS && go get -u github.com/hiddengearz/jsubfinder && go get -v github.com/projectdiscovery/httpx/cmd/httpx && go get -u github.com/tomnomnom/fff && go get -u github.com/tomnomnom/anew && go get -v github.com/hahwul/dalfox/v2 && go get -u github.com/jaeles-project/gospider && go get -u github.com/tomnomnom/hacks/html-tool && go get -u github.com/tomnomnom/httprobe
```
### SubFinder - Enumera Subdomínios
```
go get -v github.com/projectdiscovery/subfinder/cmd/subfinder
```
### AssetFinder - Enumera Dominios e Subdomínios
```
go get -u github.com/tomnomnom/assetfinder
```
### Amass - Mapping / Asset Finder
```
go get -v github.com/OWASP/Amass/v3/...
```
### WayBackURLs - Consulta Wayback Machine
```
go get github.com/tomnomnom/waybackurls
```
### GetJS - Enumera todos .js do alvo
```
go get github.com/003random/getJS
```
### JSubFinder - Garimpa subdom e secrets em .js
```
go get -u github.com/hiddengearz/jsubfinder
```
### HTTPX - Checa ativos
```
go get -v github.com/projectdiscovery/httpx/cmd/httpx
```
### Httprobe - Chega ativos
```
go get -u github.com/tomnomnom/httprobe
```
### fff - Checa .js ativos
```
go get -u github.com/tomnomnom/fff
```
### anew - Retira duplicados / Junta listas
```
go get -u github.com/tomnomnom/anew
```
### DalFox - Xss Finder
```
go get -v github.com/hahwul/dalfox/v2
```
### GoSpider - Webspider
```
go get -u github.com/jaeles-project/gospider
```
### FDsploit - Directory Traversal Tester
```
git clone https://github.com/chrispetrou/FDsploit.git && cd FDsploit && pip3 install -r requirements.txt
```
### Html-Tools - tomnomnom - busca comentários no código
```
go get -u github.com/tomnomnom/hacks/html-tool
```
