# Work-Telecom
Relatório de Desenvolvimento: App de Gestão de Produção Digi
1. Visão Geral
Este projeto consiste no desenvolvimento de uma solução digital customizada para a gestão de produção diária de equipes de infraestrutura de rede (Telecom).
O objetivo principal foi substituir o preenchimento manual de planilhas físicas por um aplicativo móvel que permite o registro simultâneo de dados em campo e a geração automatizada de relatórios.

3. O Problema
A equipe utilizava planilhas impressas para registrar:
Dados técnicos (Fusões, Splitters, IDs de Enclosure).
Consumo de materiais (Abraçadeiras, Pigtails).
Resultados de ensaios de sinal.

Desafios identificados:
Atraso na sincronização de dados entre o campo e o escritório.
Riscos de erros de transcrição manual.
Dificuldade na padronização de observações técnicas.

3. Arquitetura da Solução
A solução foi construída utilizando uma arquitetura de No-Code, focada em agilidade e eficiência operacional.
Banco de Dados: Google Sheets (Estrutura de tabelas relacionais).
Plataforma de Desenvolvimento: AppSheet (Google Cloud).
Interface: Aplicativo Híbrido (iOS/Android) com suporte a modo offline.

4. Passo a Passo da Implementação Detalhada
Fase 1: Modelagem de Dados
A estrutura da planilha foi normalizada para garantir a integridade dos dados. As colunas foram definidas conforme os requisitos técnicos da DIGI:
ID Encl.: Chave primária de identificação do elemento.
Fusões: Campo numérico para controle de emendas.
Ensaios (OBS.): Campo de texto longo para registros de sinal (ex: -22.87/-5.03).
Material Consumível: Campos quantitativos para controle de estoque.

Fase 2: Desenvolvimento do Aplicativo (AppSheet)
Conexão de Dados: Importação da planilha e regeneração da estrutura para reconhecimento de tipos.
Configuração de UX (User Experience):
Criação de visualizações do tipo Form (Formulário) para entrada de dados.
Implementação de visualização Table (Tabela) para consulta de histórico.
Lógica e Inteligência:
Scanner: Ativação da função Scannable na coluna ID Encl., permitindo o uso da câmera para leitura de QR Codes/Barcodes.
Enum Lists: Criação de menus suspensos (Dropdowns) para campos fixos (Ex: TIP PDO Construção), eliminando erros de digitação.
Data Types: Configuração de tipos Number e Decimal para garantir que apenas dados válidos sejam inseridos.

Fase 3: Automação e Relatórios
Sincronização: Configuração de sincronização em tempo real (Cloud Sync).
Geração de Relatório: O sistema foi desenhado para que cada entrada no aplicativo gere automaticamente uma nova linha na planilha mestra, que serve como base para a "Folha de Produção Diária".

5. Diferenciais Técnicos
Inovação Interna: Primeiro projeto de autoria própria da equipe focado em desempenho operacional.

Agilidade: Redução do tempo entre a execução do serviço e o fechamento do relatório diário.

Escalabilidade: A estrutura permite a adição de novos campos (como localização GPS e fotos) sem necessidade de reprogramação complexa.

Como usar este repositório
O arquivo Planilha_Base.xlsx contém a estrutura de colunas necessária.

Importe para o seu Google Drive.

Abra o AppSheet e aponte para esta planilha para replicar a solução.

Autor: Diniz dos Santos Costa
Data: 03 de Janeiro de 2026

Tecnologias: Google Sheets, AppSheet, No-Code Development.
