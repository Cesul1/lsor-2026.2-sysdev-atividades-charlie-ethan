Exercício Prático de Fixação

Para consolidar as competências adquiridas, cada aluno ou grupo deverá executar de forma autônoma a seguinte tarefa:

    1.Criar um novo grupo chamado financeiro.
    2.Associar os usuários cicrano e beltrano ao grupo financeiro (além do grupo devs ao qual já pertencem).
    3.Criar uma nova pasta compartilhada em /srv/financeiro.
    4.Definir as seguintes permissões de acesso:
        *O usuário administrador deve ter controle total.
        *O grupo financeiro deve ter acesso de leitura e escrita.
        *Os membros do grupo devs (como fulano) e o usuário novato não devem ter acesso a esta pasta financeira.
    5.Demonstrar em testes de terminal que cicrano consegue criar e alterar um relatório na pasta, enquanto fulano e novato recebem a mensagem Permission denied.


Respostas:

    1. ![financeiro criado](/imagens/aula2/aula2_grupo-financeiro.png)

    2. ![cicrano e beltrano associados](/imagens/aula2/aula2_acossiacao-cicrano-beltrano.png)

    3. ![/srv/financeiro criada](/imagens/aula2/aula2_pasta-srv-financeiro.png)

    4. ![permissões feitas](/imagens/aula2/aula2_permissoes-de-acesso.png)

    5. 
        a. ![teste do cicrano](/imagens/aula2/aula2_cicrano-teste.png)

        b. ![teste do fulano](/imagens/aula2/aula2_fulano-teste.png)

        c. ![teste do novato](/imagens/aula2/aula2_novato-teste.png)
