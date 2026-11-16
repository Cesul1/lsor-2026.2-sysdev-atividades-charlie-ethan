Aula 04: Acesso Remoto Seguro com OpenSSH e Redirecionamento de Portas no VirtualBox

Relatorio:
1) Charlie Ethan dos Santos Ugá Luna, 2024327037, 913-A, 09/11/2026

Atividade: Relatório Técnico

Cada aluno registra as evidências no seu repositório de entrega (lsor-2026.2-sysdev-atividades-<nomedoaluno>).
Onde incorporar na estrutura do repositório

lsor-2026.2-sysdev-atividades-<nomedoaluno>/
├── README.md               # Adicionar o link para atividade-aula4.md
├── atividade-aula1.md
├── atividade-aula2.md
├── atividade-aula3.md
├── atividade-aula4.md      # NOVO: Relatório Técnico da Aula 04
└── imagens/
    ├── aula4_ifconfig.png
    ├── aula4_route.png
    ├── aula4_traceroute.png
    ├── aula4_netstat_antes.png
    ├── aula4_regra_virtualbox.png
    ├── aula4_netstat_listening.png
    ├── aula4_ssh_login.png
    ├── aula4_netstat_established.png
    └── aula4_w_pts0.png

Regras:

    O relatório é o arquivo atividade-aula4.md na raiz do repositório.
    Capturas de tela em imagens/, nomeadas aula4_descricao.png (minúsculas, sem espaços ou acentos).
    Referencie com caminho relativo: ![netstat LISTENING](imagens/aula4_netstat_listening.png).
    Cada evidência deve ter o comando executado, a saída obtida e a imagem.
    Adicione ao README.md do repositório um link para atividade-aula4.md.

Evidências obrigatórias

    Linux Guest: ifconfig (IP 10.0.2.15 e MAC); route -n (gateway 10.0.2.2); traceroute 8.8.8.8.
    Windows Host (netstat -an | findstr 5222): ANTES (vazio); regra SSH no VirtualBox; DEPOIS (LISTENING); DURANTE a sessão (ESTABLISHED).
    Sessão SSH: terminal logado via ssh -p 5222 administrador@127.0.0.1; comando w mostrando pts/0.

Modelo de Relatório (7 Passos) para atividade-aula4.md

    Identificação: nome completo, matrícula, turma (Técnico em Desenvolvimento de Sistemas 2026.02), data e título da prática.
    Objetivo: diagnóstico de rotas, controle de portas com netstat e acesso remoto SSH em ambiente NAT.
    Ambiente: configurações do host Windows e da VM Ubuntu Server 26.04 LTS no VirtualBox (modo de rede, IPs, porta redirecionada).
    Procedimento: instalação de net-tools/traceroute, verificação do openssh-server, uso de route -n, w, ipconfig, netstat -an e configuração do NAT, em ordem.
    Testes e Evidências: capturas e saídas dos comandos no Linux e no Windows.
    Problemas e Soluções: ao menos um problema (ex.: conexão recusada, porta em uso, erro de parâmetro) e a correção.
    Conclusão: utilidade dos comandos de auditoria e importância de entender o fluxo de portas em redes virtualizadas.
