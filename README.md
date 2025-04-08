## Título do Projeto: SaaS de Gestão contábil

**Nome do Estudante:** Luis Felipe Mondini  
**Curso:** Engenharia de Software  
**Data de Entrega:** [Data]

---

## Resumo

Este documento propõe a criação de um SaaS voltado para a gestão financeira pessoal. O objetivo do projeto é fornecer uma solução eficaz para o gerenciamento de receitas, despesas e planejamento financeiro, com ênfase em análise preditiva, possibilitando que o usuário faça escolhas estratégicas baseadas em previsões assertivas. O texto detalha o motivo do projeto, seus requisitos funcionais e não funcionais, a estrutura planejada e as tecnologias empregadas para a sua execução e monitoramento. Trata de métodos e táticas para assegurar segurança e escalabilidade, bem como os desafios e o plano de risco esperado durante a execução. Aplicará os conhecimentos obtidos em engenharia de software, arquitetura de sistemas, desenvolvimento completo com boas práticas de codificação.

---

## 1. Introdução

A gestão financeira é um desafio para muitas pessoas, especialmente diante do crescente volume de transações digitais. A necessidade de organizar e controlar esses gastos fica cada vez mais evidente. Muitos usuários enfrentam dificuldades para acompanhar suas receitas, despesas e gerenciar os orçamentos prevendo possíveis riscos. Com a popularização de soluções hospedadas em nuvem, o modelo SaaS (Software as a Service) surge como uma excelente alternativa para o gerenciamento financeiro, permitindo que os usuários tenham controle de suas finanças de qualquer dispositivo conectado à internet, garantindo segurança e usabilidade.  

Esse projeto é relevante para Engenharia de Software, pois abrange conceitos de desenvolvimento full stack de sistemas, com práticas de segurança e escalabilidade, além do uso de modelos matemáticos preditivos através de machine learning para melhor experiência de entrega de planejamento aos usuários. O propósito deste projeto é desenvolver uma solução que facilite o gerenciamento financeiro por meio de uma plataforma intuitiva e segura, com uma boa arquitetura e uso de tecnologias em crescente no mercado.  

---

## 2. Descrição do Projeto

Muitos indivíduos tomam decisões financeiras sem um entendimento claro do impacto futuro de seus gastos, o que frequentemente resulta em endividamento e dificuldades para atingir metas financeiras. De acordo com Klapper et al. (2019), a ausência de planejamento estruturado leva a escolhas impulsivas e compromete a estabilidade econômica pessoal. O problema não está apenas na falta de controle, mas também na dificuldade de transformar dados financeiros em projeções confiáveis. Métodos tradicionais, como planilhas e registros manuais, exigem um nível de disciplina que nem sempre é realista no cotidiano dos usuários.

Além disso, a fragmentação das informações financeiras dificulta uma visão unificada da saúde econômica do usuário. Aplicativos existentes geralmente demandam entrada manual constante e não oferecem uma forma eficiente de consolidar dados automaticamente. Esse processo pode se tornar cansativo e pouco prático, levando muitos a abandonarem o acompanhamento financeiro. A situação se agrava pelo fato de que a maioria das ferramentas do mercado não considera padrões individuais de consumo e variações de renda, tratando todos os usuários com a mesma abordagem generalista. Isso limita o potencial de personalização e impede que a tecnologia atue como um verdadeiro assistente financeiro adaptado à realidade de cada pessoa.

Outro obstáculo significativo é a complexidade das informações financeiras apresentadas. Embora gráficos e tabelas sejam recursos valiosos, nem todos os usuários possuem familiaridade com conceitos contábeis e econômicos. Muitas ferramentas falham ao traduzir essas informações em insights acionáveis, tornando difícil para o usuário compreender o que precisa ser ajustado e quais medidas tomar para melhorar sua saúde financeira. A barreira na interpretação dos dados faz com que muitos desistam do planejamento antes mesmo de alcançar benefícios concretos.

Por fim, a segurança e privacidade dos dados são preocupações fundamentais para qualquer sistema que lida com informações financeiras. Vazamentos de dados ou acessos não autorizados podem comprometer não apenas informações sensíveis, mas também a confiança do usuário na plataforma. Garantir um ambiente seguro e confiável exige boas práticas de segurança digital, algo que nem todas as soluções de gestão financeira priorizam adequadamente.

Apesar de buscar resolver esses desafios, o projeto não abordará alguns aspectos específicos. A ferramenta não terá integração bancária automática, evitando riscos regulatórios e garantindo maior segurança ao usuário. O foco será na gestão financeira pessoal, sem funcionalidades voltadas para empresas ou contabilidade corporativa. Além disso, o sistema não oferecerá recomendações de investimentos ou consultoria financeira, limitando-se a fornecer uma visão organizada e preditiva das finanças do usuário, sem atuar como um assessor financeiro.

---

## 3. Especificação Técnica

### 3.1 Requisitos de Software

#### 3.1.1 Requisitos Funcionais

- Cadastro e Login de usuário:
  - RF1: Deve realizar cadastro de usuários;
  - RF2: Deve realizar autenticação com o Google;
  - RF3: Implementação de autenticação JWT para sessões mais seguras;
  - RF4: Deve permitir a alteração dos dados da conta e exclusão da mesma;

- Gestão de receitas e despesas:
  - RF5: Poderá registrar despesas de maneira detalhada (data, valor, categoria, descrição);
  - RF6: Deve categorizar transações pelo tipo (Ex: alimentação, transporte, lazer, outros);
  - RF7: Permitir editar ou excluir transações registradas;
  - RF8: Visão geral do fluxo de caixa do usuário;
  - RF9: Gráficos e relatórios dinâmicos sobre o fluxo de caixa (mensal, trimestral e anual);
  - RF10: Personalização de categorias;
  - RF11: Histórico completo de transações com filtros;

- Planejamento financeiro:
  - RF12: Definição de metas financeiras;
  - RF13: Sugestão de planejamento com base nas movimentações;

- Análise preditiva:
  - RF14: IA para previsão de fluxo de caixa;
  - RF15: Recomendação de ajustes orçamentários;

- Alertas e notificações:
  - RF16: Notificações sobre metas, despesas fora do padrão, vencimentos e alertas relevantes;

#### 3.1.2 Requisitos Não-Funcionais

- **Escalabilidade:**
  - RNF1: Uso do Google Cloud;

- **Desempenho:**
  - RNF2: Consultas otimizadas via ORM Django;

- **Segurança:**
  - RNF4: Criptografia de ponta-a-ponta;
  - RNF5: Autenticação JWT;
  - RNF6: Proteção contra SQL Injection, XSS, CSRF;
  - RNF7: Armazenamento seguro de senhas (bcrypt);

- **Usabilidade:**
  - RNF8: Front-end responsivo em ReactJS;

- **Monitoramento e Logs:**
  - RNF9: Logs e monitoramento via Datadog;

- **Compatibilidade:**
  - RNF10: Suporte a navegadores modernos;

- **Desenvolvimento e Manutenção:**
  - RNF11: Código documentado;
  - RNF12: Testes unitários e integração;

- **Integração com IA:**
  - RNF13: IA desenvolvida em Python com aprendizado contínuo;
  - RNF14: Uso de ML para previsões financeiras;
  - RNF15: Cálculos de IA sem comprometer o desempenho;

- **Licenciamento e Conformidade:**
  - RNF16: Conformidade com LGPD;
  - RNF17: Consentimento e transparência no uso dos dados.

### 3.2 Considerações de Design

- Justificativa das escolhas de design
- Arquitetura baseada em componentes e microserviços
- Uso de modelos C4 (Contexto, Contêineres, Componentes, Código)

### 3.3 Stack Tecnológica

- **Back-end:** Django + Django Rest Framework
- **Front-end:** ReactJS
- **Bibliotecas:** Pandas, Scikit-learn, Prophet, QuantLib, Plotly, Dash
- **Banco de dados:** PostgreSQL
- **Monitoramento:** Datadog
- **CI/CD:** GitHub Actions + Docker
- **Gerenciamento:** Jira, SonarCloud

### 3.4 Considerações de Segurança

- Criptografia
- Práticas de proteção contra vulnerabilidades
- Conformidade com a LGPD

---

## 4. Próximos Passos

- Prototipação inicial e validação com usuários
- Início da implementação dos módulos principais
- Testes e integração contínua
- Avaliação dos resultados da primeira fase (Portfólio I)
- Refinamento e entrega final (Portfólio II)

---

## 5. Referências

- https://www.treasy.com.br/blog/graficos-financeiros/
- https://blog.nubank.com.br/planejamento-financeiro-pessoal/
- https://wise.com/br/blog/planejamento-financeiro-com-ia
- https://www.luiztools.com.br/post/12-dicas-para-construcao-de-um-bom-saas/
- https://journalmediacritiques.com/index.php/jmc/article/view/85

---

## 6. Apêndices (Opcionais)

- Dados de suporte e gráficos adicionais

---

## 7. Avaliações de Professores

- Considerações Professor/a:
- Considerações Professor/a:
- Considerações Professor/a:

