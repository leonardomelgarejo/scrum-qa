# Fluxo de Automação de Testes por Sprint (SCRUM)

Este documento descreve o processo recomendado para automatizar testes em contexto ágil (SCRUM), priorizando a entrega contínua de qualidade e evitando acúmulo de dívida técnica.

---

## Etapas do Ciclo de Automação

### 1. Pré-Sprint (Refinamento)
- [ ] QA participa dos refinamentos das histórias.
- [ ] Identificar critérios de aceitação testáveis e automatizáveis.
- [ ] Avaliar a viabilidade técnica (ambiente, mocks, dados).
- [ ] Marcar cenários com tags sugeridas (`@manual`, `@automated`, `@skip`).

---

### 2. Início da Sprint
- [ ] Criar mini plano de testes por história.
- [ ] Alinhar com Devs pontos de testabilidade e possíveis *test hooks*.
- [ ] Priorizar testes automatizáveis de API e Unitários.

---

### 3. Durante a Sprint
- [ ] Validar manualmente os cenários assim que possível.
- [ ] Iniciar automação assim que a funcionalidade estiver disponível.
- [ ] Adicionar testes ao CI/CD (se aplicável).
- [ ] Seguir a ordem de prioridade:
  1. Unitários (Dev)
  2. API (QA ou Dev)
  3. UI (somente quando necessário)

---

### 4. Durante Pull Request
- [ ] Validar que os testes automatizados passaram.
- [ ] Revisar se os critérios de aceitação estão cobertos por testes.
- [ ] Realizar testes exploratórios se aplicável.

---

### 5. Final da Sprint / Review
- [ ] Apresentar a cobertura de testes da sprint.
- [ ] Documentar testes automatizados (ex.: tags, links no TestRail/ClickUp).
- [ ] Criar tarefas técnicas para automação pendente, se necessário.

---

## Estrutura Sugerida de Tempo por História

| Tipo de Teste              | Tempo Médio |
|---------------------------|-------------|
| Planejamento QA           | 30–45 min   |
| Teste Manual Exploratório | 30 min – 1h |
| Automação de API          | 1–2h        |
| Automação de UI Simples   | 2–4h        |
| Automação de UI Complexa  | até 6h      |
| Documentação/Checklist    | 30 min      |

---

## Definition of Done (DoD) - QA

- [ ] Testes manuais executados com sucesso
- [ ] Testes automatizados implementados e passando
- [ ] Testes integrados ao CI/CD (se aplicável)
- [ ] Nenhum cenário crítico ficou manual (sem justificativa)
- [ ] Documentação atualizada

---

## Observações

- Automação **não deve ser deixada para depois da sprint**, exceto em casos justificados e documentados.
- Sempre priorize **testes de API e unitários** antes de testes de UI.
- Mantenha as automações simples, rápidas e estáveis — especialmente no CI.
