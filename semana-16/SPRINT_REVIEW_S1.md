# Sprint Review & Retrospectiva — Sprint 1

**Projeto:** SAI — Sistema de Alerta Inteligente  
**Time:** ImperaTech  
**Data:** 09/06/2026  
**Facilitador:** Prof. Gaio Belitardo de Oliveira  
**Presentes:** Alexandro, André, Danilo, Rafael Torres de Araujo, Victor,

---

## Métricas da Sprint 1

| Métrica | Valor |
|---|---|
| Velocidade realizada | 34 pts |
| Capacidade planejada | 42 pts |
| Stories entregues | 8 / 11 |
| Stories movidas para backlog | 3 |
| Duração | 2 semanas |

---

## Incremento de Software Demonstrado

URL: **https://saisjbv.vercel.app/#/dashboard**

| # | User Story | Pontos | Status |
|---|---|---|---|
| 1 | Cards de temperatura, umidade, qualidade do ar e alertas ativos em tempo real | 5 | ✅ Feito |
| 2 | Bloco "Clima Atual – São João da Boa Vista" com sensação térmica, pressão, vento e chuva | 8 | ✅ Feito |
| 3 | Parecer Operacional (IA) com score 0/100, ameaças detectadas, confiança e nível de risco | 5 | ✅ Feito |
| 4 | Alertas Regionais com lista de cidades afetadas e severidade (Alto) | 3 | ✅ Feito |
| 5 | Previsão local 7 dias com carrossel de datas, ícones e temperaturas min/máx | 5 | ✅ Feito |
| 6 | Consulta climática por cidade (busca avulsa) | 3 | ✅ Feito |
| 7 | Sidebar com navegação: Dashboard, Mapa, Analíticos, Alertas, Estações, Centro de Controle | 3 | ✅ Feito |
| 8 | Identidade visual ImperaTech + indicador "Sistema Online" no header | 2 | ✅ Feito |
| 9 | Página de Mapa interativo com camadas de estações e alertas | 5 | ⚠️ Parcial |
| 10 | Tela de Analíticos com gráficos históricos de temperatura e umidade | 5 | 🔲 Backlog |
| 11 | Gerenciamento de Estações — CRUD básico (tela Admin) | 3 | 🔲 Backlog |

---

## Anotações da Reunião

### ✅ O que funcionou bem

- Dashboard funcional e visualmente coerente entregue no prazo, com dados reais de clima via API
- Parecer da IA integrado exibindo score, confiança e ameaças detectadas no frontend
- Deploy contínuo no Vercel funcionando sem fricção; URL pública compartilhada com o professor
- Comunicação via grupo manteve todos os membros alinhados sobre o status das tasks

### ⚠️ O que pode melhorar

- Mapa não ficou pronto — subtarefas não foram quebradas em granularidade suficiente no planejamento
- Alertas regionais exibem dados duplicados (mesma linha repetida); requer correção antes da Sprint 2
- Analíticos e CRUD de Estações foram empurrados para o backlog por falta de estimativa realista
- Definition of Done não estava clara para componentes de UI — formalizar na Sprint 2

### 💬 Feedbacks do Professor / Stakeholders

- Parecer da IA agrega valor ao produto; sugestão de tornar o score mais explicativo (detalhar critérios usados)
- Alertas precisam de distinção visual mais clara entre os níveis Alto / Médio / Baixo
- Explorar notificações em tempo real (push ou e-mail) como diferencial na Sprint 2
