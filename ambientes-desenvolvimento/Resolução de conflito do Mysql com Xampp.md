# Conflito de Porta entre XAMPP e MySQL Workbench

## Problema

Ao iniciar o MySQL no XAMPP, o serviço falha ou não inicia porque a porta 3306 já está sendo utilizada pelo MySQL Workbench.


<img width="654" height="424" alt="xamp-mysql" src="https://github.com/user-attachments/assets/079738a4-26a7-4653-acf0-4ea31458f1df" />


## Causa

Para verificar qual serviço está usando a porta padrão:

<code> netstat -ano | findstr 3306 </code>

O MySQL Server instalado separadamente estava rodando como serviço do Windows e ocupando a porta padrão do MySQL (3306).


## Solução

Alterar a pota padrão do mysql embutido no XAMPP:

Dentro do painel do XAMPP, na linha do Mysql clique em Config e então em my.ini.
Vai abrir um bloco de notas, mudar a porta padrão de 3306 para 3307, 
ATENÇÃO: necessário mudar a porta em duas linhas diferentes do arquivo


<img width="546" height="664" alt="new-port" src="https://github.com/user-attachments/assets/3dd09c2b-aa0f-451c-94bf-c8f338dd52c1" />


Próximo passo, existe um segundo arquivo para configurar, vá para a pasta
c:\xampp\phpMyAdmin\config.inc -> abrir com bloco de notas, aqui é necessário 
adicionar uma linha de código:

<code> $cfg['Servers'][$i]['port'] = 3307 </code>

<img width="665" height="373" alt="php" src="https://github.com/user-attachments/assets/b9cffde5-6c1a-40af-a7a7-75a272c8ab9f" />


Após esta configurações o mysql do xamp deve iniciar normalmente, ficando verdinho no painel do xampp e mostrando a porta 3307:


<img width="630" height="397" alt="funcionou" src="https://github.com/user-attachments/assets/f8e53277-4c5c-4170-8256-95436c114d65" />








