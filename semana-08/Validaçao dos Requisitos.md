# Processo de Validação de Requisitos - Geraldo Store Manager

Após a elaboração do **SRS (Software Requirements Specification)**, realizei uma reunião de validação com o cliente (Sr. Geraldo) para garantir que todos os requisitos funcionais e o escopo do sistema estivessem alinhados com as necessidades do negócio.

## Registro da Conversa de Validação

**Analista:** Olá, Sr. Geraldo! Com base na nossa primeira conversa, eu estruturei o documento de requisitos do seu sistema, o **Geraldo Store Manager**. Gostaria de validar os pontos principais com o senhor para garantir que estamos no caminho certo antes de iniciar o desenvolvimento.

**Sr. Geraldo:** Olá! Claro, vamos dar uma olhada. O que você planejou?

**Analista:** Foquei em resolver os problemas de estoque e organização. O sistema terá:
1. **Controle de Estoque Rígido:** O sistema impedirá vendas de produtos com estoque zerado e emitirá alertas quando um item estiver acabando.
2. **Vendas Multicanal:** O senhor poderá registrar se a venda veio da loja física, do WhatsApp ou do Instagram.
3. **Cadastro de Clientes:** Teremos um histórico completo de quem compra com o senhor para identificar seus melhores clientes.
4. **Relatórios Automáticos:** O senhor não precisará mais de cadernos; o sistema gerará relatórios de vendas por período e canal automaticamente.

**Sr. Geraldo:** Isso parece ótimo! Especialmente a parte de não vender o que não tenho no estoque e saber quem são meus clientes fiéis.

**Analista:** Perfeito. Também definimos o que **não** será feito agora para manter o sistema simples, como a emissão de notas fiscais e a integração direta com a API do WhatsApp. O foco é a gestão interna. O senhor está de acordo com esses termos?

**Sr. Geraldo:** Sim, para começar, essa organização é exatamente o que eu preciso. Pode seguir com o projeto!

---

## Conclusão da Etapa
Os requisitos foram validados e aprovados pelo cliente em **16/04/2026**. 
O projeto seguirá para a fase de **Design e Prototipagem**, conforme o cronograma estimado.

### Resumo dos Requisitos Validados:
* **Funcionais:** Módulos de Produtos, Estoque, Vendas, Clientes e Relatórios.
* **Não Funcionais:** Sistema responsivo (celular e PC), segurança com login/senha e alta performance.
* **Tecnologias:** React.js, Node.js e PostgreSQL.
