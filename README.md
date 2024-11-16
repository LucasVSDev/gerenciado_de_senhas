# Gerenciador de Senhas com Criptografia

Este projeto é um simples gerenciador de senhas que utiliza a biblioteca `Fernet` para criptografar e armazenar senhas de forma segura.

## Funcionalidades

1. **Salvar uma nova senha**: O programa permite salvar uma senha associada a um domínio específico. Ele utiliza uma chave de criptografia para proteger as informações.
2. **Recuperar uma senha existente**: Você pode consultar a senha associada a um domínio desde que forneça a chave correta.

## Requisitos

- Python 3.8 ou superior
- Bibliotecas adicionais listadas no arquivo `requirements.txt` (se aplicável)

## Instalação

1. Clone este repositório:
    ```bash
    git clone https://github.com/LucasVSDev/gerenciado_de_senhas.git
    ```
2. Navegue para o diretório do projeto:
    ```bash
    cd gerenciado_de_senhas
    ```
3. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

## Uso

1. Execute o script principal:
    ```bash
    python templates/template.py
    ```
2. Escolha uma das opções:
   - **1**: Para salvar uma nova senha.
   - **2**: Para visualizar uma senha existente.

### Instruções Detalhadas

#### Salvando uma nova senha
- Na primeira execução, uma chave de criptografia será gerada automaticamente. Certifique-se de armazená-la com segurança, pois será necessária para acessar as senhas no futuro.
- Insira o domínio e a senha que deseja salvar.
- As informações serão criptografadas e armazenadas.

#### Recuperando uma senha existente
- Forneça o domínio e a chave de criptografia usada para salvar a senha.
- O programa descriptografará e exibirá a senha correspondente, se encontrada.

## Avisos Importantes

- **Segurança da Chave**: A chave de criptografia é essencial para acessar suas senhas. Caso a perca, não será possível recuperar os dados.
- **Gerenciamento do Arquivo de Chave**: Após gerar a chave, remova o arquivo gerado ou transfira-o para um local seguro.

## Estrutura do Projeto

```plaintext
├── model
│   └── password.py             # Módulo para manipulação de senhas
├── templates                   
│   └── template.py             # Arquivo principal para execução do programa
├── views
│   └── password_views.py       # Módulo para criptografia com Fernet
├── db                          # Diretório de armazenamento dos dados
├── Keys                        # Diretório para armazenar as chaves de criptografia
├── __init__.py                 # Arquivo de inicialização
└── README.md                   

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues para sugestões ou relatórios de bugs, e envie um pull request para melhorias.

