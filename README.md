# AppMonitor Pipeline

[![CI Pipeline Status](https://img.shields.io/github/actions/workflow/status/raquelsantos242/appmonitor-pipeline/ci.yml?branch=main&label=CI%20Pipeline)](https://github.com/raquelsantos242/appmonitor-pipeline/actions/workflows/ci.yml)

## O Papel Central do Git na Entrega Contínua

O Git fornece a base para a entrega contínua ao versionar cada mudança no código e permitir que pipelines de CI/CD sejam acionados automaticamente por commits, branches ou tags. Com **branches**, equipes isolam o trabalho em novas funcionalidades, correções ou experimentos sem comprometer o código estável, integrando apenas o que já foi revisado e testado ao branch principal. Já as **tags** atuam como marcadores imutáveis de versões específicas (por exemplo, v1.0.0), facilitando a identificação de releases, auditorias e rollbacks precisos. Em ferramentas como CircleCI, filtros de branch garantem que builds e testes rodem apenas em branches definidos (como main ou develop), enquanto filtros de tag disparam deploys de produção somente quando uma tag de release é criada, assegurando um fluxo de entrega mais organizado, seguro e previsível.

## GitHub Actions: Gerenciamento de Segredos, Variáveis e Ambientes

No contexto de pipelines de CI/CD, o GitHub Actions oferece três mecanismos para gerenciar valores sensíveis e configurações:

**Segredos** protegem informações confidenciais como chaves de API e credenciais, sendo armazenados de forma criptografada e nunca expostos em logs. **Variáveis** armazenam valores não sensíveis compartilhados entre workflows, como URLs de ambientes ou endereços de suporte, visíveis na interface mas protegidas contra modificações acidentais. **Ambientes** organizam esses elementos em grupos lógicos (como desenvolvimento, staging e produção), permitindo políticas específicas por estágio e resolvendo conflitos através de uma hierarquia clara: configurações de organização são substituídas por repositório, que por sua vez são substituídas por ambiente.

Esta integração entre Git e GitHub Actions forma um ciclo virtuoso: o Git fornece a base para controle de versão e colaboração, enquanto o GitHub Actions automatiza a construção, teste e implantação, usando segredos e variáveis para garantir segurança e flexibilidade em todo o pipeline de entrega contínua.

## Workflows Implementados

### 1. CI Pipeline (ci.yml)
### 2. Deploy to Production (deploy.yml)
### 3. Diagnostic Workflow (diagnostic.yml)
### 4. Variables Demo (run-monitor.yml)


## Referências
MONTINI, L. GitHub Actions: Secrets and Environment Variables in your pipeline. Disponível em: <https://leonardomontini.dev/github-actions-secrets-variables/>. Acesso em: 15 jun. 2025.

Git tags vs branches: Differences and when to use them. Disponível em: <https://circleci.com/blog/git-tags-vs-branches/>.

