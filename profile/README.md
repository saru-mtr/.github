# SARU Motorsport Technologies (SARU MT)

A SARU é uma empresa de tecnologia focada em motorsport que conecta telemetria real,
simulação dinâmica veicular e decisão técnica rastreável de engenharia de pista.

## Repositórios ativos

- [`saru-plataforma`](https://github.com/saru-mtr/saru-plataforma): monorepo do produto, com leitores de telemetria multiformato (AiM, MoTeC, Bosch, Wintax, etc.), pipeline de dados, banco PostgreSQL, API FastAPI e interface web (Vite/React).
- [`saru-simulador`](https://github.com/saru-mtr/saru-simulador): simulador de volta (motores QSS e 14-DOF), dados processados por pista e replay 3D.
- [`saru-empresa`](https://github.com/saru-mtr/saru-empresa): decisões da empresa, requisitos das famílias (Piloto, Engenheiro, Equipe, Aluno, Campeonato), física documental, marca, negócio e processos.
- [`saru-hardware`](https://github.com/saru-mtr/saru-hardware): datalogger NV-Logger (CAN/OBD, GNSS), sniffing passivo de alta taxa e ferramentas de calibração de bancada.

## Repositórios de consulta e legado

- [`saru-poc-trackday`](https://github.com/saru-mtr/saru-poc-trackday): PoC congelada de validação do pipeline ponta a ponta em track day (referência e portabilidade).
- `saru-app`: legado arquivado da versão anterior da interface e serviços.

## Processo

- **GitHub Flow**: branch curta a partir de `main`, pull request ligado à issue, CI verde e merge por squash.
- **Linguagem**: Conventional Commits em português, títulos até 72 caracteres.
- **Rastreabilidade**: issue com prefixo de família (`PIL-`, `ENG-`, `EQP-`, `E-`) antes de qualquer código.

## Por onde começar

Consulte o [`CONTRIBUTING.md`](../CONTRIBUTING.md) deste repositório antes de abrir uma issue ou pull request.
