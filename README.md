# Controle 5.17 – Authentication Information (ISO/IEC 27001:2022)

Este repositório contém um módulo educacional e prático para **avaliar maturidade** relacionada à **governança e proteção de informações de autenticação** (credenciais), com base em boas práticas de Segurança da Informação e conformidade.

## Objetivo do controle (linguagem própria)
Estabelecer e manter práticas para **proteger credenciais e mecanismos de autenticação** (ex.: senhas, chaves, tokens, segredos de aplicações), garantindo que o uso dessas credenciais seja **individualizável, rastreável e proporcional ao risco**, reduzindo a probabilidade de acessos indevidos.

## Principais riscos mitigados
- Comprometimento de credenciais (phishing, reuse, vazamento, força bruta).
- Acesso não autorizado por autenticação fraca ou ausência de MFA.
- Uso de contas genéricas/compartilhadas, reduzindo rastreabilidade e accountability.
- Reset de senha vulnerável (engenharia social, validação insuficiente).
- Falta de monitoramento/detecção de abuso de autenticação.
- Exposição de segredos em código, planilhas, e-mails ou repositórios.

## Elementos avaliados no deep dive
O formulário avalia três grupos de critérios:

1) **Gestão de Credenciais**
- Política e padrões mínimos (complexidade, rotação quando aplicável, proibições de compartilhamento).
- Processo de criação/alteração/reset com validação adequada.
- Tratamento de contas genéricas e credenciais de serviço (controles e ownership).
- Regras para armazenamento e manuseio de segredos (vault, variáveis seguras, etc.).

2) **Autenticação e MFA**
- Aplicação de MFA para acessos críticos e privilegiados.
- Padronização de autenticação por criticidade (ex.: acesso administrativo vs. acesso comum).
- Requisitos para acesso remoto e acesso a ambientes sensíveis.
- Resistência a ataques comuns (brute force, credential stuffing, MFA fatigue quando aplicável).

3) **Proteção e Monitoramento**
- Proteção criptográfica adequada para credenciais e segredos (em repouso e em trânsito).
- Bloqueio, rate limiting e detecção de tentativas anômalas.
- Logs e trilhas de auditoria sobre autenticação (sucesso, falha, reset, elevação).
- Indicadores operacionais para governança (ex.: contas sem MFA, resets suspeitos, falhas repetidas).

## Escala de maturidade (0 a 5)
- **0 – Inexistente:** não há prática estruturada; controles não são aplicados.
- **1 – Ad-hoc:** práticas informais e inconsistentes; dependem de pessoas e urgências.
- **2 – Documentado:** regras existem, mas a aplicação varia entre sistemas/equipes.
- **3 – Padronizado:** processos replicáveis; aplicação consistente; responsabilidades definidas.
- **4 – Automatizado:** controles suportados por ferramentas e fluxos; evidências mais fáceis de obter.
- **5 – Baseado em Risco:** requisitos e exceções são proporcionais à criticidade; decisões são justificadas, registradas e revisadas.

## Conexão com 5.15 e 5.16
- **5.15 (Access Control)** define as regras e restrições de acesso (quem pode acessar o quê).
- **5.16 (Identity Management)** governa o ciclo de vida da identidade (criação, mudança e desligamento).
- **5.17 (Authentication Information)** protege o “mecanismo de validação” dessas identidades.  
Sem 5.17 consistente, 5.15 e 5.16 perdem eficácia: é possível ter política e ciclo de vida bem definidos, mas com autenticação frágil a organização continua exposta.

## Como executar
1. Baixe o repositório.
2. Abra o arquivo `index.html` diretamente no navegador (projeto **out-of-the-box**, sem backend).
3. Preencha os critérios (0 a 5). A média e classificação são calculadas automaticamente.

## Caráter educacional
Este material é **educacional** e voltado ao estudo de maturidade e arquitetura de controles.  
Não substitui auditoria formal, avaliação de conformidade, nem certificação.

## Replicabilidade
Este modelo foi estruturado para ser reutilizável em outros controles: basta ajustar o **título**, a **referência** e os **critérios** no `index.html`, mantendo a mesma base de cálculo e layout.

## FAQ – Controle 5.17 (Authentication Information)

### 1) O que exatamente está sendo medido neste módulo?
O módulo mede **maturidade de governança e execução** relacionada à proteção de credenciais e autenticação, avaliando se a organização possui práticas consistentes, rastreáveis e proporcionais ao risco para gestão de credenciais, uso de MFA e monitoramento de autenticação.

### 2) Por que “maturidade” é diferente de “ter MFA ligado”?
MFA é um mecanismo. Maturidade inclui:
- política e critérios por criticidade,
- processos de reset e exceções controladas,
- cobertura consistente em sistemas críticos,
- evidências e rastreabilidade,
- monitoramento e resposta a anomalias.

Ou seja, maturidade considera o controle como um **sistema de gestão**, não um item isolado.

### 3) Como lidar com contas técnicas/serviço sem expor credenciais?
O ponto central é reduzir a dependência de credenciais estáticas e tornar o uso auditável:
- ownership formal,
- armazenamento seguro de segredos,
- rotação quando aplicável,
- segregação e escopo mínimo,
- logging e trilha de auditoria do uso.

O objetivo é manter continuidade operacional sem perder governança e rastreabilidade.

### 4) Qual a diferença prática entre Nível 3 (Padronizado) e Nível 4 (Automatizado)?
- **Nível 3**: processos são consistentes e replicáveis, porém podem depender de execução manual e controles por amostragem.
- **Nível 4**: controles passam a ser aplicados/validados por ferramentas e fluxos (ex.: enforcement de MFA, políticas centralizadas, evidências geradas automaticamente), reduzindo variabilidade e aumentando confiabilidade.

### 5) Como este controle se conecta a governança e auditoria?
A proteção de credenciais impacta diretamente:
- rastreabilidade (accountability) e trilha de auditoria,
- segregação de funções e responsabilidade individual,
- eficácia de controles de acesso,
- evidências de conformidade.

Em termos de auditoria, credenciais fracas ou compartilhadas reduzem a confiança na atribuição de ações a indivíduos e aumentam risco operacional e regulatório.
