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

#### Fundamentos essenciais (checklist)
- **Postura (shisei)**: (preencher)
- **Pegada (kumi-kata)**: (preencher)
- **Desequilíbrio (kuzushi)**: (preencher)
- **Entrada (tsukuri)**: (preencher)
- **Execução (kake)**: (preencher)
- **Transições para o solo**: (preencher)

#### Nage-waza (exemplo de estrutura por técnica)
> Repita este molde para as técnicas que você estudar.

**Técnica:** (ex.: O-soto-gari)  
- Objetivo:
- Quando usar:
- Kuzushi:
- Tsukuri:
- Kake:
- Erros comuns:
- Ajustes/correções:
- Combinações e continuação:
- Contra-ataques comuns (e prevenção):
- Referências nas fontes:

#### Ne-waza (exemplo)
**Tema:** (ex.: Kesa-gatame e escapes)  
- Princípio:
- Pontos de controle:
- Erros comuns:
- Escape 1 / Escape 2:
- Transições:
- Referências nas fontes:

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

5. **Perguntas para o professor**
   - “Gere 5 perguntas objetivas para eu levar ao meu professor sobre **[técnica/tema]**, baseadas em dúvidas comuns e no que as fontes indicam.”

---

## Como usar este repositório
1. Fazer upload das fontes no NotebookLM.
2. Rodar os prompts acima e salvar as melhores respostas.
3. Atualizar as seções **Resumos**, **Glossário** e **Prompts reutilizáveis** com o que foi consolidado.
4. Registrar novas “cicatrizes” sempre que um prompt falhar — isso faz parte do aprendizado.

---

## Aviso de segurança
Judô envolve risco de lesão. Este material é educacional e não substitui acompanhamento presencial com orientação adequada.
