# Proposta de Intervenção Técnica e Ética  
## Atividade Prática – O Dilema da IA Contratadora  

Curso: Tecnologia em Sistemas para Internet  
Componente Curricular: Engenharia de Software  
Professor: Gaio B. Oliveira  

---

## 1. Análise do Dilema

A startup desenvolveu um software de Inteligência Artificial para triagem de currículos.  
Durante os testes, foi identificado que o algoritmo apresenta **viés algorítmico**, favorecendo determinados perfis demográficos e prejudicando grupos minoritários.

Esse problema surge porque o modelo foi treinado com dados históricos que já continham preconceitos implícitos.

### Riscos identificados:

- ⚖ Risco jurídico (LGPD – Art. 20)
- 💰 Risco financeiro (multas e processos)
- 📉 Risco reputacional
- ⚠ Violação de princípios éticos da Engenharia de Software

---

## 2. Aplicação do Código de Ética ACM/IEEE

### Cláusula 1.03
Aprovar software somente se houver crença fundamentada de que ele é seguro e não prejudica a sociedade.

**Aplicação:**  
O sistema está discriminando candidatos. Portanto, não pode ser aprovado para lançamento enquanto o problema não for corrigido.

---

### Cláusula 3.01
Garantir que o software seja desenvolvido seguindo altos padrões profissionais e éticos.

**Aplicação:**  
Ignorar o viés para acelerar o lançamento seria negligência profissional e violaria a responsabilidade social do engenheiro de software.

---

## 3. Comparação das Soluções Técnicas

| Solução | Prós | Contras | Avaliação Ética |
|----------|------|---------|----------------|
| Lançar como está | Não atrasa investidores | Alto risco jurídico e reputacional | ❌ Antiética |
| Human-in-the-loop | Reduz exclusão automática | Ainda mantém viés no ranking | ✔ Parcial |
| Toolkit de Explicabilidade (XAI) | Transparência e alinhamento com LGPD | Pode expor parte da lógica interna | ✔ Boa prática |
| Auditoria de Dados (4 semanas) | Corrige o problema na raiz | Pequeno atraso no lançamento | ✅ Melhor opção |

---

## 4. Impacto Financeiro

### Cenário 1 – Processo Judicial
- Multas de até 2% do faturamento (limitadas a R$ 50 milhões por infração).
- Custos com advogados.
- Danos à imagem da empresa.
- Possível perda de investidores.

### Cenário 2 – Atraso de 4 semanas
- Custo operacional adicional.
- Pequeno atraso estratégico.
- Preservação da reputação.
- Redução de riscos legais.

**Conclusão financeira:**  
O custo de um processo judicial é potencialmente muito maior do que o impacto de um atraso de 4 semanas para auditoria.

---

## 5. Proposta Final do Time (Solução Integrada)

Propomos uma estratégia combinada:

1. Realizar Auditoria de Dados (atraso de 4 semanas).
2. Implementar temporariamente o modelo Human-in-the-loop.
3. Adicionar módulo de explicabilidade (XAI).
4. Garantir mecanismo de revisão humana conforme Art. 20 da LGPD.

Essa solução equilibra:

- Responsabilidade social
- Conformidade legal
- Qualidade técnica
- Sustentabilidade financeira

---

## 6. Conclusão

A Engenharia de Software exige responsabilidade ética além da competência técnica.  
Lançar um sistema enviesado comprometeria direitos fundamentais e poderia gerar graves consequências legais e financeiras.

Seguindo o Código de Ética ACM/IEEE, a decisão mais responsável é realizar a auditoria e implementar mecanismos de transparência antes do lançamento.

