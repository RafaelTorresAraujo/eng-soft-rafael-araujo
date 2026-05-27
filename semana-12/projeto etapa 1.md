# 🌩️ SAI — Sistema de Antecipação Inteligente
### Projeto Final — Etapa 1 | Desenvolvimento Ágil com Scrum

> **Curso:** Tecnologia em Sistemas para Internet  
> **Disciplina:** Engenharia de Software  
> **Professor:** Gaio Belitardo de Oliveira  
> **Data:** 26/05/2026

---

## 👥 Integrantes do Grupo

| Nome | Função |
|------|--------|
| Alex | Product Owner |
| Vitor | Developer |
| Rafael | Developer |
| Andre | Developer |
| Danilo | Developer |

---

## 📌 Atividade 2 — Escolha do Problema

O projeto escolhido pelo grupo foi o **SAI — Sistema de Antecipação Inteligente**. Trata-se de uma plataforma criada para auxiliar prefeituras, órgãos da Defesa Civil e empresas logísticas no monitoramento e antecipação de riscos climáticos e operacionais.

O sistema busca resolver problemas relacionados a enchentes, tempestades, bloqueios de rotas, demora na tomada de decisão e falta de alertas preventivos. A proposta do SAI é utilizar monitoramento inteligente, análise operacional e alertas automáticos para ajudar gestores a agir **antes que os problemas aconteçam**.

> ⚠️ **Problema Central:** Gestores públicos e privados tomam decisões sobre riscos climáticos e logísticos com informações tardias, fragmentadas e sem integração. Isso resulta em atrasos na resposta a desastres, prejuízos logísticos e risco à vida de cidadãos em áreas vulneráveis.

---

## 🎯 Atividade 3 — Visão do Produto e Personas

### Visão do Produto

> *"O SAI será uma plataforma inteligente de monitoramento climático e operacional capaz de gerar alertas automáticos, exibir áreas de risco, organizar informações estratégicas e auxiliar órgãos públicos e privados na prevenção de desastres e falhas logísticas."*

### Personas

| # | Persona | Objetivo Principal | Dor Principal |
|---|---------|-------------------|---------------|
| 🚨 | Coordenador da Defesa Civil | Agir antes de desastres | Recebe informações tarde demais |
| 🏛️ | Gestora Pública | Tomar decisões rápidas e embasadas | Falta de dados organizados e centralizados |
| 🚛 | Gerente Logístico | Evitar prejuízos operacionais | Não consegue prever problemas de rota |
| 👨‍👩‍👧 | Cidadão em Área de Risco | Proteger a família com antecedência | Não recebe alertas antecipados |

---

## 📋 Atividade 4 — Product Backlog Inicial

O time elicitou os requisitos a partir das necessidades das personas, utilizando o formato padrão de Histórias de Usuário **(User Stories — 3W)**:  
`"Como um [papel], eu quero [funcionalidade] para [benefício]"`

| ID | História de Usuário |
|----|---------------------|
| US01 | Como **gestor**, quero visualizar um **painel de riscos** para entender a situação atual da cidade. |
| US02 | Como **Defesa Civil**, quero **receber alertas automáticos** para agir antes do desastre. |
| US03 | Como **gestor**, quero **cadastrar áreas de risco** para monitorar regiões críticas. |
| US04 | Como **usuário**, quero **visualizar mapa interativo** para identificar áreas perigosas. |
| US05 | Como **gerente logístico**, quero **receber aviso de rotas afetadas** para evitar atrasos. |
| US06 | Como **prefeitura**, quero **gerar relatórios operacionais** para registrar ocorrências. |
| US07 | Como **cidadão**, quero **receber alertas via WhatsApp/SMS** para proteger minha família. |
| US08 | Como **gestor**, quero **classificar alertas por gravidade** para priorizar ações de resposta. |
| US09 | Como **administrador**, quero **controlar permissões de acesso** para proteger o sistema. |
| US10 | Como **gestor**, quero **acessar histórico de alertas** para analisar padrões e tendências. |

---

## 🏷️ Atividade 5 — Priorização de Backlog e Valor de Negócio

### Método 1: Matriz MoSCoW

| Classificação | Descrição |
|---------------|-----------|
| 🔵 **Must Have** | MVP obrigatório — o software não funciona sem isso |
| 🔷 **Should Have** | Importante, mas o sistema sobrevive sem na primeira entrega |
| ⬜ **Could Have** | Desejável se houver tempo e orçamento |
| ⬛ **Won't Have** | Fora do escopo atual — registrado para releases futuras |

| ID | Funcionalidade | Classificação |
|----|---------------|---------------|
| US01 | Painel operacional de riscos | 🔵 Must Have |
| US02 | Alertas automáticos | 🔵 Must Have |
| US03 | Cadastro de áreas de risco | 🔵 Must Have |
| US04 | Mapa interativo | 🔵 Must Have |
| US05 | Avisos de rotas afetadas | 🔷 Should Have |
| US06 | Relatórios operacionais | 🔷 Should Have |
| US07 | Alertas via WhatsApp/SMS | 🔷 Should Have |
| US08 | Classificação de alertas por gravidade | 🔵 Must Have |
| US09 | Controle de usuários e permissões | 🔵 Must Have |
| US10 | Histórico de alertas | 🔷 Should Have |

---

### Método 2: Análise de Valor vs. Esforço

**Legenda dos Quadrantes:**

| Quadrante | Valor | Esforço | Ação |
|-----------|-------|---------|------|
| ⚡ **Vitória Rápida** | Alto | Baixo | Prioridade máxima — puxar para a Sprint |
| 🏗️ **Grande Projeto** | Alto | Alto | Quebrar em tarefas menores antes de executar |
| 🔹 **Preenchimento** | Baixo | Baixo | Fazer apenas se o time estiver livre |
| ⏳ **Sumidouro de Tempo** | Baixo | Alto | Descartar imediatamente |

| ID | Funcionalidade | Valor (1–5) | Esforço (1–5) | Quadrante |
|----|---------------|:-----------:|:-------------:|-----------|
| US01 | Painel operacional de riscos | 5 | 3 | 🏗️ Grande Projeto |
| US02 | Alertas automáticos | 5 | 2 | ⚡ Vitória Rápida |
| US03 | Cadastro de áreas de risco | 5 | 2 | ⚡ Vitória Rápida |
| US04 | Mapa interativo | 5 | 3 | 🏗️ Grande Projeto |
| US05 | Avisos de rotas afetadas | 4 | 3 | 🏗️ Grande Projeto |
| US06 | Relatórios operacionais | 4 | 2 | ⚡ Vitória Rápida |
| US07 | Alertas via WhatsApp/SMS | 5 | 4 | 🏗️ Grande Projeto |
| US08 | Classificação de alertas | 5 | 2 | ⚡ Vitória Rápida |
| US09 | Controle de usuários e permissões | 5 | 3 | 🏗️ Grande Projeto |
| US10 | Histórico de alertas | 4 | 2 | ⚡ Vitória Rápida |

---

## 🚀 Product Backlog Refatorado e Ordenado

> A história na posição **#1 é a mais prioritária do projeto**. A ordenação combina MoSCoW + Quadrante de Valor vs. Esforço.

| Rank | ID | Funcionalidade | Motivo da Prioridade | Quadrante |
|:----:|----|---------------|----------------------|-----------|
| 🥇 1° | US02 | Alertas automáticos de risco | Vitória Rápida + Must Have — núcleo do sistema | ⚡ Vitória Rápida |
| 🥈 2° | US03 | Cadastro de áreas de risco | Vitória Rápida + Must Have — habilita o monitoramento | ⚡ Vitória Rápida |
| 🥉 3° | US08 | Classificação de alertas por gravidade | Vitória Rápida + Must Have — prioriza respostas | ⚡ Vitória Rápida |
| 4° | US01 | Painel operacional de riscos | Must Have — visibilidade do cenário geral | 🏗️ Grande Projeto |
| 5° | US04 | Mapa interativo de áreas de risco | Must Have — visualização espacial crítica | 🏗️ Grande Projeto |
| 6° | US09 | Controle de usuários e permissões | Must Have — segurança do sistema | 🏗️ Grande Projeto |
| 7° | US06 | Relatórios operacionais | Vitória Rápida + Should Have | ⚡ Vitória Rápida |
| 8° | US10 | Histórico de alertas | Vitória Rápida + Should Have | ⚡ Vitória Rápida |
| 9° | US05 | Avisos de rotas afetadas | Grande Projeto + Should Have | 🏗️ Grande Projeto |
| 10° | US07 | Alertas via WhatsApp/SMS | Grande Projeto + Should Have — requer integração externa | 🏗️ Grande Projeto |

> **Nota:** As categorias *Could Have* e *Won't Have* não foram elicitadas nesta etapa pois o foco é estabelecer o MVP funcional. Itens como integrações com sistemas meteorológicos externos, dashboard mobile nativo e API pública poderão compor o backlog de releases futuras.

---

<div align="center">

**SAI — Sistema de Antecipação Inteligente** · Etapa 1 concluída ✅

*Engenharia de Software · Tecnologia em Sistemas para Internet*

</div>
