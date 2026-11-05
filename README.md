O que este script faz?
Este script automatiza a integração entre o Python (executado no Google Colab) e o Google Sheets. O objetivo principal é gerar uma base de dados fictícia de pacientes para fins de teste ou análise de dados e enviá-la diretamente para uma planilha na nuvem.

⚙️ Passo a Passo do Funcionamento:
Instalação e Configuração de Dependências:

Instala as bibliotecas gspread (para manipulação e integração com o Google Sheets) e Faker (para geração de dados fictícios realistas).

Autenticação Segura:

Acessa as credenciais de uma Conta de Serviço (Service Account) salvas de forma segura nos Secrets do Google Colab e realiza a autenticação na API do Google.

Conexão e Preparação da Planilha:

Conecta a uma planilha específica do Google Sheets utilizando o seu ID.

Acessa a primeira aba da planilha e a renomeia para pacientes.

Cria o cabeçalho da tabela inserindo as colunas necessárias na primeira linha (ID, Nome, Data de Nascimento, Sexo, Bairro e Tipo de Convênio).

Geração de Dados Fictícios:

Configura a biblioteca Faker para o padrão brasileiro (pt_BR) e define uma semente (seed) para garantir que os dados gerados sejam reproduzíveis em testes futuros.

Cria um laço de repetição (loop) que gera 10 registros automáticos contendo CPFs, nomes, datas, gêneros, bairros e tipos de convênio (SUS, particular ou convênio) selecionados aleatoriamente.

Envio e Validação dos Dados:

Envia todas as linhas geradas de uma só vez para o Google Sheets (inserção em lote).

Realiza uma leitura final da aba para confirmar se as linhas e o cabeçalho foram gravados corretamente e exibe uma amostra no console.
