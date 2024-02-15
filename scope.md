Sistema de listagem de gatos

Tipos de acesso:
    - Dono do sistema
    - Dono do gato
    - Cuidador de gatos

Escopo de acesso:
    - Dono do sistema:
        - Acesso a todos os cadastros (listagem dos donos dos gatos, dos cuidadores e de todos os gatos)
            -> CRUD com esses dados
        - Exclusão de qualquer um desses dados (APENAS SOFT DELETE)
    - Dono do gato:
        - Acesso aos seus gatos cadastrados
            -> CRUD com esses dados (soft delete tbm)
        - Designar o cuidador para cada gato
    - Cuidador:
        - Acesso aos gatos cadastrados com ele (apenas leitura de dados)
        - Acesso aos contatos do dono do gato cadastrado com ele

Dados de cada tipo de acesso:
    - Dono do sistema:
        - Login
        - Senha
    - Dono do gato:
        - Login
        - Senha
        - Nome
        - E-mail
        - Telefone
        - Gatos
    - Cuidador
        - Login
        - Senha
        - Nome
        - E-mail
        - Telefone
    - Gato
        - Nome
        - Raça
        - Dono
        - Cuidador
        - Foto
        - Obs importantes