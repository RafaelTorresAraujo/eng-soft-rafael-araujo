# Exercícios de Revisão — Semana 10
**Engenharia de Software** | Prof. Gaio B. Oliveira | 28/04/2026

---

## Cenário 1 — Logística de E-commerce Global

**Diagrama:** Casos de Uso

```mermaid
flowchart LR
    OP(["Operador\nLogístico"])
    RF(["Receita\nFederal"])
    TR(["Transportadora"])

    subgraph SIS ["Sistema de Despacho"]
        direction TB
        UC1(["Consultar\nEstoque"])
        UC2(["Consultar Status\nde Entrega"])
        UC3(["Emitir\nNota Fiscal"])
        UC4(["Gerar Ordem\nde Despacho"])
    end

    OP --> UC4
    TR --> UC2
    UC3 --> RF
    UC1 --> UC4
    UC2 --> UC4
    UC4 -.->|include| UC3
```

---

## Cenário 2 — Totem de Autoatendimento em Fast-Food

**Diagrama:** Casos de Uso

```mermaid
flowchart LR
    CL(["Cliente"])
    CZ(["Cozinheiro"])
    FID(["Sistema de\nFidelidade"])
    PAG(["Gateway de\nPagamento"])

    subgraph SIS ["Sistema de Autoatendimento"]
        direction TB
        UC1(["Montar Pedido"])
        UC2(["Realizar Pagamento"])
        UC3(["Visualizar Pedido\nna Cozinha"])
        UC4(["Atualizar\nFidelidade"])
    end

    CL --> UC1
    CL --> UC2
    CZ --> UC3
    UC1 -.->|include| UC3
    UC2 -.->|include| UC4
    UC2 --> PAG
    UC4 --> FID
```

---

## Cenário 3 — Sistema de Telemedicina

**Diagrama:** Sequência

```mermaid
sequenceDiagram
    participant S as Sensor
    participant A as App Mobile
    participant SV as Servidor
    participant M as Tablet Medico

    S->>A: enviarDados(bpm, ritmo)
    A->>A: analisarDados()

    alt alteracao detectada
        A->>SV: solicitarHistorico(idPaciente)
        SV-->>A: historico[]
        SV->>M: dispararAlerta(idPaciente, dados)
        M-->>SV: alertaRecebido: ok
    else dados normais
        A->>A: registrarLeitura()
    end
```

---

## Cenário 4 — Controle de Acesso Inteligente

**Diagrama:** Atividades com Swimlanes

```mermaid
flowchart TD
    subgraph USR ["Usuário"]
        A([Aproxima o celular])
        Z([Fim])
    end

    subgraph APP ["Aplicativo"]
        B[Capturar ID do dispositivo]
        C[Enviar requisicao de validacao]
        D{Reserva ativa?}
        E[Exibir acesso negado]
        H[Exibir acesso liberado]
    end

    subgraph HW ["Hardware"]
        F[Receber comando]
        G[Destrancar fechadura]
        I[Registrar log de acesso]
    end

    A --> B
    B --> C
    C --> D
    D -- Nao --> E
    E --> Z
    D -- Sim --> F
    F --> G
    G --> I
    I --> H
    H --> Z
```

---

## Cenário 5 — Marketplace de Serviços Domésticos

**Diagrama:** Casos de Uso com include e extend

```mermaid
flowchart LR
    CL(["Cliente"])
    PR(["Profissional"])
    PAG(["Sistema de\nPagamento"])

    subgraph SIS ["Marketplace de Servicos"]
        direction TB
        UC1(["Buscar\nProfissional"])
        UC2(["Filtrar por\nLocalizacao"])
        UC3(["Filtrar por\nDisponibilidade"])
        UC4(["Contratar\nServico"])
        UC5(["Processar\nPagamento"])
        UC6(["Avaliar\nProfissional"])
        UC7(["Gerenciar\nAgenda"])
    end

    CL --> UC1
    CL --> UC4
    PR --> UC7

    UC1 -.->|include| UC2
    UC1 -.->|include| UC3
    UC4 -.->|include| UC5
    UC4 -.->|extend| UC6

    UC5 --> PAG
```

> `include` — execucao obrigatoria do caso de uso base  
> `extend` — execucao condicional ou opcional

---

## Referência

> SOMMERVILLE, I. **Engenharia de software**. 10. ed. São Paulo: Pearson.
