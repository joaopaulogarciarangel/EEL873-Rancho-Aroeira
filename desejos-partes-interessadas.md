# Desejos das Partes Interessadas — Priorização MoSCoW

**EEL873 — Engenharia de Software (UFRJ, 2026/2) · Grupo F · Projeto: Sistema de Gestão do Rancho Aroeira**

Levantamento feito por conversas com o dono e observação da operação no salão e na cozinha. Para cada **usuário** do sistema foram registrados **5 desejos** em relação ao software. Em seguida, todos os desejos foram classificados pelo método **MoSCoW**.

**Legenda:** **M** = *Must have* (obrigatório) · **S** = *Should have* (importante) · **C** = *Could have* (desejável, se houver tempo) · **W** = *Won't have this time* (fora desta versão).

---

## 1. Usuários considerados

| Usuário | Quem é | Como usa o sistema |
|---|---|---|
| Proprietário / gestor | Dono do Rancho | Painel de gestão, caixa, relatórios |
| Garçons | Equipe do salão | App no celular para lançar pedidos e fechar contas |
| Equipe da cozinha | Cozinheiros | Monitor com os pedidos a preparar |
| Clientes do salão | Quem almoça na casa | Cardápio e pedido pelo celular da mesa (QR code) |
| Público do site | Clientes em potencial | Site com cardápio, horário, localização e reservas |

As demais partes interessadas identificadas na tarefa anterior (fornecedores, órgãos fiscais, ANPD, concorrentes) **não usam** o sistema e por isso não entram nesta classificação.

## 2. Desejos por usuário

### 2.1. Proprietário / gestor

| # | Desejo | MoSCoW |
|---|---|---|
| P1 | Ver as **mesas do salão em tempo real**: quais estão ocupadas, o que cada uma pediu e o que está pendente na cozinha | **M** |
| P2 | **Fechar a conta no caixa** com a taxa de serviço de 10% (opcional para o cliente) e a forma de pagamento (Pix, cartão, dinheiro) | **M** |
| P3 | Guardar o **histórico de todas as vendas** e exportá-lo em planilha para analisar depois | **M** |
| P4 | Ver **KPIs do dia, da semana, do mês e do ano**: faturamento, ticket médio, vendas por forma de pagamento e meta diária | **S** |
| P5 | Calcular a **divisão da taxa de 10% entre a equipe** e controlar o **estoque** de insumos | **S** |

### 2.2. Garçons

| # | Desejo | MoSCoW |
|---|---|---|
| G1 | **Lançar o pedido pelo celular** na mesa e mandar direto para a cozinha, sem andar com papel | **M** |
| G2 | Marcar o **ponto da carne** e os **acompanhamentos** sem precisar escrever, escolhendo em listas | **M** |
| G3 | Ver de relance quais **mesas estão livres, ocupadas ou aguardando pagamento** | **M** |
| G4 | Lançar um **item avulso** (algo fora do cardápio) com nome e preço | **S** |
| G5 | Corrigir ou retirar um item da comanda quando o cliente muda de ideia | **S** |

### 2.3. Equipe da cozinha

| # | Desejo | MoSCoW |
|---|---|---|
| K1 | Ver os pedidos **numa tela, em ordem de chegada**, aparecendo sozinhos assim que o garçom ou o cliente envia | **M** |
| K2 | Ler com clareza o **ponto da carne** e os **acompanhamentos** de cada prato | **M** |
| K3 | Ver **só o que é da cozinha** (bebidas vão para o bar) | **M** |
| K4 | Ser **avisada por som** quando chega um pedido novo | **S** |
| K5 | Ver **há quanto tempo cada pedido espera**, com destaque para os atrasados, e marcar como pronto | **S** |

### 2.4. Clientes do salão

| # | Desejo | MoSCoW |
|---|---|---|
| C1 | Ver o **cardápio com preços** pelo celular, lendo o QR code da mesa | **S** |
| C2 | **Fazer o pedido pelo próprio celular**, sem esperar o garçom no horário de pico | **S** |
| C3 | **Acompanhar a comanda da mesa** e o total a qualquer momento, inclusive com vários celulares na mesma mesa | **S** |
| C4 | **Pedir por voz**, falando o pedido como falaria ao garçom, com a IA perguntando quando houver dúvida | **C** |
| C5 | Deixar um **recado anônimo** (elogio, crítica ou sugestão) para o dono | **C** |

### 2.5. Público do site

| # | Desejo | MoSCoW |
|---|---|---|
| S1 | Saber **se a casa está aberta agora** e o horário de funcionamento | **S** |
| S2 | Saber **como chegar** (rota até o local na rodovia) | **S** |
| S3 | Ver o **cardápio e os preços** antes de ir | **S** |
| S4 | **Reservar mesa** ou pedir **orçamento de evento** sem precisar ligar | **C** |
| S5 | Conhecer a **história da casa** e o **lazer** do terreno (espaço kids, pescaria, animais, cavalo) | **C** |

## 3. Classificação MoSCoW consolidada (todos os usuários)

### Must have — sem isto o sistema não substitui o papel

| Desejo | Usuários |
|---|---|
| Lançar pedido pelo celular e enviá-lo à cozinha | Garçons (G1) |
| Ponto da carne e acompanhamentos escolhidos em listas e legíveis na cozinha | Garçons (G2), Cozinha (K2) |
| Monitor da cozinha com os pedidos em tempo real, em ordem de chegada | Cozinha (K1) |
| Separação cozinha × bar | Cozinha (K3) |
| Situação das mesas: para o garçom (livre, ocupada, aguardando pagamento) e para o dono (pedidos e pendências) | Garçons (G3), Proprietário (P1) |
| Fechamento da conta com taxa de serviço e forma de pagamento | Proprietário (P2) |
| Histórico de vendas exportável | Proprietário (P3) |

### Should have — importante, mas a operação básica funciona sem

| Desejo | Usuários |
|---|---|
| KPIs do dia, semana, mês e ano | Proprietário (P4) |
| Divisão da taxa de 10% e controle de estoque | Proprietário (P5) |
| Item avulso e correção da comanda | Garçons (G4, G5) |
| Alerta sonoro e tempo de espera na cozinha | Cozinha (K4, K5) |
| Cardápio, pedido e comanda pelo QR code da mesa | Clientes (C1, C2, C3) |
| Site com horário, rota e cardápio | Público (S1, S2, S3) |

### Could have — desejável, se houver tempo

| Desejo | Usuários |
|---|---|
| Pedido por voz com IA | Clientes (C4) |
| Recados anônimos | Clientes (C5) |
| Reservas e orçamento de eventos pelo site | Público (S4) |
| Página da história e do lazer | Público (S5) |

### Won't have — fora desta versão

| Item | Motivo |
|---|---|
| Emissão de nota fiscal eletrônica pelo sistema | Exige integração com a Secretaria de Fazenda e certificado digital; continua no processo atual |
| Pagamento online pelo celular do cliente | O pagamento segue no caixa; evita taxas e estornos |
| Delivery e retirada no local | A casa trabalha com almoço no salão; não há operação de entrega |
| Aplicativo para instalar | Tudo funciona no navegador do celular, sem instalação |

## 4. Critérios usados na priorização

- **Must** é o que a **proposta inicial** pede e o que tira a operação do papel: o caminho *garçom → cozinha → caixa → histórico*. Se faltar qualquer elo, a casa volta às comandas escritas.
- **Should** são ganhos claros que dependem do núcleo pronto: os indicadores dependem do histórico; o pedido pelo QR depende do monitor da cozinha.
- **Could** são diferenciais para o cliente. O **pedido por voz** é o mais inovador, mas depende de um serviço de IA, tem custo por uso e precisa de testes com falas reais antes de ir para o salão — por isso vem depois do pedido pelo QR, que já resolve a mesma necessidade com toque.
- **Won't** são pedidos plausíveis que mudariam o modelo de operação da casa ou exigiriam integrações caras para esta versão.
