
Aqui será falado como fazer uma instalação rápida do Arch linux utilizando o instalador archinstall.

Requesitos:
- Computador (opcional)
- [ISO Arch linux](https://archlinux.org/download/)
- Pendrive

## Criando o Pendrive

Primeiramente é necessário construir um meio de instalação, uma das maneiras mais comuns de se fazer é colocando o instalador dentro de um pendrive.

uma maneira fácil de se fazer é utilizando o aplicativo [Ventoy](https://www.ventoy.net/en/download.html), onde parte do HD será dedicada para um pequeno programa, mas por parte do usuário será necessário apenas colocar o arquivo .ISO dentro da pasta.
[Download Alternativo Ventoy](https://sourceforge.net/projects/ventoy/files/)

### Windows
Para sistemas Windows terá um executável na pasta baixada, o aplicativo é fácil de entender e não precisa de muita explicação, coloque o Pendrive, clique botão, jogue .ISO no pendrive.
### Linux

Linux é um pouquinho mais complicado porque até onde fui não consegui encontrar uma ferramenta com GUI. mas é possivel tranquilamente fazer a mesma instalação por este tutorial
https://www.youtube.com/watch?v=6aZc2yqDN9o


## Instalando

Com o pendrive em mãos coloque ele no computador e entre na BIOs do seu computador. aqui é importante resaltar alguns detalhes:

o instalador irá procurar por padrões EFI, softwares modernos instalados na BIOs que auxiliam com compatibilidade. lembre-se de selecionar para a BIOs iniciar com padrões modernos e não o padrão legado.

Após isto inicie o pendrive com o Ventoy e selecione a ISO do arch linux.

Ao iniciar o arquivo .ISO você será recebido pela tela inicial do arch linux, podera ser levemente diferente mas o importante é entrar na opção Install Arch Linux ou similar.
![[Pasted image 20240422123536.png]]

Após isto veremos uma longa lista de simbolos e textos com alguns dando OK e outros poucos FAILURE e então seremos recebidos por uma tela preta: o Bash!

Inicialmente antes de fazer qualquer coisa, precisamos atualziar o archinstall que esta presente no pendrive: 
```sh
sudo pacman -S archinstall
```
arch linux busca funcionar perfeitamente com uma conexão cabeada logo de frente.
em seguida podemos instalar o sistema executando o pacote instalado.
```sh
archinstall
```

