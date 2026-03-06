# Instalação e Configuração do Android Studio para ambientes de aula

## Problema

  A IDE Android Studio utiliza diversas bibliotecas Java (SDKs) e emuladores de Android, por padrão, ao instalar ou iniciar o software ele busca tais dependencias
em um diretório padrão dentro das pastas de usuario. Este comportamento padrão em um laboratório de aulas onde cada aluno tem seu usuário faz com que toda vez que um
novo aluno use a máquina, a IDE faz o download novamente das dependências, fazendo com que a aula atrase e muitas vezes sobrecarregando a rede além de encher o disco das máquinas 
com diversos emuladores e dependencias iguais dentro das pastas de cada usuario.

## Solução:

Preparação Essencial para antes da Instalação

Crie a pasta "Android" em C:\\. Dentro dela, crie a pasta "Sdk".
Na pasta Sdk é onde ficarão os compiladores e emuladores de versões do Android.


Projetos: Para salvar projetos na máquina independente 
do usuário caso seja necessário. (Opcional)


<img width="665" height="231" alt="Android-Folder" src="https://github.com/user-attachments/assets/b60e687b-1059-47f0-a8ea-1b5b0d547ab1" />


<br/><br/><br/><br/>
Iniciando o Processo de Instalação: 

1. Executar o Instalador
Inicie o arquivo de instalação do Android Studio.
2. Seleção Customizada
Escolha a opção "custom" para personalizar.
<br/>
A opção "custom" permite configurar o SDK.

<img width="696" height="522" alt="Android-install-type" src="https://github.com/user-attachments/assets/245791ae-9b57-4261-9c27-ae8ba7a33c59" />


<br/><br/><br/><br/>

Android SDK Location:
1. Selecionar a pasta C:\Android\Sdk, onde serão baixadas as dependências, compiladores e emuladores.
2. Componentes
Marque todos os campos.
Garanta que todas as dependências sejam baixadas


<br/><br/>

<img width="709" height="544" alt="sdk-components" src="https://github.com/user-attachments/assets/4699e7e2-869f-4e18-a47a-951d2d65bd86" />


<br/><br/>

## Requisitos e Emuladores

Para que o Android Studio rode tranquilamente é recomendado 16GB de RAM, o Android Studio emula a versão escolhida do Android no projeto.


1. Emuladores:
Se pode baixar e configurar alguns emuladores para o aluno, dessa maneira já estarão prontos alguns emuladores que rodem tranquilamente ao nível do hardware da máquina.

2. Versão Android
Para configurar/instalar emuladores: na barra a esquerda clique em device manager -> + -> adicionar device -> selecionar um dispositivo e então escolher a versão do Android. Recomendado para máquinas mais fracas: 
selecionar Small Phone e Android 8.1
Emuladores leves melhoram o desempenho.


## Solução de Problemas Comuns

1. Driver do Emulador:

Em algumas máquinas a instalação do driver 
Android Emulator não ocorreu de forma 
automática, para resolver isso é necessário 
criar um device (como descrito na seção
anterior), então um aviso irá aparecer no 
topo da tela (como na imagem) clicar para 
instalar o driver.


2. Device Padrão:

Um device do Android 16 vem instalado por 
padrão, é recomendado dar um start nele, na 
barra a esquerda: Devices para checar se o 
drive Android Emulator está instalado, caso 
não uma tela irá aparecer perguntado se você 
quer instala-lo.
Verifique a instalação do driver. A tela perguntará se 
você quer instala-lo.




<img width="529" height="398" alt="driver-not-found" src="https://github.com/user-attachments/assets/25ba032c-93ae-4684-b44f-e4193339b910" />


## Configuração para o Aluno


Importante saber: quando um novo usuário abrir o Android Studio, irá 
para a mesma tela de instalação "Install type" onde o 
software pergunta se quer instalação "Padrão" ou "Customizada". 
Necessário repetir os passos, selecionando "Custom" e a pasta 
"C:\Android\Sdk", desta forma as configurações de usuário saberão 
onde buscar as dependências.
Por padrão cada usuário faz download dos emuladores e 
compiladores de forma individual apenas para seu usuário




















