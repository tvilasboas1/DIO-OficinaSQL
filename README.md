🛠️ Modelo Conceitual para Oficina Mecânica
📝 Descrição do Projeto
Este repositório contém o esquema conceitual completo para um sistema de gerenciamento de oficina mecânica, desenvolvido a partir da narrativa fornecida. O modelo abrange todas as entidades necessárias para controle de ordens de serviço, clientes, veículos, equipes mecânicas e peças.

🔍 Contexto do Modelo
Narrativa Implementada:
Controle completo de ordens de serviço (OS)

Gestão de clientes e seus veículos

Alocação de equipes mecânicas por especialidade

Cálculo automático de valores (mão-de-obra + peças)

Rastreamento do status das OS

Decisões de Design Adicionais:
Tabela de Histórico: Adicionei um sistema de histórico para rastrear alterações nas OS

Classificação de Serviços: Categorizei serviços por complexidade

Estoque de Peças: Implementei controle de estoque além do requisito original

Sistema de Avaliações: Adicionei entidade para feedback dos clientes

🗃️ Entidades Principais
Entidade	Descrição
Cliente	Dados pessoais e de contato
Veículo	Informações técnicas e histórico
OrdemServico	OS com valor, status e datas
EquipeMecanicos	Grupos por especialidade
Mecanico	Profissionais com códigos e especialidades
Servico	Catálogo de serviços com valores
Peca	Peças com estoque e valores
📊 Diagrama do Modelo
Diagrama Conceitual da Oficina

🛠️ Estrutura do Repositório
Copy
oficina-mecanica-model/
├── docs/
│   ├── DECISIONS.md       # Justificativas de design
│   └── REQUIREMENTS.md    # Narrativa completa
├── scripts/
│   ├── schema.sql         # Script completo de criação
│   └── dummy_data.sql     # Dados de exemplo
├── assets/
│   ├── diagrama_er.png    # Versão compactada
│   └── diagrama_er.pdf    # Versão para impressão
└── examples/
    ├── queries.sql        # Consultas úteis
    └── reports.sql        # Relatórios gerenciais
▶ Como Utilizar
Execute o script principal:

bash
Copy
mysql -u usuario -p < scripts/schema.sql
Para carregar dados de exemplo:

bash
Copy
mysql -u usuario -p oficina_db < scripts/dummy_data.sql
🔄 Fluxo do Sistema
mermaid
Copy
graph TD
    A[Cliente] -->|Leva| B[Veículo]
    B --> C[Ordem de Serviço]
    C --> D[Equipe Mecânica]
    D --> E[Serviços]
    E --> F[Peças]
    F --> G[Cálculo Total]
    G --> H[OS Finalizada]
🏆 Funcionalidades Implementadas
Cálculo automático de valor da OS

Controle de status das ordens de serviço

Vinculação veículo-cliente

Alocação por especialidade mecânica

Sistema de histórico de alterações

Controle de estoque de peças

🤝 Como Contribuir
Faça um fork do projeto

Crie sua branch (git checkout -b feature/improvement)

Commit suas mudanças (git commit -m 'Add some feature')

Push para a branch (git push origin feature/improvement)

Abra um Pull Request

📄 Licença
Este projeto está licenciado sob a MIT License.
