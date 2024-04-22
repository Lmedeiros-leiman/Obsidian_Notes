
Após instalar o Arch Linux é possível que o sistema quebre, tanto faz o motivo: update quebrado, usuário cometendo um erro ou simplesmente raio espacial no momento certeiro. O que importa é ter uma ferramenta para poder restaurar e ter um backup do sistema.

Time Shift é uma ferramenta exclusiva para administradores de sistema, então o usuário comum terá que colocar a senha de administrador para usar.

Isso não é exclusividade do linux, um usuário responsável Windows também dirá a mesma coisa: sempre mantenha seus backups perto e sempre tenha mais de um.

O Time Shift irá criar um espelho do seu sistema operacional num momento do tempo e então você pode só copiar e colar para outras máquinas.

## Instalação do App

Para sistemas Linux sempre consulte seu gerenciador de pacotes, verifique se ele já não possui um pacote para instalar o Time Shift, no caso do Arch seria:
```sh
sudo pacman -S timeshift
```
Mas isso pode mudar conforme a sua distribuição.

Pior dos casos busque um repositório do aplicativo e compile e instale o mesmo do zero.
```sh 
git clone https://github.com/linuxmint/timeshift.git
cd timeshift
makepkg -si
```

## Utilizando

Após instalar o timeshift possui uma versão em terminal e uma versão em GUI.
O aplicativo irá questionar qual o tipo de backup o espelho devera ser, isso vai depender da formatação do disco e em alguns casos podera ser escolhida apenas uma das opções ou até mesmo ambas.
![[../Pasted image 20240422160252.png|Pasted image 20240422160252.png]]

Após selecionar ele irá calcular o disco, verificar arquivos e perguntar um local destino para os espelhos.
**O LOCAL QUE VOCÊ IRÁ GUARDAR DEVE POSSUIR UMA FORMATAÇÃO COMPATÍVEL COM LINUX!** então caso queira manter o velho HD guardando seus espelhos garanta que ele não esteja usando o sistema NFTS windows.

![[../Pasted image 20240422165921.png|Pasted image 20240422165921.png]]

Após isto o app fará perguntas simples como "quantos backups devo fazer? quantos devo fazer?".

Importante lembrar que ele irá perguntar se os arquivos da área de trabalho do usuário devem ser mantidos e o mesmo para a pasta raiz.

Após estas escolhas o programa começara a fazer backups de acordo com seu agendamento, caso queria fazer um backup apenas clique no botão Criar

![[../Pasted image 20240422170257.png|Pasted image 20240422170257.png]]


