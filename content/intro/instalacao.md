# Instalação

Bom, se você chegou até aqui, quer dizer que realmente está interessado em dar continuade nesse aprendizado, e agora, iremos instalar o compilador em Crystal em seu computador pessoal.

## Sistemas Operacionais
- [macOS](https://github.com/lanjoni/crystal4noobs/blob/main/content/intro/instalacao.md#macos)
- [Windows](https://github.com/lanjoni/crystal4noobs/blob/main/content/intro/instalacao.md#windows)
- [Debian/Ubuntu e derivados](https://github.com/lanjoni/crystal4noobs/blob/main/content/intro/instalacao.md#debianubuntu-e-derivados)
- [Red Hat/Fedora e derivados](https://github.com/lanjoni/crystal4noobs/blob/main/content/intro/instalacao.md#red-hatfedora-e-derivados)
- [OpenSUSE](link-terceira-parte)
- [Arch Linux/Manjaro e derivados](link-terceira-parte)
- [Gentoo](link-terceira-parte)
- [FreeBSD](link-terceira-parte)

---

### macOS
A instalação do Crystal para o macOS é feita utilizando o gerenciador de pacotes <a href="https://brew.sh/">Homebrew</a>. Para realizar sua instalação utilize os seguintes comandos no terminal:
```
brew update
brew install crystal
```
Para instalar uma nova versão do Crystal basta executar:
```
brew upgrade crystal
```
Para mais informações sobre a instalação do Crystal no macOS clique <a href="https://crystal-lang.org/install/on_mac_os/">aqui!</a>

#

### Windows
Caso você esteja utilizando Windows, recomendo que instale alguma distribuição Linux de sua preferência para utilizar juntamente do WSL. O compilador Crystal ainda não consegue rodar nativamente no Windows, e por isso, sua compatibilidade é gerenciada pelo WSL no Windows. Para mais informações sobre a instalação do WSL clique <a href="https://docs.microsoft.com/en-us/windows/wsl/install">aqui!</a>

#

### Debian/Ubuntu e derivados
Para iniciar nossa intalação, primeiramente precisamos adicionar o repositório deb oficial do Crystal, e para isso execute em seu terminal:
```
curl -fsSL https://crystal-lang.org/install.sh | sudo bash
```
ou 
```
curl -fsSL https://crystal-lang.org/install.sh | sudo bash -s -- --channel=nightly
```
Para dar continuidade em nosso setup manual exeute:
```
echo "deb http://download.opensuse.org/repositories/devel:/languages:/crystal/{REPOSITORY}/ /" | sudo tee /etc/apt/sources.list.d/crystal.list

curl -fsSL https://download.opensuse.org/repositories/devel:languages:crystal/{REPOSITORY}/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/crystal.gpg > /dev/null
```
Agora que os repositórios já estão proprieamente adicionados, vamos instalar o compilador Crystal:
```
sudo apt update
sudo apt install crystal
```

Na documentação oficial é recomendado a adição de algumas bibliotecas para funcionalidades específicas, e caso queira adicionar, execute:
```
sudo apt install libssl-dev
sudo apt install libxml2-dev
sudo apt install libyaml-dev
sudo apt install libgmp-dev
sudo apt install libz-dev
```

Quando uma nova versão do Crystal for lançada, você pode instalá-la executando:
```
sudo apt update
sudo apt install crystal
```

#

### Red Hat/Fedora e derivados
