# FAQ – Controle 5.17 (Authentication Information)

## 1) O que exatamente está sendo medido neste módulo?
O módulo mede **maturidade de governança e execução** relacionada à proteção de credenciais e autenticação, avaliando se a organização possui práticas consistentes, rastreáveis e proporcionais ao risco para gestão de credenciais, uso de MFA e monitoramento de autenticação.

## 2) Por que “maturidade” é diferente de “ter MFA ligado”?
MFA é um mecanismo. Maturidade inclui:
- política e critérios por criticidade,
- processos de reset e exceções controladas,
- cobertura consistente em sistemas críticos,
- evidências e rastreabilidade,
- monitoramento e resposta a anomalias.
Ou seja, maturidade considera o controle como um **sistema de gestão**, não um item isolado.

## 3) Como lidar com contas técnicas/serviço sem expor credenciais?
O ponto central é reduzir a dependência de credenciais estáticas e tornar o uso auditável:
- ownership formal,
- armazenamento seguro de segredos,
- rotação quando aplicável,
- segregação e escopo mínimo,
- logging e trilha de auditoria do uso.
O objetivo é manter continuidade operacional sem perder governança e rastreabilidade.

## 4) Qual a diferença prática entre Nível 3 (Padronizado) e Nível 4 (Automatizado)?
- **Nível 3**: processos são consistentes e replicáveis, porém podem depender de execução manual e controles por amostragem.
- **Nível 4**: controles passam a ser aplicados/validados por ferramentas e fluxos (ex.: enforcement de MFA, políticas centralizadas, evidências geradas automaticamente), reduzindo variabilidade e aumentando confiabilidade.

## 5) Como este controle se conecta a governança e auditoria?
A proteção de credenciais impacta diretamente:
- rastreabilidade (accountability) e trilha de auditoria,
- segregação de funções e responsabilidade individual,
- eficácia de controles de acesso,
- evidências de conformidade.
Em termos de auditoria, credenciais fracas ou compartilhadas reduzem a confiança na atribuição de ações a indivíduos e aumentam risco operacional e regulatório.