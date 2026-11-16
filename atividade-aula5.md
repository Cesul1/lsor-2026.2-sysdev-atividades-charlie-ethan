Aula 05: Estrutura de Diretórios do Linux (FHS) e Pastas Departamentais com Permissões

Relatorio:
1) Charlie Ethan dos Santos Ugá Luna, 2024327037, 913-A, 09/11/2026

Atividade: Relatório Técnico
Cada aluno registra a prática no seu repositório de entrega (lsor-2026.2-sysdev-atividades-<nomedoaluno>), mantendo a mesma estrutura usada nas aulas anteriores.
6.1. Onde incorporar na estrutura do repositório

lsor-2026.2-sysdev-atividades-<nomedoaluno>/
├── README.md               # Adicionar o link para atividade-aula5.md
├── atividade-aula1.md
├── atividade-aula2.md
├── atividade-aula3.md
├── atividade-aula4.md
├── atividade-aula5.md      # NOVO: Relatório Técnico da Aula 05
└── imagens/
    ├── ... (imagens das aulas anteriores)
    ├── aula5_ls_raiz.png
    ├── aula5_bin_sbin.png
    ├── aula5_etc_pwd.png
    ├── aula5_auth_log.png
    ├── aula5_mkdir_ls_r.png
    ├── aula5_grupos_id.png
    ├── aula5_chown_chmod.png
    ├── aula5_arquivo_660.png
    ├── aula5_teste_a_fulano.png
    ├── aula5_teste_b_cicrano.png
    ├── aula5_teste_c_novato.png
    └── aula5_desafio_*.png

Regras (as mesmas das aulas anteriores):

    O relatório é o arquivo atividade-aula5.md, na raiz do repositório.
    As capturas de tela ficam em imagens/, nomeadas aula5_descricao.png (minúsculas, sem espaços nem acentos).
    Referencie as imagens com caminho relativo: ![Teste A](imagens/aula5_teste_a_fulano.png).
    Adicione ao README.md do repositório um link para atividade-aula5.md.

6.2. Como escrever cada evidência

O relatório não é um álbum de prints. Cada passo deve ser contado em três partes, sempre nesta ordem:

    Texto explicando o que você está fazendo e por quê, com suas palavras (ex.: "Agora vou dar ao grupo ti-group a posse da pasta para que só a equipe de TI consiga acessá-la").
    Bloco de código com os comandos exatamente como você digitou.
    Print da execução, mostrando o comando e a saída no terminal da sua VM. O prompt (administrador@ubuntu-server ou fulano@ubuntu-server) deve aparecer no print, para confirmar quem executou.

Depois do print, escreva uma ou duas frases interpretando o resultado (o que a saída mostra e se era o esperado).

Exemplo de como um passo deve ficar no atividade-aula5.md:

### Passo 4 — Donos e permissões das pastas

Neste passo eu transfiro a posse das pastas dos departamentos para o usuário
`administrador` e para o grupo de cada departamento. Em seguida, aplico a
permissão 770, para que só o dono e os membros do grupo possam entrar na pasta.

```bash
sudo chown -R administrador:ti-group /srv/ti-dept
sudo chown -R administrador:vendas-group /srv/vendas-dept
sudo chmod -R 770 /srv/ti-dept /srv/vendas-dept
ls -ld /srv/ti-dept /srv/vendas-dept
```

![Donos e permissões das pastas](imagens/aula5_chown_chmod.png)

A saída do `ls -ld` mostra `drwxrwx---`, com dono `administrador` e o grupo
de cada departamento. Ou seja, os outros usuários ficaram sem nenhum acesso,
como esperado.

6.3. Evidências obrigatórias

    Passo 1: ls na raiz; ls -ld /bin /sbin (links simbólicos); pwd e ls -F | head -n 15 em /etc; leitura do auth.log (ou journalctl).
    Passo 2: mkdir -p e a árvore mostrada por ls -R.
    Passo 3: criação dos grupos, usermod -aG e a saída de id fulano e id cicrano.
    Passo 4: ls -ld antes (dono root) e depois (drwxrwx---).
    Passo 5: arquivo com -rw-rw----.
    Testes A, B e C: acesso permitido para fulano e Permission denied para cicrano e novato.
    Desafio: todos os comandos e os testes com beltrano (permitido) e fulano (bloqueado).

6.4. Explique os comandos

Inclua no relatório uma tabela com cada comando usado nesta aula e o que ele faz, com suas palavras. Use a tabela abaixo como ponto de partida e complete a coluna da direita:
Comando 	O que significa / o que faz
cd /etc 	
pwd 	
ls -F, ls -R, ls -ld 	
sudo tail -n 10 /var/log/auth.log 	
mkdir -p 	
groupadd 	
usermod -aG 	
id 	
chown -R dono:grupo 	
chmod 770 / chmod 660 	
touch 	
su - x su 	
whoami 	
6.5. Modelo de Relatório (7 Passos) para atividade-aula5.md

    Identificação: nome completo, matrícula, turma (Técnico em Desenvolvimento de Sistemas 2026.02), data e título da prática.
    Objetivo: o que foi praticado (pastas do FHS, criação de diretórios com mkdir -p, grupos e permissões de pastas departamentais).
    Ambiente: VM ubuntu-server (Ubuntu Server 26.04 LTS, 768 MB de RAM, 1 CPU) no VirtualBox e usuários utilizados nos testes.
    Procedimento: os Passos 1 a 5, cada um com texto + bloco de código + print + interpretação, como no exemplo da seção 6.2.
    Testes: Testes A, B e C e o Desafio, no mesmo formato, e a tabela de comandos da seção 6.4.
    Problemas e Soluções: ao menos um problema encontrado (ex.: esquecer o sudo, usar su sem hífen, grupo que não "pegou" até um novo login) e como foi resolvido.
    Conclusão: por que separar pastas por grupo e usar permissões restritas é importante para a segurança de um servidor.
