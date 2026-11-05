# Desejos das Partes Interessadas — Priorização MoSCoW

**EEL873 — Engenharia de Software (UFRJ, 2026/2) · Grupo F · Projeto: Sistema de Gestão do Rancho Aroeira**
**Grupo:** João Paulo Garcia · Gabriel dos Santos Percu Saldanha · Henrique Gebara · Danilo Santiago Baptista

As partes interessadas são as **12 identificadas na tarefa T1** (planilha de partes interessadas, com as classificações de poder, influência, PLU, interesse e engajamento). Para cada uma foram levantados **5 desejos** em relação ao software, por conversas com o dono e observação da operação no salão e na cozinha. Cada desejo foi então classificado pelo método **MoSCoW**, do ponto de vista do que o sistema deve entregar.

**Legenda:** **M** = *Must have* (obrigatório) · **S** = *Should have* (importante) · **C** = *Could have* (desejável, se houver tempo) · **W** = *Won't have this time* (fora desta versão).

> Nas partes interessadas que **não usam** o sistema (fisco, ANPD, fornecedores, concorrentes, usuários mal-intencionados), a classificação diz se o sistema vai **atender** àquele desejo. Para os **usuários mal-intencionados**, o desejo é algo que o sistema deve **impedir**: o desejo em si fica como **W**, e o requisito de proteção correspondente aparece na consolidação.

---

## 1. Desejos por parte interessada

### 1.1. Proprietário (patrocinador) — João José de Assis Rangel
*T1: poder e influência ALTO · PLU ALTO/ALTO/ALTO · interesse ALTO · LIDERA*

| # | Desejo | MoSCoW |
|---|---|---|
| P1 | Ver as **mesas do salão em tempo real**: ocupadas, o que cada uma pediu e o que está pendente na cozinha | **M** |
| P2 | **Fechar a conta no caixa** com a taxa de serviço de 10% (opcional para o cliente) e a forma de pagamento | **M** |
| P3 | Guardar o **histórico de todas as vendas** e exportá-lo em planilha para analisar depois | **M** |
| P4 | Ver **KPIs do dia, da semana, do mês e do ano**: faturamento, ticket médio, formas de pagamento e meta diária | **S** |
| P5 | Calcular a **divisão dos 10% entre a equipe**, controlar o **estoque** e divulgar a casa num **site** | **S** |

### 1.2. Desenvolvedores / gerentes do projeto — Grupo F
*T1: poder MÉDIO · influência ALTO · interesse ALTO · LIDERA*

| # | Desejo | MoSCoW |
|---|---|---|
| D1 | Ter **acesso à operação real** (dono, garçons e cozinha) para levantar e validar os requisitos | **M** |
| D2 | **Infraestrutura com custo próximo de zero** (hospedagem e banco de dados em nuvem, em planos gratuitos) | **M** |
| D3 | Um **cardápio cadastrado num lugar só**, usado igualmente pelo garçom, pela cozinha e pelo cliente | **S** |
| D4 | **Publicar versões novas sem parar a casa**, fora do horário de funcionamento (sexta a domingo, 11h30–15h30) | **S** |
| D5 | **Backup automático** do banco de dados | **S** |

### 1.3. Garçons
*T1: poder BAIXO · influência MÉDIO · interesse ALTO · NEUTRO*

| # | Desejo | MoSCoW |
|---|---|---|
| G1 | **Lançar o pedido pelo celular** na mesa e mandá-lo direto para a cozinha e o bar | **M** |
| G2 | Marcar o **ponto da carne** e os **acompanhamentos** escolhendo em listas, sem escrever | **M** |
| G3 | Ver de relance quais **mesas estão livres, ocupadas ou aguardando pagamento** | **M** |
| G4 | Receber a **comissão dos 10%** calculada corretamente | **S** |
| G5 | Lançar **item avulso** e corrigir a comanda quando o cliente muda de ideia | **S** |

### 1.4. Equipe da cozinha
*T1: poder BAIXO · influência MÉDIO · interesse MÉDIO · APÓIA*

| # | Desejo | MoSCoW |
|---|---|---|
| K1 | Ver os pedidos **numa tela, em ordem de chegada**, aparecendo sozinhos assim que são enviados | **M** |
| K2 | Ler com clareza o **ponto da carne** e os **acompanhamentos** | **M** |
| K3 | Ver **só o que é da cozinha** (bebidas vão para o bar) | **M** |
| K4 | Ser **avisada por som** quando chega um pedido novo | **S** |
| K5 | Ver **há quanto tempo cada pedido espera** e marcar o prato como pronto | **S** |

### 1.5. Clientes do salão
*T1: poder BAIXO · influência BAIXO · interesse MÉDIO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| C1 | Ver o **cardápio com preços** pelo celular, lendo o QR code da mesa | **S** |
| C2 | **Pedir pelo próprio celular**, sem esperar o garçom no horário de pico | **S** |
| C3 | **Acompanhar a comanda da mesa** e o total, mesmo com vários celulares na mesma mesa | **S** |
| C4 | **Pedir por voz**, falando como falaria ao garçom, com a IA perguntando quando houver dúvida | **C** |
| C5 | Deixar um **recado anônimo** (elogio, crítica ou sugestão) para o dono | **C** |

### 1.6. Público do site (clientes em potencial)
*T1: poder BAIXO · influência BAIXO · interesse BAIXO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| S1 | Saber **se a casa está aberta agora** e o horário de funcionamento | **S** |
| S2 | Saber **como chegar** pela BR-356 (km 174) | **S** |
| S3 | Ver o **cardápio e os preços** antes de ir | **S** |
| S4 | **Reservar mesa** ou pedir **orçamento de evento** sem precisar ligar | **C** |
| S5 | Conhecer a **história da casa** e o **lazer** do terreno | **C** |

### 1.7. Fornecedores de insumos
*T1: poder BAIXO · influência BAIXO · interesse BAIXO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| F1 | Receber os **pedidos de reposição com antecedência** | **C** |
| F2 | Receber os pedidos nas **quantidades corretas**, sem faltar nem sobrar | **C** |
| F3 | Que o restaurante saiba **o que está acabando** antes de faltar (estoque com nível mínimo) | **S** |
| F4 | **Compras regulares**, previsíveis a partir do histórico de consumo | **C** |
| F5 | Fazer pedidos e cotações por um **portal integrado** ao sistema | **W** |

### 1.8. Fornecedores de tecnologia (nuvem) — hospedagem e banco de dados
*T1: poder BAIXO (organização) / MÉDIO (PLU) · influência MÉDIO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| N1 | Uso **dentro dos limites** do plano gratuito (requisições, armazenamento) | **M** |
| N2 | Uso **dentro dos termos de serviço** | **M** |
| N3 | Acesso ao banco **com autenticação** e chaves secretas protegidas | **M** |
| N4 | **Monitoramento** do consumo para não ser surpreendido por bloqueio | **S** |
| N5 | Converter o uso gratuito em **assinatura paga** | **W** |

### 1.9. Órgãos fiscais — SEFAZ-RJ e Receita Federal
*T1: poder ALTO · influência BAIXO · PLU ALTO/ALTO/BAIXO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| R1 | **Toda venda registrada**, sem venda "por fora" | **M** |
| R2 | Valores **coerentes** entre o caixa e o histórico (taxa de serviço tratada de forma consistente) | **M** |
| R3 | Registro da **forma de pagamento** de cada venda | **M** |
| R4 | Histórico **guardado pelo prazo legal** e exportável para o contador | **S** |
| R5 | **Emissão de nota fiscal eletrônica** pelo próprio sistema | **W** |

### 1.10. Órgão de proteção de dados — ANPD (LGPD)
*T1: poder ALTO · influência BAIXO · PLU ALTO/ALTO/BAIXO · DESCONHECE*

| # | Desejo | MoSCoW |
|---|---|---|
| L1 | Coletar **só os dados necessários** de clientes (nome e contato na reserva ou no orçamento) | **M** |
| L2 | Dados de clientes e logins da equipe **protegidos** (acesso só com autenticação) | **M** |
| L3 | Recados **realmente anônimos**: nenhum dado que identifique o autor | **S** |
| L4 | **Prazo de retenção** definido para os dados pessoais | **S** |
| L5 | Se houver gravação de **voz** do cliente, aviso claro e descarte após o uso | **C** |

### 1.11. Usuários mal-intencionados (classe desfavorecida)
*T1: PLU MÉDIO/BAIXO/ALTO ("perigoso") · DESCONHECE — desejos que o sistema deve IMPEDIR*

| # | Desejo (a impedir) | MoSCoW | Requisito de proteção |
|---|---|---|---|
| X1 | Fazer **pedido falso** de uma mesa onde não está | **W** | Só pede pelo QR quem está na mesa (QR assinado e sessão por mesa) — **M** |
| X2 | **Alterar o preço** de um item no pedido | **W** | O servidor recalcula o preço pelo cardápio; o celular nunca envia preço — **M** |
| X3 | **Ver a comanda de outras mesas** | **W** | Cada mesa vê só a própria comanda — **M** |
| X4 | **Encher a cozinha** de pedidos ou abusar do pedido por voz | **W** | Limite de pedidos e de falas por mesa — **S** |
| X5 | Mandar **spam** de recados | **W** | Limite de recados por origem — **S** |

### 1.12. Concorrentes locais — churrascarias e quiosques da região
*T1: tudo BAIXO · DESCONHECE (recebem valor negativo do projeto)*

| # | Desejo | MoSCoW |
|---|---|---|
| O1 | **Manter a própria clientela**, sem perdê-la para o atendimento mais ágil do Rancho | **W** |
| O2 | Que o Rancho **não apareça** nas buscas e mapas da região | **W** |
| O3 | **Conhecer os preços** do Rancho para se posicionar | **W** (o cardápio público é escolha do dono) |
| O4 | Que o Rancho **não divulgue** o lazer e os eventos, que são diferenciais | **W** |
| O5 | **Copiar a ideia** do sistema | **W** |

---

## 2. Classificação MoSCoW consolidada

### Must have — sem isto o sistema não substitui o papel

| Desejo | Partes interessadas |
|---|---|
| Lançar pedido pelo celular e enviá-lo à cozinha e ao bar | Garçons (G1) |
| Ponto da carne e acompanhamentos em listas, legíveis na cozinha | Garçons (G2), Cozinha (K2) |
| Monitor da cozinha em tempo real, em ordem de chegada, só com itens da cozinha | Cozinha (K1, K3) |
| Situação das mesas para o garçom e para o dono | Garçons (G3), Proprietário (P1) |
| Fechamento da conta com taxa de serviço e forma de pagamento; toda venda registrada | Proprietário (P2), Fisco (R1, R2, R3) |
| Histórico de vendas exportável | Proprietário (P3) |
| Proteção do pedido pelo QR: sessão por mesa, preço calculado no servidor, comanda só da própria mesa | Mal-intencionados (X1, X2, X3) |
| Autenticação da equipe e proteção dos dados pessoais | ANPD (L1, L2), Fornecedores de tecnologia (N3) |
| Custo próximo de zero, dentro dos limites e termos dos planos gratuitos | Desenvolvedores (D2), Fornecedores de tecnologia (N1, N2) |
| Acesso à operação real para validar os requisitos | Desenvolvedores (D1) |

### Should have — importante, mas a operação básica funciona sem

| Desejo | Partes interessadas |
|---|---|
| KPIs do dia, semana, mês e ano | Proprietário (P4) |
| Divisão dos 10% e comissão correta; estoque com nível mínimo | Proprietário (P5), Garçons (G4), Fornecedores de insumos (F3) |
| Item avulso e correção da comanda | Garçons (G5) |
| Alerta sonoro e tempo de espera na cozinha | Cozinha (K4, K5) |
| Cardápio, pedido e comanda pelo QR code da mesa | Clientes do salão (C1, C2, C3) |
| Site com horário, rota e cardápio | Público do site (S1, S2, S3), Proprietário (P5) |
| Cardápio único, publicação sem parar a casa, backup automático | Desenvolvedores (D3, D4, D5) |
| Histórico guardado e exportável para o contador; prazo de retenção | Fisco (R4), ANPD (L4) |
| Recados realmente anônimos; limites contra abuso e spam | ANPD (L3), Mal-intencionados (X4, X5) |
| Monitoramento do consumo da nuvem | Fornecedores de tecnologia (N4) |

### Could have — desejável, se houver tempo

| Desejo | Partes interessadas |
|---|---|
| Pedido por voz com IA, com aviso e descarte do áudio | Clientes do salão (C4), ANPD (L5) |
| Recados anônimos | Clientes do salão (C5) |
| Reservas e orçamento de eventos pelo site | Público do site (S4) |
| Página da história e do lazer | Público do site (S5) |
| Pedidos de reposição planejados a partir do histórico | Fornecedores de insumos (F1, F2, F4) |

### Won't have — fora desta versão

| Item | Motivo |
|---|---|
| Nota fiscal eletrônica pelo sistema | Exige integração com a SEFAZ e certificado digital; continua no processo atual (R5) |
| Portal para fornecedores | Fora do objetivo, que é a operação do salão (F5) |
| Assinatura paga de nuvem | O orçamento exige planos gratuitos nesta versão (N5) |
| Desejos dos mal-intencionados | São bloqueados pelos requisitos de proteção (X1–X5) |
| Desejos dos concorrentes | Não são atendidos; representam o valor negativo do projeto (O1–O5) |
| Pagamento online, delivery/retirada e aplicativo instalável | Mudariam o modelo de operação da casa ou contrariam a simplicidade exigida |

## 3. Critérios usados na priorização

- **Must** é o caminho que a proposta inicial pede e que tira a operação do papel — *garçom → cozinha → caixa → histórico* —, mais as **restrições** que não se negociam: segurança contra fraude no pedido, proteção de dados (LGPD), registro de toda venda (fisco) e custo zero de infraestrutura.
- **Should** são ganhos que dependem do núcleo pronto (os indicadores dependem do histórico; o pedido pelo QR depende do monitor da cozinha) ou que reduzem riscos operacionais (backup, limites contra abuso).
- **Could** são diferenciais. O **pedido por voz** é o mais inovador, mas depende de um serviço de IA, tem custo por uso, exige cuidado com dados de voz e precisa de testes com falas reais — por isso vem depois do pedido pelo QR, que resolve a mesma necessidade com toque.
- **Won't** são desejos fora do objetivo desta versão, e os desejos das partes interessadas **negativas** (mal-intencionados e concorrentes), que o sistema não atende por definição.
- A **planilha T1** orientou o peso de cada parte interessada: o proprietário (ALTO em tudo, LIDERA) define o núcleo; os garçons (interesse ALTO, NEUTRO) têm os desejos operacionais como Must, para que passem a apoiar; fisco e ANPD (poder ALTO, influência BAIXA) não pedem funcionalidades, mas impõem restrições obrigatórias.
