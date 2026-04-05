# Estudos de Judô com NotebookLM

Este repositório documenta a criação de um **caderno temático no NotebookLM** para apoiar meus estudos de **Judô**, organizando fontes abertas, registrando experimentos de prompts (incluindo erros e acertos) e consolidando um **miniguia final** para revisão e evolução contínua.

---

## 1) Contexto e Objetivos

### Contexto
O Judô é uma arte marcial e esporte olímpico com forte base técnica, tática, física e filosófica. A curva de aprendizado costuma ser acelerada quando o estudo é estruturado em torno de:
- **Fundamentos** (postura, pegadas, deslocamento, desequilíbrio)
- **Técnicas** (nage-waza e ne-waza)
- **Regras e arbitragem**
- **Treinamento e periodização**
- **Análise de lutas e tomada de decisão**

### Objetivos deste caderno temático
1. **Entender e revisar fundamentos técnicos** (por que uma técnica funciona, quando usar, erros comuns).
2. **Construir repertório de estudo** por categoria (quedas, transições, imobilizações, estrangulamentos, chaves).
3. **Aprimorar leitura tática** (kumi-kata, kuzushi, direção de ataque, combos e contra-ataques).
4. **Criar um conjunto de prompts reutilizáveis** para revisões rápidas antes/depois de treinos.
5. **Registrar “cicatrizes” de prompt engineering**: o que funcionou, o que falhou e como ajustar.

> **Escopo (importante):** este material é focado em estudo e revisão. Para técnicas e segurança, a prática deve ser acompanhada por um(a) professor(a) qualificado(a).

---

## 2) Curadoria de Fontes
A seguir está uma lista de fontes locais utilizadas neste estudo:
- [Apostila de Judô LIPEJU 2024](fontes/Apostila-de-judo-LIPEJU-2024.pdf)
- [apostilajudo.pdf](fontes/apostilajudo.pdf)
- [handbook.pdf](fontes/handbook.pdf)
- [judoinaction0000kudo.pdf](fontes/judoinaction0000kudo.pdf)
- [Judo Kodokan - Jigoro Kano](https://judomangueira.com.br/wp-content/uploads/2020/04/JUDO-KODOKAN-Jigoro-Kano_.pdf)

---

## 3) Engenharia de Prompts e “Cicatrizes” (Experimentos + Troubleshooting)

Nesta seção eu registro:
- **Perguntas estratégicas**
- **Variações de prompts testadas**
- **Resultados e referências**
- **Dificuldades encontradas** e como corrigi

> OBS: quanto mais específico o prompt (técnica + situação + objetivo + restrições), melhor a qualidade.

### 3.1 Perguntas estratégicas (o que eu queria extrair do NotebookLM)
- Quais são os **princípios** por trás de *kuzushi* aplicados às técnicas mais comuns?
- Quais são os **erros mais frequentes** em determinadas projeções e como corrigi-los?
- Como montar **combinações (renraku-waza)** e **contra-ataques (kaeshi-waza)** a partir do kumi-kata?
- Quais são as **regras atuais** que mais impactam estratégias de competição?
- Como transformar o conteúdo em um **plano de estudo semanal**?

---

### 3.2 Prompts testados (com variações)

#### Prompt A — Resumo técnico estruturado por técnica
**Versão 1 (genérica)**
- “Explique o Seoi-nage.”

**Problema (“cicatriz”)**
- Resposta superficial, pouco aplicável ao treino:
  
O **Seoi-nage**, traduzido como *arremesso pelo ombro e braço* (ou “arremesso carregando nas costas”), é uma das técnicas mais importantes e fundamentais do Judô. É classificada como uma **Te-waza** (técnica de braço/mão) e faz parte da **primeira série (Dai Ikkyo)** do **Gokyo** (sistema oficial de classificação de projeções da Kodokan).

**Princípio (visão geral)**
- O princípio básico é **desequilibrar o oponente para a frente** (ou para a **diagonal frontal direita**), **posicioná-lo sobre as costas** e **arremessá-lo por cima do ombro**.

**Variações principais**
- **Morote Seoi-nage** (duas mãos): mantém pegada na **manga** e na **lapela**; o **cotovelo** do braço que segura a lapela entra sob a **axila** do oponente para “carregar”.
- **Ippon Seoi-nage** (um braço e o ombro): o braço do oponente é segurado por dentro e “preso” contra o ombro do praticante. *(Observação: na listagem oficial da Kodokan, pode aparecer separado como parte do “extra gokyo”.)*
- **Eri Seoi-nage** (ou **Eri Ippon Seoi-nage**): aplicado segurando a **lapela** (ou manga) do **lado contrário**.

**Fases da execução (tríade clássica)**
- **Kuzushi (desequilíbrio):** puxar o oponente para a frente/diagonal frontal direita, levando o peso para os **dedos dos pés**.
- **Tsukuri (preparação/posicionamento):** girar o corpo para a esquerda, posicionando as **costas contra o peito** do adversário; dobrar os **joelhos** para baixar o centro de gravidade.
- **Kake (finalização/arremesso):** esticar as pernas e curvar o corpo para a frente, puxando com as mãos para baixo para projetar o oponente sobre o ombro.

**Versão 2 (melhorada)**
- “Com base nas fontes do notebook, faça um resumo técnico do *Ippon Seoi-nage* com:
  1) objetivo da técnica,
  2) pré-requisitos (kumi-kata e postura),
  3) etapas (kuzushi → tsukuri → kake),
  4) erros comuns e correções,
  5) variações seguras para treino.”

**O que melhorou**
- Estrutura consistente e foco em aplicação:
  
Com base nos fundamentos e manuais técnicos contidos nas fontes, o **Ippon Seoi-nage** (arremesso usando um braço e o ombro) é uma técnica de braço (**Te-waza**) essencial no Judô, classificada oficialmente como parte do **Extra Gokyo** da Kodokan e presente no **Nage-no-kata**.

Abaixo, o resumo técnico estruturado:

1) **Objetivo da técnica**
- Desequilibrar o oponente para a frente (ou diagonal frontal direita) e **posicioná-lo sobre as costas** para arremessá-lo por cima do **ombro direito**.

2) **Pré-requisitos (kumi-kata e postura)**
- **Postura (Shisei):** geralmente inicia em **Migi-shizentai** (postura natural à direita).
- **Pegada (Kumi-kata):**
  - Mão esquerda segura a parte interna da **manga direita** do oponente (*sode*).
  - A mão direita pode começar na lapela, mas deve ser **liberada** para entrar sob a **axila** do adversário durante a entrada.

3) **Etapas da execução (contínuas)**
- **Kuzushi (desequilíbrio):**
  - Puxar o oponente para a frente/diagonal frontal direita, forçando passo e levando o peso para a ponta dos pés.
  - Pode haver uma ação de “provocar reação” (ex.: empurrar levemente para trás e puxar quando ele avança), dependendo do contexto.
- **Tsukuri (posicionamento):**
  - Girar o corpo para a esquerda (pivô), apoiando-se nos dedos do pé direito.
  - Entrar o braço direito profundamente sob a axila direita do oponente, prendendo o braço dele contra o próprio ombro.
  - Baixar o centro de gravidade flexionando joelhos e encostar as costas no peito do oponente.
- **Kake (finalização):**
  - Estender as pernas com vigor e curvar o corpo à frente, puxando a manga para baixo (movimento em arco) para projetar o oponente sobre o ombro.

4) **Erros comuns e correções**
- **Erro de inclinação:** não curvar o tronco o suficiente para a frente.
  - **Consequência:** o peso do oponente pode cair sobre o cotovelo, aumentando risco de lesão.
  - **Correção:** inclinar bem o tronco e puxar as mãos em direção ao solo.
- **Entrada forçada do cotovelo:** tentar “enfiar” o cotovelo na axila sem o giro correto do pulso.
  - **Correção:** o pulso deve girar naturalmente para dentro para facilitar o encaixe.
- **Falta de controle pós-queda:** perder o equilíbrio após projetar.
  - **Correção:** buscar estabilizar em **Jigo-hontai** após a projeção, mantendo domínio do braço do adversário.

5) **Variações seguras para treino**
- **Morote Seoi-nage:** mantém duas mãos no judogi (manga e lapela), com cotovelo sob a axila.
- **Eri Seoi-nage (Eri Ippon Seoi-nage):** com pegada na lapela do lado contrário.
- **Seoi-otoshi:** variação em que Tori ajoelha um ou ambos joelhos para baixar ainda mais o centro de gravidade no tsukuri.

**Dica de treino**
- É fundamental que Uke execute **ukemi** corretamente, pois a projeção pode ter impacto considerável.

---

#### Prompt B — Comparação entre técnicas parecidas
**Versão 1**
- “Compare O-soto-gari e O-uchi-gari.”

**Versão 2 (melhorada)**
- “Compare *O-soto-gari* vs *O-uchi-gari* nas dimensões:
  - direção do desequilíbrio (kuzushi),
  - padrão de entrada (tsukuri),
  - riscos típicos de contra-ataque,
  - quando cada uma é mais indicada (situações de kumi-kata e movimento),
  - sinais de decisão (gatilhos durante a luta).
  Responda citando trechos/treinchos das fontes do notebook.”

**Cicatriz / troubleshooting**
- Quando eu não pedia “cite as fontes do notebook”, às vezes a IA generalizava demais.
- Solução: sempre incluir “**use apenas as fontes carregadas** e **cite referências**”.

---

#### Prompt C — Plano de estudo semanal
**Versão 1**
- “Monte um plano de estudo de judô.”

**Versão 2 (melhorada)**
- “Crie um plano de estudo de 4 semanas (3 sessões/semana, 30–45 min cada), com foco em:
  - fundamentos (kuzushi, kumi-kata, movimentação),
  - 2 técnicas de nage-waza por semana,
  - 1 tópico de ne-waza por semana,
  - 1 revisão de regras por semana,
  - exercícios de autoavaliação (checklist).
  Use somente as fontes do notebook e proponha prompts para cada sessão.”

**Cicatriz / troubleshooting**
- Plano ficou grande demais e difícil de executar.
- Solução: pedir **tempo por sessão**, **limite de itens**, e **entregáveis por sessão**.

---

### 3.3 Padrões que eu aprendi
- Pedir **estrutura** (itens numerados) melhora consistência.
- Incluir **contexto de situação** (treino vs competição, iniciantes vs intermediário) aumenta utilidade.
- Sempre pedir **referências** das fontes carregadas no NotebookLM.
- Definir **limites** (ex.: “máximo 10 bullets”) evita respostas longas demais.

---

## 4) Miniguia de Estudo (Entrega Final)

### 4.1 Resumos estruturados

#### Fundamentos essenciais (resumo + checklist)

**1) Postura (Shisei) — resumo**
- Objetivo: manter equilíbrio, mobilidade e prontidão para atacar/defender sem “entregar” o centro de gravidade.
- Pontos-chave:
  - Coluna alinhada e quadril “solto” (evitar rigidez).
  - Base estável, com peso distribuído para permitir deslocamento imediato.
  - Cabeça e olhar ativos (percepção de distância e timing).

**Checklist — Postura (shisei)**
- [ ] Minha base está estável (sem pés paralelos demais / sem “pé pesado”)  
- [ ] Consigo avançar/recuar/lateralizar sem cruzar as pernas  
- [ ] Meu centro de gravidade está baixo o suficiente para resistir a puxões  
- [ ] Não estou inclinado excessivamente para frente/trás  
- [ ] Mantenho postura mesmo sob disputa de pegada  

**2) Pegada (Kumi-kata) — resumo**
- Objetivo: criar **vantagem de alavancas** (controle de manga/lapela), limitar o ataque do adversário e abrir ângulos para kuzushi e entrada.
- Pontos-chave:
  - Não é “segurar forte”; é **segurar funcional** (mãos ativas, cotovelos bem posicionados).
  - Buscar controlar **manga** para matar ataque e **lapela/colarinho** para orientar direção.
  - A pegada deve conduzir ao próximo passo (kuzushi), e não existir “por si só”.

**Checklist — Pegada (kumi-kata)**
- [ ] Tenho um objetivo claro para a pegada (atacar qual técnica?)  
- [ ] Estou controlando pelo menos uma manga de forma efetiva  
- [ ] Minha pegada não me deixa quadrado(a) e sem mobilidade  
- [ ] Estou vencendo a disputa de postura/cotovelos (não “abraçando” o oponente)  
- [ ] Consigo alternar pegadas (plano A / plano B) sem travar o movimento  

**3) Desequilíbrio (Kuzushi) — resumo**
- Objetivo: deslocar o equilíbrio do oponente para um ponto onde ele tenha pouca capacidade de defesa/recuperação, facilitando o tsukuri e o kake.
- Pontos-chave:
  - Kuzushi é **direção + timing + reação** (não só puxar/empurrar).
  - Criar reação: induzir passo, travar uma perna, ou manipular tronco/ombros pela pegada.
  - Preferir desequilíbrios que alinhem com sua técnica-alvo (ex.: frente/diagonal para seoi; lateral/trás para técnicas de perna).

**Checklist — Kuzushi**
- [ ] Estou desequilibrando em uma direção compatível com a técnica que quero aplicar  
- [ ] Estou provocando passo/reação (em vez de “forçar” sem resposta)  
- [ ] Sinto o peso do oponente mudar (ponta do pé / calcanhar / lateral)  
- [ ] Minha cabeça e tronco permanecem estáveis (não me desequilibro junto)  
- [ ] O kuzushi acontece antes da entrada (não depois)  

**4) Entrada (Tsukuri) — resumo**
- Objetivo: posicionar corpo/quadril/braços de forma que o arremesso ou controle no solo se torne “natural” a partir do kuzushi criado.
- Pontos-chave:
  - Tsukuri deve ser **contínuo** (sem pausas entre kuzushi → entrada).
  - Ajuste de distância: perto o suficiente para encaixar, longe o suficiente para manter mobilidade.
  - Ângulo: entrar “no trilho” da técnica (não de frente quadrado(a) quando o ângulo pede diagonal/rotação).

**Checklist — Tsukuri**
- [ ] Minha entrada é contínua (sem duas etapas “travadas”)  
- [ ] Estou com a distância correta (nem colado(a) demais, nem longe)  
- [ ] Meus pés posicionam o quadril/ombros no ângulo certo  
- [ ] Meus joelhos flexionam para baixar o centro de gravidade quando necessário  
- [ ] Eu não perco a pegada/controle no meio da entrada  

**5) Execução (Kake) — resumo**
- Objetivo: finalizar a projeção (ou transição) com eficiência, mantendo controle e reduzindo risco de contra-ataque.
- Pontos-chave:
  - Kake é aceleração e finalização: **compromisso com a direção**.
  - Mãos e tronco “terminam” o movimento (não largar o controle no final).
  - Pós-técnica: recuperar base e já pensar na continuidade (imobilização / controle / retorno à postura).

**Checklist — Kake**
- [ ] Eu finalizo na direção certa (sem “meia força” ou mudança de rumo)  
- [ ] Mantenho controle do braço/pegada durante a queda  
- [ ] Consigo recuperar postura/base após a técnica  
- [ ] Evito girar de forma que ofereça as costas sem controle  
- [ ] Tenho uma continuação planejada (transição ou controle)  

**6) Transições para o solo (Nage → Ne-waza) — resumo**
- Objetivo: aproveitar o desequilíbrio/queda para estabelecer controle no chão (osaekomi) ou progredir para finalizações, antes que o oponente recupere a guarda/posição.
- Pontos-chave:
  - O melhor momento é “na queda”: não esperar estabilizar em pé para depois pensar no chão.
  - Manter pelo menos um controle-chave: braço, cabeça, quadril, ou linha dos ombros.
  - Priorizar posição dominante e estabilidade antes de buscar finalização.

**Checklist — Transições**
- [ ] Após o arremesso eu mantenho contato/controle (não “descolo”)  
- [ ] Eu caio/ajoelho em posição que favorece controle (sem me expor)  
- [ ] Tenho 1–2 transições padrão para cada técnica estudada  
- [ ] Minha primeira meta no chão é estabilizar (controle)  
- [ ] Sei quando parar e reiniciar (evitar “forçar” posição perdida)  

---

#### Nage-waza — resumos estruturados por técnica (modelos + exemplos)

**Molde por técnica**
**Técnica:** (ex.: O-soto-gari)  
- Objetivo:
- Quando usar (gatilhos):
- Kuzushi (direção + como provocar):
- Tsukuri (pés/quadril/ângulo):
- Kake (finalização):
- Erros comuns:
- Ajustes/correções:
- Combinações (renraku-waza) e continuação:
- Contra-ataques comuns (e prevenção):
- Segurança (ukemi / cuidado articular):

---

**Exemplo 1 — Ippon Seoi-nage (resumo operacional)**
- Objetivo: projetar para a frente/diagonal, carregando o oponente no ombro com controle de um braço.
- Quando usar (gatilhos):
  - Oponente com postura mais alta ou avançando.
  - Quando você consegue controlar uma manga e criar reação de passo para frente.
- Kuzushi:
  - Induzir avanço (provocar passo) e puxar para frente/diagonal, transferindo peso do uke.
- Tsukuri:
  - Giro e encaixe com costas no peito, braço entrando sob axila para “prender” o braço.
  - Baixar o centro com flexão de joelhos, alinhando quadril/ombro.
- Kake:
  - Estender pernas e finalizar com tronco à frente e controle da manga.
- Erros comuns:
  - Entrar sem kuzushi real; cotovelo mal encaixado; tronco pouco inclinado.
- Ajustes/correções:
  - Trabalhar kuzushi em passo; enfatizar giro contínuo; terminar puxando para baixo e à frente.
- Combinações e continuação:
  - Seoi-nage → transição para controle no chão (estabilizar braço).
- Contra-ataques comuns (e prevenção):
  - Defesa com base baixa e travas na pegada; prevenir com kuzushi + timing (sem “forçar entrada parada”).
- Segurança:
  - Uke com ukemi consistente; não jogar “em cima do cotovelo”; controlar o final do movimento.
    
---

**Exemplo 2 — O-soto-gari (resumo operacional)**
- Objetivo: projetar para trás/lateral, reapando a perna do uke com controle do tronco.
- Quando usar (gatilhos):
  - Uke com peso na perna atacada ou recuando linearmente.
  - Quando sua pegada consegue “abrir” o tronco do uke e travar recuperação.
- Kuzushi:
  - Direção para trás e levemente lateral, quebrando a postura e tirando o calcanhar do “chão forte”.
- Tsukuri:
  - Ajustar ângulo (não ficar quadrado), aproximar quadril e alinhar peito/ombros para dominar o eixo do uke.
- Kake:
  - Reapamento amplo e contínuo, com controle do tronco (não apenas “chutar a perna”).
- Erros comuns:
  - Atacar só a perna sem dominar o tronco; entrar longe; reapamento curto.
- Ajustes/correções:
  - Priorizar controle do tronco via pegadas; aproximar antes do reapamento; finalizar até o uke cair “limpo”.
- Combinações e continuação:
  - O-soto-gari → continuação para imobilização (passar para controle lateral, se encaixar).
- Contra-ataques comuns (e prevenção):
  - Contra com entrada por dentro (variações de inner reap) se você ficar quadrado(a); prevenir com ângulo e domínio do tronco.
- Segurança:
  - Cuidado com colisão de joelho; garantir que uke consiga cair com segurança.

---

#### Ne-waza — resumos estruturados por tema (modelos + exemplo)

**Molde por tema**
**Tema:** (ex.: Kesa-gatame e escapes)  
- Princípio:
- Pontos de controle (o que não pode “soltar”):
- Passo a passo (entrada → estabilização → progressão):
- Erros comuns:
- Escape 1 / Escape 2 (do uke) e como prevenir:
- Transições:
- Checklist (autoavaliação rápida):

---

**Exemplo — Osaekomi: Kesa-gatame (visão de estudo)**
- Princípio: controlar cabeça/ombros e impedir que o uke recupere quadril e gire para dentro.
- Pontos de controle:
  - Pressão do tronco e controle da linha dos ombros.
  - Controle de cabeça/braço (dependendo da variação estudada nas fontes).
- Passo a passo:
  - Entrada: chegar pela lateral após queda ou passagem.
  - Estabilização: ajustar base (joelhos/pés) e distribuir peso para impedir ponte e giro.
  - Progressão: procurar transições para outras imobilizações se o uke criar espaço.
- Erros comuns:
  - Ficar “alto(a)” e leve; base estreita; perder controle do braço.
- Escapes (do uke) e prevenção:
  - Escape por ponte e giro: prevenir com base aberta e ajuste de peso.
  - Escape recuperando quadril/perna por dentro: prevenir bloqueando quadril e reencaixando pressão.
- Transições:
  - Kesa-gatame → variação de controle lateral / retomada de posição dominante.
- Checklist:
  - [ ] Base está aberta e estável
  - [ ] Peso bem distribuído (não só nos braços)
  - [ ] Quadril do uke está controlado (sem espaço)
  - [ ] Tenho um plano de transição se ele começar a escapar

---

### 4.2 Glossário (principais conceitos)
- **Judogi**: uniforme do judô.
- **Tori**: quem aplica a técnica.
- **Uke**: quem recebe a técnica.
- **Kumi-kata**: disputa/estratégia de pegada.
- **Kuzushi**: desequilíbrio do oponente.
- **Tsukuri**: preparação/entrada da técnica.
- **Kake**: execução final da técnica.
- **Nage-waza**: técnicas de projeção.
- **Ne-waza**: técnicas de solo.
- **Te-waza**: técnica de braço ou mão.
- **Osaekomi-waza**: imobilizações.
- **Shime-waza**: estrangulamentos.
- **Kansetsu-waza**: chaves de articulação.
- **Renraku-waza**: técnicas combinadas.
- **Randori**: treino livre.
- **Shiai**: competição.

---

### 4.3 Prompts reutilizáveis (para futuras revisões)

1. **Revisão rápida (10 min)**
   - “Faça uma revisão rápida de **[técnica/tema]** em no máximo 12 bullets, incluindo: objetivo, 3 pontos-chave, 3 erros comuns, 2 correções e 1 exercício de treino. Use apenas as fontes do notebook e cite as referências.”

2. **Correção de erro específico**
   - “Estou errando **[descrição do erro]** em **[técnica]**. Quais são as causas prováveis e correções, com base nas fontes carregadas? Cite as referências.”

3. **Comparação para decisão tática**
   - “Compare **[técnica A]** vs **[técnica B]** para o cenário: **[ex.: oponente canhoto, pegada dominante, movimento para trás]**. Liste critérios de decisão e riscos. Use apenas as fontes.”

4. **Checklist pré-treino**
   - “Crie um checklist de 8 itens para eu revisar antes do treino com foco em **[tema]**. Use apenas as fontes.”

5. **Perguntas para o sensei**
   - “Gere 5 perguntas objetivas para eu levar ao meu sensei sobre **[técnica/tema]**, baseadas em dúvidas comuns e no que as fontes indicam.”

---

## Como usar este repositório
1. Fazer upload das fontes no NotebookLM.
2. Rodar os prompts acima e salvar as melhores respostas.
3. Atualizar as seções **Resumos**, **Glossário** e **Prompts reutilizáveis** com o que foi consolidado.
4. Registrar novas “cicatrizes” sempre que um prompt falhar — isso faz parte do aprendizado.

---

## Aviso de segurança
Judô envolve risco de lesão. Este material é educacional e não substitui acompanhamento presencial com orientação adequada.
