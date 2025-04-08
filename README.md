# Título do Projeto: SaaS de Gestão Contábil  
**Nome do Estudante:** Luis Felipe Mondini  
**Curso:** Engenharia de Software  
**Data de Entrega:** [Data]

## 1. Resumo

Este documento propõe a criação de um SaaS voltado para a gestão financeira pessoal. O objetivo do projeto é fornecer uma solução eficaz para o gerenciamento de receitas, despesas e planejamento financeiro, com ênfase em análise preditiva. Isso permitirá ao usuário tomar decisões estratégicas baseadas em previsões assertivas. O texto detalha a motivação do projeto, seus requisitos funcionais e não funcionais, a estrutura planejada e as tecnologias empregadas em sua execução e monitoramento. Também aborda métodos e táticas para assegurar segurança e escalabilidade, além dos desafios e do plano de risco previstos para a execução. O projeto aplica conhecimentos adquiridos em engenharia de software, arquitetura de sistemas e desenvolvimento full stack com boas práticas de codificação.

## 2. Introdução

A gestão financeira é um desafio para muitas pessoas. Com o crescente volume de transações digitais, torna-se cada vez mais necessário organizar e controlar os gastos. Muitos usuários têm dificuldade para acompanhar receitas, despesas e gerenciar orçamentos, prevendo possíveis riscos. Com a popularização de soluções em nuvem, o modelo SaaS (Software as a Service) surge como uma excelente alternativa, permitindo o controle financeiro de qualquer dispositivo conectado à internet, com segurança e usabilidade.

Este projeto é relevante para a Engenharia de Software, pois envolve desenvolvimento full stack com práticas de segurança e escalabilidade, além do uso de modelos matemáticos preditivos via machine learning para melhorar a entrega de planejamento aos usuários. O propósito é desenvolver uma solução que facilite o gerenciamento financeiro por meio de uma plataforma intuitiva, segura, com boa arquitetura e uso de tecnologias modernas e em ascensão no mercado.

## 3. Descrição do Projeto

Muitas pessoas tomam decisões financeiras sem compreender o impacto futuro de seus gastos, o que leva frequentemente ao endividamento e à dificuldade de alcançar metas. Klapper et al. (2019) apontam que a ausência de planejamento estruturado conduz a escolhas impulsivas, comprometendo a estabilidade econômica.

O problema vai além da falta de controle: a dificuldade de transformar dados financeiros em projeções confiáveis é crítica. Métodos tradicionais, como planilhas e registros manuais, exigem disciplina, algo que nem sempre é viável no dia a dia.

Além disso, a fragmentação das informações financeiras dificulta uma visão unificada da saúde econômica. Muitos aplicativos exigem entrada manual constante e não consolidam os dados de forma eficiente, tornando o processo cansativo e pouco prático. A maioria das ferramentas também não considera padrões individuais de consumo ou variações de renda, limitando a personalização e impedindo que atuem como verdadeiros assistentes financeiros.

Outro obstáculo é a complexidade das informações apresentadas. Embora gráficos e tabelas sejam úteis, nem todos os usuários estão familiarizados com conceitos contábeis. Muitas ferramentas falham em transformar dados em *insights* acionáveis, dificultando a tomada de decisão e desmotivando o uso contínuo.

Por fim, segurança e privacidade são essenciais. Vazamentos ou acessos não autorizados comprometem informações sensíveis e a confiança do usuário. Garantir um ambiente seguro exige boas práticas de segurança digital, muitas vezes negligenciadas.

Apesar de buscar solucionar esses desafios, o projeto **não** abrangerá:
- Integração bancária automática, evitando riscos regulatórios;
- Funcionalidades voltadas a empresas ou contabilidade corporativa;
- Recomendações de investimento ou consultoria financeira.

O foco será exclusivo na gestão pessoal, com previsões e organização financeira sem atuar como assessor financeiro.

## 4. Especificação Técnica

### 4.1. Requisitos de Software

#### 4.1.1. Requisitos Funcionais

**Cadastro e Login de Usuário:**
- RF1: Cadastro de usuários;
- RF2: Autenticação com Google;
- RF3: Autenticação via JWT para sessões seguras;
- RF4: Edição e exclusão de conta;

**Gestão de Receitas e Despesas:**
- RF5: Registro detalhado de despesas (data, valor, categoria, descrição);
- RF6: Categorização de transações (ex: alimentação, transporte, lazer);
- RF7: Edição ou exclusão de transações;
- RF8: Visão geral do fluxo de caixa (receitas, despesas, saldo);
- RF9: Gráficos e relatórios mensais, trimestrais e anuais;
- RF10: Criação de categorias personalizadas;
- RF11: Histórico completo de transações com filtros;

**Planejamento Financeiro:**
- RF12: Definição de metas (ex: economizar valor, quitar dívida);
- RF13: Sugestões de planejamento com base nas movimentações;

**Análise Preditiva:**
- RF14: Previsões de fluxo de caixa com IA;
- RF15: Recomendações de ajustes baseadas em histórico de consumo;

**Alertas e Notificações:**
- RF16: Notificações sobre metas, despesas fora do padrão, contas a vencer;

#### 4.1.2. Requisitos Não-Funcionais

**Escalabilidade:**
- RNF1: Utilização do Google Cloud para escalar a aplicação;

**Desempenho:**
- RNF2: Consultas otimizadas no ORM do Django;

**Segurança:**
- RNF4: Criptografia de ponta a ponta;
- RNF5: Autenticação via JWT;
- RNF6: Proteção contra SQL Injection, XSS, CSRF;
- RNF7: Armazenamento de senhas com bcrypt;

**Usabilidade:**
- RNF8: Front-end responsivo em ReactJS com foco em acessibilidade e legibilidade;

**Monitoramento:**
- RNF9: Monitoramento e logs via Datadog;

**Compatibilidade:**
- RNF10: Compatibilidade com navegadores modernos (Chrome, Firefox, Edge, Safari);

**Manutenção e Desenvolvimento:**
- RNF11: Código bem documentado;
- RNF12: Testes unitários e de integração;

**Integração com IA:**
- RNF13: IA desenvolvida em Python com aprendizado contínuo;
- RNF14: Uso de machine learning para previsões financeiras;
- RNF15: Cálculos de IA devem ser eficientes para não comprometer o desempenho;

**Licenciamento e Conformidade:**
- RNF16: Conformidade com a LGPD;
- RNF17: Consentimento explícito e transparência no uso de dados;

**Representação dos Requisitos:**
- Diagrama de Casos de Uso (UML);

### 4.2. Considerações de Design

- Discussão das decisões de design e alternativas consideradas;
- Visão Inicial da Arquitetura: descrição dos componentes e suas interconexões;
- Padrões Utilizados: MVC, Microserviços;
- Modelos C4: níveis de Contexto, Contêineres, Componentes e Código;

### 4.3. Stack Tecnológica

#### 4.3.1. Linguagens

- Back-end: Django (Python) pela robustez, segurança, integração com bibliotecas de IA e construção eficiente de APIs;
- Front-end: ReactJS, devido à sua componentização, alta reutilização e integração fluida com APIs;

#### 4.3.2. Bibliotecas

- Pandas & Scikit-learn: manipulação de dados e criação de modelos preditivos;
- Prophet: previsão de séries temporais com sazonalidade;
- QuantLib: cálculos financeiros avançados;
- Plotly & Dash: dashboards interativos;
- Django Rest Framework: APIs escaláveis;

#### 4.3.3. Ferramentas de Desenvolvimento e Gestão

- SonarCloud: análise contínua de qualidade do código;
- Datadog: monitoramento em tempo real e alertas;
- Jira: organização e gestão ágil de tarefas;
- GitHub + GitHub Actions: versionamento, CI/CD automatizado;
- Docker: containerização da aplicação para consistência entre ambientes;

#### 4.3.4. Banco de Dados

- PostgreSQL: robustez, confiabilidade, suporte a transações ACID e consultas complexas;

### 4.4. Considerações de Segurança

- Análise das vulnerabilidades mais prováveis e estratégias para mitigação, com foco em segurança de dados, autenticação, criptografia e conformidade legal;

## 5. Próximos Passos

Planejamento das próximas etapas, incluindo cronograma para Portfólio I e II;

## 6. Referências

- https://www.treasy.com.br/blog/graficos-financeiros/  
- https://blog.nubank.com.br/planejamento-financeiro-pessoal/  
- https://wise.com/br/blog/planejamento-financeiro-com-ia  
- https://www.luiztools.com.br/post/12-dicas-para-construcao-de-um-bom-saas/  
- https://journalmediacritiques.com/index.php/jmc/article/view/85

## 7. Apêndices (Opcionais)

Informações complementares, dados ou discussões que extrapolem o corpo principal do texto;

## 8. Avaliações de Professores

- Considerações Professor(a):  
- Considerações Professor(a):  
- Considerações Professor(a):
