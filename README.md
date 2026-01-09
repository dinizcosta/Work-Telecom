# Work-Telecom
Relatório de Desenvolvimento: App de Gestão de Produção Digi

Este projeto consiste no desenvolvimento de uma solução digital customizada para a gestão de produção diária de equipes de infraestrutura de rede de fibra ótica. Como chefe de equipe, identifiquei a necessidade de eliminar o uso de planilhas físicas e o retrabalho de preenchimento ao fim do dia.

O aplicativo permite o registro em tempo real de materiais, IDs de caixas (Enclosures) e observações técnicas diretamente do campo, com sincronização automatizada.
🛠️ Tecnologias Utilizadas
Banco de Dados: Google Sheets (Estrutura relacional)

Plataforma: AppSheet (Google Cloud)

Interface: Mobile (iOS/Android) com suporte Offline.

🚀 Implementação Passo a Passo (Início: 02/01/2026)
Fase de Modelagem: Estruturação do Google Sheets para receber dados de IDs de Enclosure, materiais (pigtails, abraçadeiras, etc.) e medições de sinal.

Configuração de UX: Criação de formulários intuitivos com funções de Scanner para QR Codes e Enum Lists para padronização de tipos de construção.

Lógica de Dados: Implementação de tipos numéricos e decimais para garantir a precisão dos registros de sinal (ex: -22.87 dB).

📈 Histórico de Versões (Changelog)
[v1.0.0] - 02/01/2026
Lançamento do MVP (Mínimo Produto Viável).

Funcionalidades básicas: Registro de materiais, observações de campo e IDs de caixas.

[v1.1.0] - 05/01/2026
Correção de Bugs: Ajuste no motor de atualização automática que causava o fechamento inesperado da aplicação (crash fix).

[v1.2.0] - 06/01/2026
Otimização de Fluxo: Remoção de tabelas e campos desnecessários que não competiam ao departamento, tornando a inserção de dados 30% mais ágil.

[v1.3.0] - 08/01/2026
Implementação de Dashboard: Adição de painel visual para consulta, edição e exclusão de itens cadastrados diretamente pelo app.
Ajuste de Tipagem: Correção de caracteres e validação de campos decimais para garantir compatibilidade com os relatórios de medição e outros calculos.


Autor: Diniz dos Santos Costa
Data: 03 de Janeiro de 2026

Tecnologias: Google Sheets, AppSheet, No-Code Development.
