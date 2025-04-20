# RotaSmart

RotaSmart é um aplicativo Android desenvolvido para gerenciar viagens, permitindo o registro de despesas, abastecimentos, hospedagens, passeios, pedágios, manutenções e muito mais. O projeto utiliza Java como linguagem principal e SQLite para persistência de dados.

## Funcionalidades

- **Gerenciamento de Viagens**:

  - Criação, edição e exclusão de viagens.
  - Registro de informações como data de início, local de partida, destino final e quilometragem.

- **Registro de Despesas**:

  - Inserção de despesas gerais, abastecimentos, hospedagens, passeios, pedágios e manutenções.
  - Atualização e exclusão de registros.

- **Relatórios e Estatísticas**:

  - Geração de relatórios em PDF com detalhes das viagens e despesas.
  - Exibição de estatísticas, como porcentagens de tipos de hospedagem e qualidade de vias.

- **Persistência de Dados**:
  - Banco de dados SQLite para armazenamento local.
  - Tabelas específicas para cada tipo de entidade (viagem, despesa, abastecimento, etc.).

## Tecnologias Utilizadas

- **Linguagem**: Java
- **Banco de Dados**: SQLite
- **Frameworks e Bibliotecas**:
  - [iText](https://itextpdf.com/) para geração de PDFs.
  - Android SDK para desenvolvimento de aplicativos móveis.

## Estrutura de Dados

Entidades

- Viagem:
  Atributos: id, nome, dataDeInicio, dataDeTermino, localDePartida, DestinoFinal, kilometragemInicial, gastoTotal, etc.
  Relacionamentos: possui listas de Abastecimento, Alimentacao, Despesa, Diario, Estacionamento, Hospedagem, Manutencao, Passeio e Pedagio.

- Despesa:
  Atributos: id, data, descricao, valor, categoria, metodoPagamento, local, id_viagem.

- Abastecimento, Alimentacao, Hospedagem, Manutencao, Passeio, Pedagio:
  Herdam de Despesa e possuem atributos específicos.
  Banco de Dados
