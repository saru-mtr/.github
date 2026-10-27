# Como contribuir

Este arquivo vale para todos os repositórios da organização SARU Motorsport Technologies (saru-mtr) que não
tiverem um `CONTRIBUTING.md` próprio.

## Passo a passo

1. Abra uma issue nova ou pegue uma existente, com prefixo de família no título e no
   rótulo (`E`, `PIL`, `CAM`, `ENG`, `EQP`, `ALU`).
2. Crie a branch a partir da issue, já com o nome no padrão `<prefixo>/<numero>-<tema>`,
   em minúsculas e com hífen entre palavras, e mude para ela:
   `gh issue develop <numero> --name pil/42-corte-de-volta-por-gps --checkout` (ou via `wt novo`).
3. Confira com `git branch --show-current` que está na branch certa antes do primeiro commit.
4. Faça commits em Conventional Commits, em português, até 72 caracteres no título
   (exemplo: `feat(leitor): adiciona corte de volta por GPS`).
5. Abra o pull request com `Closes #<numero>` (para fechar a issue automaticamente no merge) ou `Refs #<numero>` (quando a issue aguardar conferência manual), para vincular a tarefa.
6. Espere a CI ficar verde e sem conflitos. O merge é por squash; o agente mescla o próprio PR
   com CI verde e sem conflito (regra global do ecossistema).
7. Apague a branch após o merge.

## Definition of Ready

Uma issue entra em desenvolvimento quando, nesta ordem:

1. Tem id com prefixo e está no catálogo da família ou da empresa.
2. Tem fonte registrada.
3. Diz para quem e para quê, e aponta um objetivo claro.
4. Tem pelo menos um critério de aceitação em Dado, Quando, Então.
5. As dependências estão listadas e nenhuma está bloqueada.
6. Quem vai fazer entendeu o escopo; dúvida bloqueante vira pergunta a Vitor antes de começar.
7. Se toca física, calibração ou validação, a regra segue E-RN-02 (número de física só com tabela de medição comprovada contra o acervo).

## Definition of Done

Um item está pronto quando:

1. Cada critério de aceitação foi verificado por teste automatizado ou demonstração registrada.
2. Lint e testes estão verdes na CI.
3. A documentação (`decisions.md`, ADR ou matriz de rastreabilidade) foi atualizada no mesmo PR.
4. O PR foi mesclado por squash na `main`.
5. Nenhum push direto na `main`.

## Uso de IA

Toda contribuição gerada por um agente de IA leva, na descrição do pull request, a identificação
do agente e a issue de referência. O agente mescla o próprio PR quando a CI estiver verde e sem conflito.
Ações destrutivas, exclusões em massa ou alterações de permissões globais continuam exigindo
aprovação humana prévia.

## Segredo

Cada repositório lista suas variáveis de ambiente em `.env.example`, sem valores reais.
O arquivo `.env` nunca é commitado (fica sempre em `.gitignore`). Segredos de produção
ficam nos GitHub Secrets da organização.
