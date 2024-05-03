# Instalando Essenciais

Precisamos instalar os pacotes essenciais para o desenvolvimento em C#! Atualmente 2024 eu estou com Linux, pois 2024 é o ano do Linux!

A microsoft tem um ambiente muito interessante em que quanto mais próximo do windows e da maneira que a microsoft programa, mais facil são as coisas: se programar no windows tem acesso á IDE gratuita oficial: Visual Studio enquanto no linux/mac tem acesso somente ao visual studio code, que pode se tornar melhor mas não sai pronto logo da instalação.

https://wiki.archlinux.org/title/.NET
Para fazer a instalação no arch é simples, basta instalar o programa já salvo na lista de pacotes do pacman:
```bash
sudo pacman -S dotnet-sdk
# acima ira instalar a versão mais recente do framework
# tambem é possivel selecionar uma versão especifica do dotnet:
# sudo pacman -S dotnet-sdk-6.0
```

https://github.com/dotnet/core
Repositório possui algumas informações extras sobre a instalação.
### Preparando VSCode

OK, vou estar utilizando o binário oficial da microsoft, simplesmente não estou a fim de baixar e instalar manualmente o servidor Omnisharp e outras funcionalidades só pra ficar com um monte de coisa espalhada depois. Vou instala-lo:

```bash
# é possivel só clonar o repositório e instalar manualmente com mkinstall -Si
git clone https://aur.archlinux.org/visual-studio-code-bin.git ./code
cd code
makepkg -Si
# compilamos o VScode e instalamos suas dependencias.
# pessoalmente prefiro ignorar essas estapas usando paru:
paru -S visual-studio-code-bin
# porem é preciso instalar paru.
```

O motivo de não usar o pacote ```code``` que o arch providencia é por que ele é uma versão que possui uma loja de extensões diferente do code original, isso é mais um problema de comunicação entre a microsoft e a comunidade linux mas independente o problema existe.

O motivo que preciso do code original é linha de extensões C#:

> ** .Net MAUI --> C# Dev Kit --> C# **

isso vai providenciar um ambiente que permite utilizar o dotnet pela barra de comandos do visual code E integração com MAUI para desenvolver tecnologias mobile (linux apenas android, mas windows para android e iOS)

Não esqueça de logar na sua conta microsoft.** para garantir que tudo funcione.
# Usando Dotnet

OK, assumindo que ja temos um editor de texto/IDE pronta, não importa se é visual code, KDevelop ou até o bloco de notas, precisamos aprender a usar o CLI do dotnet pelo terminal, a menos que essa função seja integrada com o editor.

para começar, digite ```dotnet --info``` no terminal linux, caso não apareça os dados do Framework, instale ou verifique sua pasta de binários.

para criar um projeto novo procure primeiro um template para usar, como o framework é grande existem multiplas saidas e começar do 0 normalmente é reservado para que já conhece ou sabe o que busca no .NET.

para buscar uma lista de todos os templates possiveis basta usar
```bash
dotnet new search <filtro>
dotnet new search mobile
dotnet new search desktop
dotnet new search web
# e então apenas crie o projeto:
dotnet new <nome_template>

```


