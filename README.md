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
