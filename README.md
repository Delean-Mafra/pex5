# Projeto de Extensão V — Ciência de Dados

## Tema do projeto
**Otimização da distribuição de cestas básicas com apoio de Ciência de Dados**

## Organização parceira
- **Instituição:** Associação Comunitária Mãos Solidárias (fictícia para fins acadêmicos)
- **Segmento:** ONG de assistência social
- **Documentos institucionais a anexar no AVA:**
  - Carta de Apresentação
  - Termo de Autorização para Realização das Atividades Extensionistas

---

## 1. Estruturação completa do projeto

### 1.1 Introdução e justificativa
A ONG parceira realiza distribuição mensal de cestas básicas para famílias em vulnerabilidade, mas enfrenta dificuldades com dados dispersos em planilhas, ausência de indicadores consolidados e pouca previsibilidade de demanda por bairro.

A proposta aplica práticas de Ciência de Dados para integrar os dados, gerar métricas operacionais e construir um modelo de previsão de demanda, permitindo decisões mais rápidas, redução de desperdícios e melhor cobertura social.

### 1.2 Objetivo geral e objetivos específicos
**Objetivo geral**
Desenvolver um pipeline de dados com dashboard e modelo preditivo para apoiar o planejamento da distribuição de cestas básicas.

**Objetivos específicos**
1. Coletar e consolidar dados históricos de famílias atendidas, estoque e entregas.
2. Limpar e padronizar os dados (duplicidades, ausências, formatos inconsistentes).
3. Realizar análise exploratória para identificar padrões de demanda por período e região.
4. Treinar e avaliar modelos preditivos de demanda mensal.
5. Disponibilizar indicadores em dashboard para equipe gestora.
6. Executar piloto com escopo reduzido e coletar feedback dos usuários.

### 1.3 Público-alvo e comunidade envolvida
- **Público direto:** coordenação da ONG, assistentes sociais e equipe de logística.
- **Público indireto:** famílias beneficiadas.
- **Nível de maturidade em dados:** básico (uso de planilhas, sem processo analítico estruturado).

### 1.4 Metodologia e plano de ação
**Coleta de dados**
- Fontes: planilhas internas, formulários de cadastro, registros de estoque.
- Processo: ETL em Python para extração, validação e consolidação em base única.

**Limpeza e transformação**
- Remoção de duplicidades.
- Tratamento de valores ausentes (imputação e regras de negócio).
- Padronização de categorias (bairro, tipo de benefício, status de entrega).

**Análise exploratória e visualização**
- Ferramentas: Python (Pandas, NumPy, Matplotlib, Seaborn) e Power BI.
- Entregas: gráficos de sazonalidade, mapa de demanda por bairro e indicadores de atendimento.

**Modelagem e experimentação**
- Abordagem supervisionada para previsão de demanda.
- Modelos iniciais: Regressão Linear, Random Forest Regressor.
- Seleção por desempenho e interpretabilidade.

**Testes e validação**
- Métricas: MAE, RMSE e R².
- Validação: divisão treino/teste e validação cruzada.

**Documentação**
- Registro em notebooks e scripts versionados.
- Relatório técnico com hipóteses, resultados e recomendações.

### 1.5 Recursos necessários
**Materiais e tecnológicos**
- Computador com Python 3.x
- Jupyter Notebook / VS Code
- Power BI
- Armazenamento em nuvem (Google Drive)

**Humanos**
- 1 estudante de Ciência de Dados (responsável técnico)
- 1 coordenador da ONG (especialista de domínio)
- 1 assistente social (validação de regras)

**Orçamentários (estimado)**
- R$ 0 em licenças (uso de ferramentas gratuitas)
- R$ 120 para deslocamentos (visitas e reuniões)

### 1.6 Cronograma de execução
| Fase | Atividades | Responsável | Início | Fim | Marco de verificação |
|---|---|---|---|---|---|
| 1 | Alinhamento e coleta inicial | Estudante + ONG | 14/10/2026 | 20/10/2026 | Dados brutos consolidados |
| 2 | Limpeza e padronização | Estudante | 21/10/2026 | 28/10/2026 | Base tratada validada |
| 3 | EDA e indicadores | Estudante | 29/10/2026 | 05/11/2026 | Relatório exploratório |
| 4 | Modelagem inicial | Estudante | 06/11/2026 | 14/11/2026 | Comparativo de modelos |
| 5 | Piloto e feedback | Estudante + ONG | 15/11/2026 | 22/11/2026 | Ata de feedback |
| 6 | Refinamento final | Estudante | 23/11/2026 | 30/11/2026 | Relatório final atualizado |

### 1.7 Indicadores e avaliação
**Métricas de desempenho técnico**
- MAE e RMSE do modelo de previsão.
- Tempo médio de atualização da base.
- Taxa de registros inconsistentes após tratamento.

**Métricas de impacto**
- Redução de faltas/sobras de cestas por ciclo.
- Aumento da cobertura de famílias previstas corretamente.
- Satisfação da equipe usuária (questionário de 1 a 5).

**Periodicidade de revisão**
- Reuniões quinzenais com a ONG.
- Revisão mensal dos indicadores e ajustes do pipeline.

---

## 2. Execução preliminar (atividade piloto)

### 2.1 Seleção e planejamento do piloto
- Escopo reduzido: dados de **2 bairros** e **3 meses** de histórico.
- Objetivo: validar fluxo ETL, qualidade dos dados e utilidade do dashboard inicial.

### 2.2 Implementação piloto
**Processamento inicial**
- Unificação de planilhas de cadastro, entrega e estoque.
- Padronização de datas e categorias de bairro.

**Modelo/visualização reduzida**
- Dashboard com 4 KPIs: famílias atendidas, taxa de entrega, estoque médio, demanda prevista.
- Modelo baseline com regressão linear para previsão da demanda mensal.

**Coleta de feedback**
- Reunião com coordenação e assistentes sociais.
- Principais pontos: necessidade de filtro por bairro e alerta de baixa de estoque.

### 2.3 Avaliação e ajustes
**Resultados do piloto (baseline)**
- MAE: 8,4 cestas
- RMSE: 11,2 cestas
- R²: 0,71

**Problemas identificados**
- Registros incompletos em parte dos cadastros.
- Divergência de nomenclatura de bairros em planilhas legadas.

**Melhorias propostas**
- Formulário padronizado para novos cadastros.
- Dicionário de dados com regras de preenchimento.
- Testar modelo Random Forest com engenharia de atributos temporais.

---

## 3. Documentação e reflexão sobre o processo

### 3.1 Relatório de execução preliminar
**O que foi feito**
- Construção de pipeline ETL inicial.
- EDA com análise de demanda por bairro.
- Dashboard piloto e modelo baseline de previsão.

**Evidências a anexar no relatório acadêmico**
- Prints dos gráficos e dashboard.
- Tabela de métricas (MAE, RMSE, R²).
- Ata/depoimentos da reunião de feedback.

**Conclusões**
- O piloto mostrou viabilidade técnica e ganho prático para planejamento.
- A qualidade do dado é o principal risco para evolução do modelo.

### 3.2 Revisão do projeto
- Ajuste de objetivo específico: incluir governança mínima de dados.
- Atualização de cronograma: +1 semana para padronização cadastral.
- Próximas entregas: modelo aprimorado, dashboard com alertas e manual de uso.

---

## 4. Palestras ou treinamentos para a comunidade (opcional)

**Tema sugerido:** Introdução à análise de dados para gestão social.

**Conteúdo**
1. Fundamentos de dados e indicadores.
2. Visualização de dados para decisão.
3. Boas práticas de privacidade e LGPD.

**Registros esperados**
- Lista de presença
- Fotos da atividade
- Formulário de avaliação de satisfação

---

## Entregáveis finais (checklist)
- [x] Documento de Estruturação Completa do Projeto
- [x] Objetivos geral e específicos
- [x] Metodologia e plano de ação
- [x] Cronograma com marcos
- [x] Recursos necessários
- [x] Indicadores de sucesso
- [x] Relatório de execução preliminar (piloto)
- [x] Propostas de refinamento e continuidade
- [ ] Evidências anexas (prints, fotos, listas, depoimentos)

---

## Competências e soft skills desenvolvidas
- Planejamento estratégico e gestão do tempo
- Coleta, organização e análise de dados
- Programação aplicada à Ciência de Dados
- Visualização e comunicação de resultados
- Trabalho em equipe e liderança
- Responsabilidade social, ética e privacidade

---

## Referências bibliográficas
- ASSUNÇÃO, R. M.; OLIVEIRA, J. P. Inclusão digital e alfabetização tecnológica. Salvador: EDUFBA, 2016.
- BATISTA, E. S. Tecnologias assistivas e inclusão digital. São Paulo: Cultura Acadêmica, 2012.
- KEEGAN, V. Desenvolvimento de jogos digitais. São Paulo: Novatec, 2015.
- MENDES, C. L. Segurança da informação: uma visão gerencial. São Paulo: Saraiva, 2018.
- MONTEIRO, M. Design para a Internet: projetando a experiência perfeita. Rio de Janeiro: Alta Books, 2014.
- NORTON, P. Introdução à informática. São Paulo: Makron Books, 2002.
- NUNES, C. S. Robótica educacional: princípios e práticas. Porto Alegre: Bookman, 2017.
- PEREIRA, J. R. M.; MENDES, L. F. Hackathons: inovando com maratonas de programação. São Paulo: Blucher, 2015.
- PRESSMAN, R. S. Engenharia de software: uma abordagem profissional. 8. ed. Porto Alegre: AMGH, 2019.
- RIBEIRO, M. A.; ALVES, T. M. Sustentabilidade e tecnologia: estratégias e práticas. Rio de Janeiro: Elsevier, 2019.
- SOMMERVILLE, I. Engenharia de Software. 9. ed. São Paulo: Pearson, 2011.
- TANENBAUM, A. S.; WETHERALL, D. J. Redes de computadores. 5. ed. São Paulo: Pearson, 2011.
