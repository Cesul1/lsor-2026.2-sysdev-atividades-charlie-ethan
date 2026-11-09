Relatório (Modelo de 7 Passos)

Crie um README.md em seu repositório pessoal no GitHub com:

    1.Identificação: nome completo, matrícula, turma, data e título da prática.
    2.Objetivo: o que foi realizado.
    3.Ambiente: especificações da VM, modo de rede e endereços IP.
    4.Procedimento: comandos executados, em ordem.
    5.Testes: capturas de tela de ip addr, ip route e dos testes de ping; tabela comparativa NAT x Bridge (IP, gateway, host acessa a VM).
    6.Problemas e Soluções: ao menos um problema encontrado e como foi resolvido.
    7.Conclusão: o que foi validado e aprendido.

Critérios de Avaliação

    *Identificou corretamente IP, máscara, gateway e MAC.
    *Explicou por que o host não alcança 10.0.2.15 no modo NAT.
    *Executou os testes de ping em camadas e diagnosticou a camada de uma *falha.
    *Comparou NAT e Bridge com evidências.
    *Documentou no formato de 7 passos.

1. 
    a. ![IP addr, IP link e IP route identificados](/imagens/aula3/aula3_passo1-ip.png)
    b. ![Netplan status feito](/imagens/aula3/aula3_passo1-netplan-status.png)

    ![tabela](/imagens/aula3/aula3_passo1_tabela.png)

2. 
    a. ![Ping feito](/imagens/aula3/aula3_passo2-ping.png)
    b. ![Ping continuação](/imagens/aula3/aula3_passo2-ping2.png)

3. 
    a. ![sudo apt update](/imagens/aula3/aula3_passo3-apt-update.png)
    b. ![Intalação do tracerout](/imagens/aula3/aula3_passo3-traceroute-instalacao.png)
    c. ![Usando o traceroute](/imagens/aula3/aula3_passo3-uso-traceroute.png)

4. 
    a. ![Modo placa em ponte colocado](/imagens/aula3/aula3_passo4-placa-em-ponte.png)
    b. ![Ip-ping feito](/imagens/aula3/aula3_passo4-ip-ping.png)

    ![tabela](/imagens/aula3/aula3_passo4-tabela.png)

5. 
    a. ![powershell do windows](/imagens/aula3/aula3_passo5-powershell1.png)
    b. ![powershell do windows continuação](/imagens/aula3/aula3_passo5-powershell2.png)