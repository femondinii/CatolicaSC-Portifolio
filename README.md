# Título do Projeto: SaaS de Gestão Contábil  
**Nome do Estudante:** Luis Felipe Mondini  
**Curso:** Engenharia de Software  
**Data de Entrega:** [Data]

## 1. Resumo

Este projeto propõe a criação de um SaaS voltado para a gestão financeira pessoal. A proposta visa oferecer aos usuários uma ferramenta prática e acessível para controle de receitas, despesas e planejamento financeiro, com o apoio de recursos preditivos baseados em machine learning. A solução incorpora práticas de engenharia de software, arquitetura escalável, segurança da informação e usabilidade, promovendo uma experiência confiável e personalizada. Além disso, aborda os desafios técnicos enfrentados, os métodos adotados para mitigação de riscos e as tecnologias aplicadas ao longo do projeto.

## 2. Introdução

Com o crescimento das transações digitais e a complexidade crescente na gestão das finanças pessoais, torna-se cada vez mais necessário o uso de soluções tecnológicas que auxiliem o usuário a manter o controle financeiro e tomar decisões estratégicas. No entanto, ferramentas tradicionais, como planilhas e aplicativos genéricos, frequentemente exigem esforço contínuo e carecem de personalização. A falta de previsibilidade e dificuldade na interpretação de dados financeiros prejudica a tomada de decisões conscientes e a adesão ao uso dessas ferramentas.

Nesse contexto, uma aplicação SaaS (Software como Serviço) oferece uma alternativa escalável e segura, permitindo acesso multiplataforma e centralização das informações financeiras. O projeto se destaca por aplicar conceitos da engenharia de software moderna, desenvolvimento full stack, modelagem preditiva e boas práticas de arquitetura para entregar uma plataforma intuitiva, com foco em acessibilidade, segurança e análise inteligente dos dados com machine learning.

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
- RNF3: Criptografia de ponta a ponta;
- RNF4: Autenticação via JWT;
- RNF5: Proteção contra SQL Injection, XSS, CSRF;
- RNF6: Armazenamento de senhas com bcrypt;

**Usabilidade:**
- RNF7: Front-end responsivo em ReactJS com foco em acessibilidade e legibilidade;

**Monitoramento:**
- RNF8: Monitoramento e logs via Datadog;

**Compatibilidade:**
- RNF9: Compatibilidade com navegadores modernos (Chrome, Firefox, Edge, Safari);

**Manutenção e Desenvolvimento:**
- RNF10: Código bem documentado;
- RNF11: Testes unitários e de integração;

**Integração com IA:**
- RNF12: IA desenvolvida em Python com aprendizado contínuo;
- RNF13: Uso de machine learning para previsões financeiras;
- RNF14: Cálculos de IA devem ser eficientes para não comprometer o desempenho;

**Licenciamento e Conformidade:**
- RNF15: Conformidade com a LGPD;
- RNF16: Consentimento explícito e transparência no uso de dados;

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
