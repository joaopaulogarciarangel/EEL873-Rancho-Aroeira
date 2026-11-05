# Sistema de Gestão — Rancho Aroeira

**EEL873 — Engenharia de Software (UFRJ, 2026/2) · Grupo F**

Projeto de um sistema para apoiar a operação do **Rancho Aroeira**, um quiosque de churrascaria à beira da BR-356 (km 174, Curva de Grussaí, São João da Barra/RJ), especializado em **cortes servidos na pedra**: a carne chega selada numa pedra a 250–350 °C e o cliente finaliza no ponto que preferir. A casa abre **só no almoço, de sexta a domingo (11h30–15h30)**, tem **15 mesas** e um terreno com área de lazer (espaço kids, pescaria, animais e passeio a cavalo).

## Links

| O quê | Onde |
|---|---|
| Repositório | https://github.com/joaopaulogarciarangel/EEL873-Rancho-Aroeira |
| Página do projeto (GitHub Pages) | https://joaopaulogarciarangel.github.io/EEL873-Rancho-Aroeira/ |
| Proposta inicial informal | [seção abaixo](#1-proposta-inicial-informal) |
| Análise de valor (B2B e B2C) | [seção abaixo](#3-análise-de-valor) |
| Desejos das partes interessadas (MoSCoW) | [desejos-partes-interessadas.md](desejos-partes-interessadas.md) · [página](https://joaopaulogarciarangel.github.io/EEL873-Rancho-Aroeira/desejos.html) · [PDF](desejos-partes-interessadas.pdf) |
| Referência das pirâmides | Almquist, Senior e Bloch (2016) — [B2C](https://media.bain.com/elements-of-value/) · Almquist, Cleghorn e Sherer (2018) — [B2B](https://media.bain.com/b2b-eov/index.html) |

---

## 1. Proposta inicial informal

Texto enviado ao professor na abertura do trabalho:

> Boa noite, professor! Como deve estar aparecendo, esse é o grupo F. Um dos integrantes que sou eu (João Paulo Garcia) tem um pai que acabou de abrir um quiosque de churrascaria na beira da estrada. Sou de Campos dos Goytacazes e fica mais no interior ainda de campos, bem rústico e pouca tecnologia.
>
> Nisso, pensamos em desenvolver um sistema para que meu pai trabalhe melhor operacionalmente na churrascaria. Nesse sentido, o escopo seria fazer um sistema em que o garçom faça pedidos pelo celular e os pedidos fossem para um monitor da cozinha com os pratos que devem ser preparados. Isso porque atualmente é tudo feito a mão e no papel.
>
> Além disso, ter uma página de gerenciamento que tenha algumas seções como KPIs do dia/semana/mês/ano, uma seção de monitoramento das mesas do salão com os pedidos e comandas. Além de salvar o histórico de vendas para fazer análises posteriormente e extrair insights da operação.
>
> Isso pensando e abstraindo inicialmente, pode ser que o projeto se desenvolva mais ao ser produzido e com as possíveis necessidades do meu pai.

## 2. O problema e o sistema proposto

**Situação atual.** Comandas em papel: o garçom anota, leva à cozinha, a cozinha prepara pela ordem em que os papéis chegam e o caixa soma tudo à mão no fim. Os problemas típicos são comanda perdida ou ilegível, item esquecido, ponto da carne trocado, demora no pico do almoço, conta conferida item a item e **nenhum registro** das vendas para saber o que vende mais, em que dia e com que ticket médio.

**Partes do sistema** (o núcleo vem da proposta inicial; as extensões são as "possíveis necessidades" que a proposta já previa e que serão confirmadas com o dono ao longo do projeto):

| Parte | Quem usa | O que faz |
|---|---|---|
| **App do garçom** (núcleo) | Garçons | Abrir a mesa, lançar pedidos pelo celular (com ponto da carne e acompanhamentos), enviar à cozinha e ao bar, fechar a conta |
| **Monitor da cozinha** (núcleo) | Cozinha | Ver os pedidos em tempo real, em ordem de chegada, com alerta de pedido novo e tempo de espera; marcar como pronto |
| **Painel do gestor** (núcleo) | Dono / gestor | KPIs do dia, semana, mês e ano; mesas do salão com pedidos e comandas; caixa; histórico de vendas exportável para análise |
| Controle financeiro (extensão) | Dono | Taxa de serviço de 10% e sua divisão entre a equipe; estoque de insumos; demonstrativos semanais |
| Pedido do cliente pela mesa (extensão) | Clientes | QR code em cada mesa: o cliente vê o cardápio, pede pelo próprio celular e acompanha a comanda da mesa |
| Pedido por voz com IA (extensão) | Clientes | Na mesa, o cliente **fala ou escreve** o pedido em linguagem natural ("uma picanha para dois, ao ponto, com farofa e duas cocas"); uma IA interpreta a fala, monta os itens com tamanho, ponto e acompanhamentos, **pergunta quando o pedido é ambíguo** ("qual picanha?") e o cliente confirma antes de enviar à cozinha. A IA nunca define preço nem envia sozinha: os itens passam pelas mesmas regras do cardápio |
| Site público (extensão) | Clientes e público | Cardápio com preços, horário (aberto/fechado agora), como chegar, reservas, orçamento de eventos e um canal de recados anônimos |

**Restrições do contexto.** Equipe e clientes com **pouca familiaridade com tecnologia** (interface muito simples, sem instalar aplicativo), uso **pelo celular**, beira de estrada com **internet instável**, e **orçamento baixo** de uma empresa familiar recém-aberta — inclusive para a IA, que deve priorizar serviços com plano gratuito e ter limite de uso por mesa.

## 3. Análise de valor

A análise usa as duas pirâmides de **Elementos do Valor** apresentadas no Capítulo 4 do livro-texto:

- **B2B** (Almquist, Cleghorn e Sherer, 2018; 40 elementos): o software é "vendido" a uma **organização** — o próprio Rancho Aroeira, representado pelo dono e usado pela equipe.
- **B2C** (Almquist, Senior e Bloch, 2016; 30 elementos): as extensões voltadas ao **cliente do restaurante** (pedido pela mesa e site) entregam valor a **pessoas**.

Como o livro recomenda, não se marca a pirâmide inteira: foram escolhidos os elementos **mais importantes para este cliente**, com a justificativa de cada um. Os níveis vão da base (essencial) ao topo.

### 3.1. Pirâmide B2B — o Rancho Aroeira como cliente

**Compromissos básicos** *(table stakes — sem eles o sistema não é aceito)*

| Elemento | Por que foi escolhido |
|---|---|
| Satisfazer especificações | O garçom precisa lançar o pedido e ele precisa chegar à cozinha, sempre. Se falhar num sábado cheio, o sistema é abandonado e volta o papel |
| Preço aceitável | Empresa familiar recém-aberta: o sistema deve rodar com custo mensal próximo de zero (serviços de nuvem em planos gratuitos) e celulares que a equipe já tem |
| Conformidade regulatória | Reservas e recados guardam dados pessoais de clientes (LGPD); o histórico de vendas precisa bater com o caixa |

**Valor funcional**

| Elemento | Por que foi escolhido |
|---|---|
| Redução de custos | Menos pratos refeitos por erro de comanda, menos desperdício e menos tempo gasto somando contas à mão |
| Aumento de receitas | Mesa atendida mais rápido gira mais no almoço de 4 horas; nenhum item consumido fica fora da conta; o site e as reservas trazem clientes novos |
| Qualidade do produto | O ponto da carne e os acompanhamentos chegam à cozinha exatamente como o cliente pediu — numa casa de cortes na pedra, o ponto **é** o produto |
| Inovação | Pedido por voz com IA, que entende o jeito de falar do cliente, num quiosque de beira de estrada — algo raro mesmo em restaurantes grandes |

**Valor da facilidade de fazer negócios**

| Elemento | Por que foi escolhido |
|---|---|
| Poupar tempo | O pedido vai do celular do garçom ao monitor da cozinha sem ninguém andar até lá |
| Reduzir esforço | Fechar a conta vira um clique, com taxa de serviço e forma de pagamento já calculadas; no pico, o pedido por voz deixa o cliente pedir sozinho e o garçom fica livre para servir |
| Diminuir problemas | Fim da comanda perdida, ilegível ou esquecida — a principal dor da operação em papel |
| Informação | KPIs do dia, semana, mês e ano e o histórico de vendas: o dono passa a saber o que vende, quando e quanto |
| Transparência | O dono enxerga em tempo real as mesas abertas, o que cada uma pediu e o que está atrasado |
| Organização | Pedidos em ordem de chegada na cozinha, separados por setor (cozinha e bar) |
| Integração | Garçom, cozinha, caixa, estoque e relatórios trabalham sobre os mesmos dados, sem redigitar |
| Simplificação | Interface com poucos botões e linguagem do dia a dia, para uma equipe com pouca tecnologia; para o cliente, falar é mais simples que navegar num cardápio de 76 itens |
| Disponibilidade | Funciona no celular, sem instalar nada, de qualquer lugar — inclusive para o dono acompanhar de casa |
| Configurabilidade | Cardápio, preços e número de mesas ajustáveis sem mexer no código |
| Ajuste cultural | O sistema deve caber num quiosque rústico de beira de estrada, não exigir que a casa vire um restaurante de shopping |

**Valor individual**

| Elemento | Por que foi escolhido |
|---|---|
| Redução da ansiedade | O dono deixa de depender da memória e dos papéis para saber se cada mesa foi atendida e cobrada |
| Crescimento e desenvolvimento | A equipe aprende a trabalhar com ferramentas digitais simples, o que aumenta sua qualificação |

**Valor inspiracional**

| Elemento | Por que foi escolhido |
|---|---|
| Visão | O histórico de vendas permite antecipar tendências (dias e pratos mais vendidos, efeito do clima, sazonalidade) e decidir com dados |
| Esperança | Um negócio que acabou de abrir ganha estrutura para crescer sem perder o controle |

**Elementos não escolhidos (e por quê):** *escalabilidade* e *alcance* — é uma casa só, de 15 mesas, sem plano de rede; *expansão da rede* e *marketability* (carreira) — não se aplicam a um negócio familiar; *responsabilidade social* — o sistema não tem impacto social direto além do próprio negócio.

### 3.2. Pirâmide B2C — o cliente do restaurante

**Valor funcional**

| Elemento | Por que foi escolhido |
|---|---|
| Poupar tempo | Pedir pelo celular da mesa sem esperar o garçom passar, no horário de pico — falando o pedido inteiro de uma vez |
| Informar | Cardápio com fotos e preços, horário com aviso de "aberto agora", rota até o local na rodovia e a comanda da mesa sempre visível |
| Reduzir esforço | Pedir **por voz**, sem procurar item por item no cardápio — importante para quem tem pouca familiaridade com celular; reservar mesa ou pedir orçamento pelo site, sem ligar |
| Evitar problemas | O pedido chega à cozinha como o cliente escolheu (ponto e acompanhamentos), e a conta não traz surpresas |
| Variedade | O cardápio completo à mão, com tamanhos (para 2 ou para 4) e acompanhamentos, ajuda a escolher |
| Conectar com outras pessoas | Mesa com vários celulares compartilha uma só comanda — a família pede junta |

**Valor emocional**

| Elemento | Por que foi escolhido |
|---|---|
| Reduzir ansiedade | Ver a comanda da mesa e o total a qualquer momento; deixar um recado anônimo sem constrangimento |
| Design e estética | O site e o cardápio digital transmitem a identidade rústica da casa (pedra, brasa, aroeira) |
| Diversão e entretenimento | Conversar com um atendente virtual que entende o pedido é uma novidade divertida na mesa; o site mostra o lazer do terreno (espaço kids, pescaria, animais, cavalo), que faz parte da experiência do almoço |

**Valor de mudança de vida**

| Elemento | Por que foi escolhido |
|---|---|
| Afiliação e pertencimento | A página da história da casa (uma família, um terreno à beira da estrada) aproxima o cliente de um negócio familiar do interior |

**Impacto social:** não foi escolhido — o sistema não tem efeito sobre a sociedade além dos clientes e da própria casa.

**Elementos não escolhidos (e por quê):** *fazer dinheiro* e *reduzir custo* para o cliente — o preço do prato não muda com o sistema; *integrar* e *organizar* a vida do cliente — o uso é pontual, durante o almoço; *nostalgia*, *status*, *bem-estar* e *valor terapêutico* — vêm da experiência no restaurante, não do software.

## 4. Próximos passos

Elicitação de requisitos com o dono e a equipe, testes do pedido por voz com falas reais de clientes, histórias do usuário, casos de uso, modelagem do processo de atendimento em BPMN e priorização das extensões pelo método MoSCoW. Este repositório será atualizado a cada entrega da disciplina.
