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
        - Data de cadastro
        - Data de desativação
    - Cuidador
        - Login
        - Senha
        - Nome
        - E-mail
        - Telefone
        - Data de cadastro
        - Data de desativação
    - Gato
        - Nome
        - Raça
        - Dono
        - Cuidador
        - Foto
        - Obs importantes
        - Data de cadastro
        - Data de desativação

Interações importantes:
    - Se o dono do gato for desativado, o cadastro do gato também deve ser desativado
    - Se o Cuidador for desativado, então o gato deve ter a exclusão do cuidador do seu cadastro
    - Se houver um gato sem cuidador cadastrado, o Dono do gato não pode realizar nenhuma ação no sistema
    - E-mail e telefone devem ser únicos