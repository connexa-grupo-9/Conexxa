# ADR-001 — Solução de arquitetura e stack da aplicação

- **Situação:** proposta
- **Data:** 2026-10-30
- **Participantes:** Gabriel, Thiago, Matheus, Camila, Kauan

## Contexto

Para decidir qual stack será utilizada, é necessário considerar as experiências pessoais e profissionais de cada membro da equipe. Para a decisão de modelo de arquitetura, é necessário considerar a escala prevista para a aplicação, sua base de usuários, e os objetivos de segurança e robustez do cliente.

## Decisão

A arquitetura escolhida para a aplicação utiliza dois componentes principais:
- Serviço Frontend em React desenvolvido em forma de SPA.
- Backend aderente ao modelo de *slicing* vertical, desenvolvido em ASP.NET

## Alternativas consideradas

| Alternativa | Por que não foi escolhida |
|---|---|
| Monolito vertical | Alto risco de acoplamento durante a sua implementação |
| Microsserviços | Complexidade incompatível com os recursos e necessidades do projeto |

## Consequências

- **Positivas:** Facilidade dos membros da equipe em interagir com o ASP.NET, arquitetura robusta com baixo acoplamento entre cada módulo.
- **Negativas:** Implementação do sistema precisa aderir obrigatoriamente ao modelo escolhido.
- **Como verificar:** Validação do uso do ASP.NET como framework, validação do uso das ferramentas de compilação da Microsoft.
