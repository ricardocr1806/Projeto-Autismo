# Especificação do produto (versão 1.0)

> **App de rotina, diário, comunidade e benefícios para mães e pais de crianças autistas.**
> Este documento descreve tudo o que o app deve ter antes de começarmos a programar.
> Base de pesquisa: `pesquisa-dores-pais-de-autistas.md` e `proposta-app.md`.

---

## Sumário

1. [Visão e nome](#1-visão-e-nome)
2. [Para quem é](#2-para-quem-é)
3. [Mapa do app (abas e telas)](#3-mapa-do-app)
4. [Módulo 1: Hoje (tela inicial)](#4-módulo-1--hoje)
5. [Módulo 2: Rotina](#5-módulo-2--rotina)
6. [Módulo 3: Atividades (exercícios, música e brincadeiras)](#6-módulo-3--atividades)
7. [Módulo 4: Diário da criança e relatórios em PDF](#7-módulo-4--diário-da-criança)
8. [Módulo 5: Clã (comunidade de mães)](#8-módulo-5--clã)
9. [Módulo 6: Hub de parceiros e benefícios](#9-módulo-6--hub-de-parceiros-e-benefícios)
10. [Módulo 7: Aprender (blog de estudos e mercado)](#10-módulo-7--aprender-blog)
11. [Módulo 8: Guia "Como avançar no tratamento"](#11-módulo-8--guia-como-avançar-no-tratamento)
12. [Módulos extras úteis para os pais](#12-módulos-extras)
13. [Modelo de negócio](#13-modelo-de-negócio)
14. [Segurança, ética e LGPD](#14-segurança-ética-e-lgpd)
15. [Tecnologia](#15-tecnologia)
16. [Roteiro de lançamento](#16-roteiro-de-lançamento)
17. [Métricas de sucesso](#17-métricas-de-sucesso)
18. [Riscos e como reduzi-los](#18-riscos)
19. [Próximos passos](#19-próximos-passos)
20. [Fontes científicas usadas nesta especificação](#20-fontes)

---

## 1. Visão e nome

**Missão:** nenhuma mãe atípica deve enfrentar o autismo do filho sozinha, sem informação ou sem dinheiro para começar.

**Promessa:** *"Organize o dia do seu filho, registre a evolução dele, aprenda o que funciona e conte com um clã de mães que entendem você. Tudo em um só app, a partir de R$ 9,90 por mês."*

**Sugestões de nome** (consultar o INPI antes de decidir):

| Nome | Ideia |
|---|---|
| **Elo** | O elo entre mães, filhos, terapeutas e escola. |
| **Clã Atípico** | Assume a ideia do clã logo no nome. |
| **Juntas** | Foco na comunidade de mães. |
| **Ninho** | Acolhimento, casa e rotina. |

> **Identidade visual:** evitar a peça de quebra-cabeça, porque muitos autistas a rejeitam por sugerir que "falta uma peça". Preferir o símbolo do infinito (neurodiversidade) ou uma identidade própria. Usar cores calmas e pouco estímulo visual.

**Princípios do produto:**
1. **Preço acessível e foco em crescer a base.** Assinatura de R$ 9,90 a R$ 49,90 por mês (seção 13). O SOS Crise e o cartão com QR são sempre grátis, e há assinatura patrocinada para famílias de baixa renda.
2. **Baseado em evidência.** Todo conteúdo clínico é revisado por profissionais e mostra seu nível de evidência.
3. **Feito para mães cansadas.** Tudo se faz com até 3 toques, as lições duram até 10 minutos, há áudio sempre e o app funciona sem internet.
4. **Comunidade com gente de verdade.** Os estudos mostram que programas sem apoio humano têm mais abandono.
5. **Respeito à criança autista.** Nada de "cura", nada de "normalizar". O objetivo é desenvolvimento, autonomia e bem-estar.

---

## 2. Para quem é

### Persona principal: Juliana, 34 anos, mãe do Davi (4 anos, TEA nível 2)
- Mora na periferia de uma capital e depende do SUS. Está na fila do CER há 7 meses.
- Saiu do emprego para cuidar do Davi e vive com a renda do marido mais o BPC, que ainda está em análise.
- Tem um celular Android simples, com pouco espaço e um pacote de dados limitado.
- Se informa por grupos de WhatsApp e pelo Instagram.
- **Dores:** crises diárias, Davi come só 5 alimentos, dorme mal, ela não sabe o que fazer em casa e se sente sozinha e esgotada.
- **O que ela quer:** "Saber o que fazer com ele hoje" e "alguém que me entenda".

### Persona secundária: Marcos, 38 anos, pai da Sofia (7 anos, TEA nível 1)
- Tem plano de saúde, mas o plano limita as sessões. A escola não oferece mediadora.
- **O que ele quer:** organizar laudos e relatórios para brigar com o plano e com a escola, e dividir as tarefas com a esposa.

### Outros usuários (com acesso convidado)
- Avós, babá e outros cuidadores, que veem a rotina e registram no diário.
- Terapeutas, que recebem um relatório ou um link temporário.
- A escola (professor ou mediador), que recebe o relatório escolar e, numa fase futura, um diário compartilhado.

---

## 3. Mapa do app

### Barra inferior (5 abas)

| Aba | O que tem |
|---|---|
| 🏠 **Hoje** | O resumo do dia: rotina, atividade sugerida, registro rápido e o clã. |
| 🗓️ **Rotina** | Quadro visual, timer, músicas de rotina e o modo criança. |
| 📒 **Diário** | Registros, gráficos e relatórios em PDF. |
| 👥 **Clã** | O grupo da mãe, o fórum aberto e as trocas. |
| ✨ **Descobrir** | Aprender (blog), Guia do tratamento, Benefícios, Direitos, Mapa e Atividades. |

### Elementos fixos
- **Botão SOS Crise:** sempre visível no topo, levando a um passo a passo calmo para a hora da crise.
- **Botão "+":** registro rápido no diário de qualquer tela.
- **Seletor de criança:** para famílias com mais de um filho autista.

### Primeiro acesso (cadastro em 2 minutos)
1. Nome da mãe e celular. O login é por código via SMS ou WhatsApp, sem senha.
2. Dados básicos da criança: apelido, idade, se já tem diagnóstico, se faz terapia, se fala, se tem dificuldade com sono ou alimentação.
3. Cidade, para montar o clã e o mapa.
4. Fase da jornada: "suspeita", "recebi o laudo agora", "em terapia" ou "faz tempo que sei".
5. O app monta automaticamente uma rotina inicial, uma trilha de atividades e o primeiro passo do Guia do tratamento.

---

## 4. Módulo 1: Hoje

A tela inicial responde a três perguntas: **o que eu faço agora, como foi o dia e quem está comigo.**

```
┌─────────────────────────────────┐
│ Bom dia, Juliana ☀️     [SOS]   │
│                                 │
│ ROTINA DE HOJE (Davi)           │
│ ✅ Acordar  ✅ Café  ⏳ Banho     │
│ ▢ Escola  ▢ Brincar  ▢ Dormir   │
│                                 │
│ ⭐ ATIVIDADE DO DIA (10 min)     │
│ "Bolhas de sabão: pedir mais"   │
│ [Ver como fazer]  [Fiz! ✔]      │
│                                 │
│ 📒 COMO FOI A NOITE?            │
│ 😴 Bem   😐 Mais ou menos   😫 Mal│
│                                 │
│ 👥 SEU CLÃ                       │
│ Ana: "Alguém tem dica de..."    │
│ 3 mensagens novas               │
│                                 │
│ 💡 DICA: Antecipar mudanças     │
│ reduz crises. (2 min de leitura)│
└─────────────────────────────────┘
```

**Funcionalidades:**
- Rotina do dia com um toque para marcar cada tarefa.
- Atividade do dia escolhida pelo objetivo e pela idade, com a opção "fiz" (que registra no diário).
- Perguntas rápidas que alimentam o diário: sono, humor e se houve crise hoje.
- Prévia do clã.
- Dica do dia, ligada ao blog.
- **Check-in da mãe** uma vez por semana: "Como você está de 0 a 10?". Se a nota for baixa, o app oferece apoio (ver o Módulo extra "Cuidar de quem cuida").

---

## 5. Módulo 2: Rotina

**Por quê:** rotina previsível e antecipação reduzem ansiedade e crises. Agendas visuais estão entre as estratégias mais usadas em intervenções para o autismo.

### Funcionalidades
1. **Quadro visual de rotina**
   - Pictogramas: usar a base gratuita **ARASAAC** (verificar a licença), fotos reais da própria casa ou desenhos.
   - Formatos: lista vertical, "agora → depois" (primeiro-depois) e linha do tempo do dia.
   - **Modelos prontos:** manhã, ida à escola, banho, refeição, dormir, ida ao médico ou ao dentista, passeio, dia sem escola.
   - Arrastar para reordenar, e cópia da rotina para outros dias.
2. **Timer visual:** um círculo que diminui, mostrando "quanto falta", com aviso sonoro ou só vibração para crianças sensíveis a som.
3. **Avisos de transição:** "Em 5 minutos vamos para o banho" (voz gravada pela mãe ou voz do app).
4. **Músicas de rotina:** uma música curta para cada etapa (banho, escovar os dentes, guardar os brinquedos, dormir). A mãe também pode gravar a própria voz cantando.
5. **Sistema de recompensas (economia de fichas):** estrelas por etapa concluída, trocadas por um prêmio escolhido pela família, com o objetivo visível ("faltam 2 estrelas para o parquinho").
6. **Modo criança:** tela simplificada, com só a rotina e o timer, botões grandes e bloqueio para a criança não sair do modo (a saída exige um código da mãe).
7. **Mudanças imprevistas:** o card "Hoje vai ser diferente" ajuda a antecipar uma mudança na rotina.
8. **Integração com o diário:** rotinas cumpridas e não cumpridas viram dado. Por exemplo: "nos dias sem rotina houve mais crises".

### Ideias futuras
- Imprimir a rotina em PDF para colar na geladeira ou levar para a escola.
- Rotina compartilhada com avós, babá e escola.

---

## 6. Módulo 3: Atividades

Uma biblioteca de **exercícios, música e brincadeiras** para fazer em casa com materiais simples, inspirada nos programas com evidência citados nas seções 2 e 20.

### Como cada atividade é apresentada
```
🎯 Objetivo: Comunicação, pedir "mais"
⏱️ 10 min · 👶 2 a 6 anos · 🧺 Material: bolhas de sabão
📶 Nível: iniciante

COMO FAZER (com vídeo de 60 segundos e áudio)
1. Sente-se de frente para a criança, na altura dos olhos.
2. Faça bolhas e pare. Espere ela olhar para você ou para o pote.
3. Diga "mais?" e espere 5 segundos.
4. Qualquer tentativa (olhar, som, gesto, palavra) → faça bolhas!

ADAPTE: Se ela não se interessar → tente balão, pião ou carrinho.
O QUE OBSERVAR: Ela olhou para você? Fez algum som ou gesto?
[✔ Fiz]  [⭐ Favoritar]  [📒 Registrar o que ela fez]
```

### Filtros
- **Objetivo:** comunicação, atenção compartilhada, imitação, brincar, coordenação motora, regulação/calma, autonomia (vestir, comer, higiene), sensorial e social.
- **Idade:** 1-3, 3-6, 6-10 e 10 anos ou mais.
- **Tempo:** 5, 10 ou 15 minutos.
- **Material:** nenhum, caseiro ou comprado.
- **Ambiente:** casa, rua ou banho.

### 6.1 Brincadeiras (o coração do módulo)
Inspiradas no CST da OMS e nas intervenções que unem brincadeira e técnicas comportamentais (as NDBIs, como ESDM, JASPER e PRT):
- seguir a liderança da criança, entrando na brincadeira dela;
- brincadeiras de "pausa e espera" para estimular o pedido;
- jogos de vez ("minha vez, sua vez");
- imitação de ações com brinquedos e com o corpo;
- brincadeiras sensoriais (massinha, água, areia, feijão);
- faz de conta, para crianças maiores.

**A trilha semanal:** uma "missão da semana" (por exemplo, 10 minutos de brincadeira guiada por dia, durante 7 dias), com um vídeo, a prática e um registro.

### 6.2 Exercícios físicos
**Evidência:** meta-análises de ensaios randomizados mostram melhora de habilidades motoras, coordenação e habilidades sociais com exercício. Há também redução pequena de comportamentos repetitivos (efeito pequeno, com resultados conflitantes entre os estudos). Esportes com bola e artes marciais (katá) aparecem entre os melhores resultados.
- **Pausas de movimento** de 3 minutos: pular, dança da estátua, "andar como bicho".
- **Circuitos caseiros:** almofadas, cadeiras e fita no chão.
- **Jogos com bola:** chutar, arremessar, quicar.
- **Yoga infantil e alongamento**, com cartões ilustrados.
- **Atividades para gastar energia** antes de dormir ou de fazer a lição.
- Aviso: crianças com condições médicas devem ter liberação do médico.

### 6.3 Música
**Evidência:** a musicoterapia feita por profissional tem evidência moderada (revisão Cochrane de 2022), mas o maior estudo isolado (TIME-A) não encontrou efeito. O uso de música para acalmar tem evidência fraca, e muitas crianças são sensíveis a sons.
- **Cantinho da calma:** uma playlist que funciona offline (sons da natureza, ruído branco, músicas lentas), com volume baixo por padrão e sem anúncios. A mãe marca o que funciona com o filho, e o diário mostra: "essa música ajudou em 4 das 5 vezes".
- **Músicas de rotina:** integradas ao Módulo 2.
- **Brincadeiras musicais:** imitar ritmos, parar quando a música para, instrumentos caseiros.
- **Alerta sensorial:** "Se seu filho é sensível a sons, na crise prefira silêncio ou abafador."

### Volume inicial
**30 atividades** no lançamento (15 brincadeiras, 8 exercícios e 7 de música e calma), chegando a 100 em 6 meses.

---

## 7. Módulo 4: Diário da criança

**Por quê:** o médico vê a criança 15 minutos a cada 3 meses, enquanto a mãe vê 24 horas por dia. O diário transforma o que a mãe observa em **informação organizada**, que serve a médico, terapeuta, escola, Defensoria ou processo.

### 7.1 Tipos de registro (todos com até 3 toques)

| Registro | O que perguntar | Detalhe opcional |
|---|---|---|
| 🌩️ **Crise** | Intensidade (1 a 5) e duração | **O que aconteceu antes** (gatilho: barulho, mudança, fome, sono, negativa, tela), **o que aconteceu** (choro, agressão, autoagressão, fuga), **o que ajudou**, local, foto ou áudio |
| 😴 **Sono** | Hora de dormir, hora de acordar e quantas vezes acordou | Qualidade, cochilo, uso de tela antes de dormir |
| 🍽️ **Alimentação** | Comeu bem, pouco ou recusou | Alimento novo tentado (aceitou, tocou, cheirou ou recusou), lista de alimentos aceitos |
| 💊 **Medicação** | Remédio, dose e horário | Efeitos percebidos e lembretes |
| 🌟 **Conquista** | O que ela fez de novo | Foto ou vídeo, categoria (fala, autonomia, social, escola) |
| 🧩 **Terapia** | Qual terapia e se compareceu | Anotação do terapeuta e tarefa para casa |
| 😊 **Humor do dia** | Ótimo, bom, difícil ou muito difícil | Observação livre |
| 🚽 **Desfralde e higiene** | Escape ou sucesso | Horários |
| 🏫 **Escola** | Como foi o dia segundo a escola | Bilhete ou foto da agenda |
| 📝 **Anotação livre** | Texto ou áudio | Pode ser transcrito automaticamente (futuro) |

> O registro de crise segue o modelo **ABC (antecedente, comportamento e consequência)**, usado por analistas do comportamento e terapeutas para entender a função de um comportamento. Isso torna o registro útil de verdade para o terapeuta.

### 7.2 Visualização
- **Linha do tempo:** tudo que aconteceu, dia a dia.
- **Gráficos simples:** crises por semana, horas de sono, alimentos aceitos e conquistas acumuladas.
- **Descobertas automáticas** (correlações, sem diagnóstico). Exemplos:
  - "As crises foram 2x mais frequentes nos dias depois de noites com menos de 8 horas de sono."
  - "O gatilho mais comum este mês foi barulho."
  - "O que mais ajudou: abafador (6 vezes) e colo (4 vezes)."
- **Calendário de cores**, com dias bons e dias difíceis.

### 7.3 Relatórios em PDF (o maior diferencial)
A mãe escolhe o **período** (30, 90 ou 180 dias, ou personalizado), o **modelo** e **o que incluir**.

| Modelo | Para quem | O que contém |
|---|---|---|
| 🩺 **Médico / terapeuta** | Neuropediatra, psiquiatra, terapeutas | Resumo do período, gráficos de crises e sono, padrões de gatilho, alimentação, medicação e efeitos, conquistas, perguntas que a mãe quer fazer na consulta |
| 🏫 **Escola** | Professor, coordenação, mediador | Como a criança se comunica, gatilhos de crise, o que acalma, o que ela gosta, rotina que funciona, recomendações dos terapeutas |
| ⚖️ **Jurídico / plano / Defensoria** | Advogado, Defensoria, ANS, Procon | Cronologia de crises e de episódios de risco (autoagressão, fuga), **terapias prescritas x terapias recebidas**, histórico de pedidos e negativas com número de protocolo, documentos anexos (laudos) |
| 📋 **Resumo de uma página** | Emergência, novo profissional, babá | Quem é a criança, diagnóstico, medicação, alergias, como se comunica, o que acalma, contatos |

**Regras:**
- O PDF traz o aviso: *"Relatório de registros feitos pela família. Não substitui laudo ou avaliação profissional."*
- O PDF é **gerado no próprio celular**, o que funciona offline e protege a privacidade.
- Pode ser compartilhado por WhatsApp e e-mail, ou por um **link temporário** (expira em 7 dias) para o terapeuta.

### 7.4 Compartilhamento
- Convidar o pai, os avós e a babá para registrar no diário, cada um com sua permissão.
- No futuro, terapeutas poderão responder no diário com anotações e tarefas para casa.

---

## 8. Módulo 5: Clã

**Por quê:** as mães relatam isolamento e pouca rede de apoio, e se informam principalmente com outras mães. A evidência mostra que o **apoio humano** reduz o abandono, e que pessoas que não são especialistas, quando treinadas, conseguem apoiar outras famílias (estudos PASS).

### 8.1 O que é um clã
- Um **grupo fechado de 8 a 12 mães (ou pais)**, formado automaticamente por **região**, **idade da criança** e **fase da jornada**. Por exemplo: "Clã Zona Leste SP · filhos de 2 a 5 anos · recém-diagnóstico".
- Cada clã tem uma **mãe-guia**: uma mãe mais experiente, voluntária, treinada pelo app e acompanhada pela equipe. No futuro ela pode receber uma bolsa ou benefícios.
- Cada clã tem nome e emblema próprios, escolhidos pelas integrantes.

### 8.2 Funcionalidades do clã
1. **Mural do clã:** mensagens, fotos (só dentro do clã) e áudios.
2. **Pedido de ajuda**, com categorias:
   - 💬 desabafo: "só preciso que alguém me ouça";
   - ❓ dúvida: "alguém já passou por isso?";
   - 🤝 ajuda prática: acompanhar numa consulta, indicar um profissional, ajudar com documentos;
   - 🎁 doação ou troca: roupas, brinquedos sensoriais, materiais.
3. **Check-in semanal do clã:** "Como foi sua semana?", com reações de apoio.
4. **Encontro ao vivo semanal** de 30 a 45 minutos por vídeo, conduzido pela mãe-guia, com um tema da semana ligado à trilha de atividades.
5. **Conquistas compartilhadas:** a mãe pode compartilhar uma conquista do diário com o clã ("O Davi falou 'mãe' hoje!").
6. **Missões coletivas:** "Esta semana todas vamos tentar 1 alimento novo".
7. **Selos de ajuda:** reconhecimento para quem mais ajuda (por exemplo, "Mãe-farol" e "Mão amiga"), sem ranking competitivo.

### 8.3 Além do clã
- **Fórum aberto:** perguntas para todas as mães do app, organizadas por tema (sono, alimentação, escola, direitos, adolescência, vida adulta).
- **Clãs temáticos opcionais:** pais (homens), mães solo, autismo nível 3, adolescentes, mães autistas, famílias de baixa renda, cidades do interior.
- **Banco de trocas:** doação ou troca de materiais por cidade.
- **Encontros presenciais** (futuro): eventos organizados pelos clãs da mesma cidade, como piqueniques e "sessões azuis" de cinema.

### 8.4 Regras e segurança da comunidade
- **Fotos de crianças:** só são permitidas dentro do clã fechado, nunca no fórum aberto, e com um aviso de consentimento.
- **Proibido** vender, indicar ou divulgar "cura" ou tratamentos perigosos (ver a lista da seção 9.5).
- **Moderação em 3 camadas:** filtro automático de palavras e links, mãe-guia e equipe do app.
- **Botão denunciar** em todo post.
- **Detecção de risco:** mensagens com sinais de desespero ou risco de suicídio disparam acolhimento e o contato do **CVV (188)** e do CAPS mais próximo.
- **Verificação:** cadastro por celular e regras aceitas na entrada. Perfis de profissionais e de empresas são identificados.
- **Sem anúncios dentro do clã.** O clã é um espaço seguro.

---

## 9. Módulo 6: Hub de parceiros e benefícios

**Objetivo:** dar às famílias **descontos reais em tratamentos, produtos e serviços**, o que ajuda a compensar a assinatura, e **complementar a receita** do app.

### 9.1 Categorias de parceiros

| Categoria | Exemplos de benefício |
|---|---|
| 🧠 **Terapias** | Clínicas multidisciplinares e terapeutas autônomos (fono, TO, psicologia, psicopedagogia) com **preço social** ou desconto |
| 🩺 **Saúde** | Neuropediatras, dentistas preparados para autistas, exames, farmácias e farmácias de manipulação |
| 🎧 **Produtos** | Abafadores, brinquedos sensoriais, pratos e talheres adaptados, roupas sem etiqueta, materiais pedagógicos |
| 🏫 **Educação** | Escolas inclusivas, cursos para pais, reforço escolar especializado, cursos de formação de mediador |
| ⚖️ **Jurídico** | Advogados de saúde e previdência com primeira consulta gratuita ou preço social |
| ✂️ **Serviços "amigos do autista"** | Cabeleireiro, fotógrafo, buffet, hotel e transporte |
| 🎢 **Lazer** | Sessões de cinema adaptadas, parques com horário sensorial, esportes adaptados, natação |
| 💼 **Trabalho e renda** | Vagas com horário flexível para mães, cursos de renda extra, empresas parceiras |
| 🆘 **Plantão de acolhimento** | Terapeutas e clínicas verificados que oferecem orientação por telefone ou vídeo durante crises, em horários definidos, aparecendo na **Rede de ajuda próxima** (seção 12.1-B). Contrapartida: selo "Parceiro de plantão" e destaque no Hub. Não há ranking pago em emergência. |
| 🔖 **Produtos de identificação** | Pulseiras, etiquetas, chaveiros e adesivos com o QR code do Cartão da criança |

### 9.2 Formatos de parceria
1. **Cupom ou preço social:** a mãe resgata no app e o parceiro valida (código ou QR).
2. **Vitrine do parceiro:** uma página com fotos, serviços, avaliações das mães, endereço e WhatsApp.
3. **Destaque na categoria:** um anúncio nativo, sempre identificado como **"Patrocinado"**.
4. **Conteúdo patrocinado:** separado do conteúdo científico, sempre identificado e revisado pela equipe.
5. **Patrocínio institucional:** uma empresa patrocina clãs, eventos, trilhas ou "bolsas de terapia".
6. **Benefício corporativo:** empresas oferecem o app e os descontos aos funcionários que são pais de autistas.

### 9.3 Selo "Parceiro verificado"
Para receber o selo, o parceiro precisa:
- ter CNPJ ativo ou registro profissional válido no conselho (CRP, CREFONO, COFFITO, CRM ou CRO);
- assinar a **Política de Parceiros** (seção 9.5);
- ter avaliações das mães acima de 4 estrelas, revistas a cada 6 meses;
- não ter reclamações graves sem solução.

### 9.4 Avaliações
- Só avalia quem resgatou o benefício.
- Os critérios são: acolhimento, preço justo, explica o que faz, envolve os pais e trata bem a criança.

### 9.5 Política de anúncios e parceiros (inegociável)
**É proibido anunciar:**
- qualquer coisa que prometa **"cura do autismo"** ou "tirar a criança do espectro";
- **MMS / dióxido de cloro**, que é proibido pela Anvisa e é um produto corrosivo;
- quelação, ozonioterapia, células-tronco fora de pesquisa clínica aprovada, câmara hiperbárica para autismo e "desintoxicação";
- suplementos, dietas ou produtos com promessa de tratar o autismo;
- profissionais sem registro no conselho;
- qualquer tratamento sem evidência científica, segundo a avaliação do conselho científico do app.

**Regras de privacidade nos anúncios:**
- **Os dados de saúde do diário NUNCA são usados para direcionar anúncios.** A segmentação é feita só por cidade e pelas categorias de interesse que a própria mãe escolher (opt-in).
- Não há anúncios no Diário, no Clã, no SOS Crise, no modo criança nem no conteúdo científico.
- Os anúncios seguem o Código de Defesa do Consumidor e o CONAR.

---

## 10. Módulo 7: Aprender (blog)

Uma central de **estudos explicados em linguagem simples**, **atualizações de mercado e de direitos** e **orientações práticas**.

### 10.1 Seções

| Seção | O que publica | Frequência |
|---|---|---|
| 🔬 **Estudos explicados** | Uma pesquisa resumida em 3 minutos: o que foi estudado, o que encontraram, quão confiável é e **o que fazer com isso em casa** | 1 por semana |
| 📰 **Atualizações e mercado** | Novas leis, decisões da ANS e do STJ, programas do SUS (como o CST), novos serviços, apps, startups e tendências | 1 por semana |
| 🧭 **Guia do tratamento** | Os passos para avançar no tratamento (Módulo 8) | Fixo, revisado a cada trimestre |
| ✅❌ **Mitos e verdades** | Combate à desinformação: vacinas, MMS, "curas" e dietas milagrosas | 2 por mês |
| 🏠 **Na prática** | Como lidar com sono, alimentação, crises, desfralde, dentista, corte de cabelo e viagens | 1 por semana |
| 💜 **Histórias de mães** | Relatos reais (com autorização) e a voz de **adultos autistas** | 2 por mês |
| 🏫 **Para a escola** | Material para enviar ao professor | 1 por mês |

### 10.2 Semáforo de evidência
Todo post sobre tratamento traz um selo:
- 🟢 **Evidência forte:** várias pesquisas boas concordam. Exemplo: intervenção mediada pelos pais.
- 🟡 **Evidência moderada:** resultados promissores, mas com dúvidas. Exemplo: musicoterapia.
- 🟠 **Evidência fraca ou inicial:** estudos pequenos. Exemplo: música para acalmar em crises.
- 🔴 **Sem evidência ou perigoso:** exemplos: MMS e quelação.

### 10.3 Formato de cada post
1. **Título simples:** "Exercício físico ajuda crianças autistas?"
2. **Resposta curta** em 2 linhas, no topo.
3. O que a pesquisa diz, em até 300 palavras.
4. **Caixa "O que fazer com isso"**, com 3 ações práticas e um link para uma atividade do app.
5. O selo do semáforo.
6. As fontes (links) e a data da última revisão.
7. Uma versão em **áudio** de 2 a 3 minutos.
8. Um botão para "compartilhar no clã".

### 10.4 Processo editorial
- **Conselho científico:** 1 fonoaudiólogo, 1 terapeuta ocupacional, 1 psicólogo ou analista do comportamento, 1 neuropediatra ou psiquiatra infantil, 1 advogado e **1 adulto autista**.
- Todo post clínico é revisado por um membro do conselho antes de ser publicado.
- Todo post é revisado a cada 12 meses ou quando sair um estudo novo.
- **Conteúdo científico nunca é patrocinado.**

### 10.5 Primeiras 20 pautas (com base nas pesquisas já levantadas)

**Estudos explicados**
1. Pais podem ser parte da terapia? O que dizem 12 estudos com 964 crianças. 🟢
2. O programa da OMS para cuidadores (CST) chegou ao Brasil: o que é e como participar. 🟢
3. Musicoterapia funciona? O que a revisão Cochrane de 2022 e o maior estudo do mundo dizem. 🟡
4. Exercício físico ajuda crianças autistas? As meta-análises respondem. 🟢🟡
5. Brincar é terapia: o que são as NDBIs (ESDM, JASPER, PRT) e como usar em casa. 🟢
6. Abafadores de ruído: quando usar e o que diz a ciência. 🟠
7. Música para acalmar na crise: ajuda ou atrapalha? 🟠

**Atualizações e mercado**

8. Mapa Autismo Brasil 2026: o que os dados de 23 mil famílias revelam.
9. Censo do IBGE: o Brasil tem 2,4 milhões de autistas diagnosticados. O que isso muda.
10. Nova linha de cuidado do Ministério da Saúde para o autismo (rastreio de 16 a 30 meses).
11. Plano de saúde negou terapia? Seus direitos e o passo a passo.
12. BPC para autistas: as concessões triplicaram. Como pedir.
13. Decreto 12.686/2025: o que muda sobre o profissional de apoio escolar.

**Mitos e verdades**

14. Vacina causa autismo? ❌ Não.
15. MMS / dióxido de cloro: por que é perigoso e proibido. 🔴
16. "Meu filho vai sair do espectro?" O que é realista esperar da terapia.

**Na prática**

17. Crise x birra: como diferenciar e o que fazer em cada uma.
18. Seletividade alimentar: o passo a passo (olhar → tocar → cheirar → provar).
19. Sono: rotina de dormir para crianças autistas.
20. Primeiros 30 dias depois do diagnóstico: um checklist.

---

## 11. Módulo 8: Guia "Como avançar no tratamento"

Uma **trilha interativa** que a mãe percorre no próprio ritmo. Cada etapa tem checklist, explicação, modelos de documentos e onde buscar ajuda. O app destaca a etapa em que a família está.

### Etapa 1: Percebi sinais
- Sinais de alerta por idade: não responde ao nome, pouco contato visual, não aponta, atraso na fala, perda de habilidades, interesses muito restritos, sensibilidade sensorial intensa.
- Questionário de triagem **M-CHAT-R/F** (de 16 a 30 meses), feito no app, com o aviso de que **não é diagnóstico**.
- **O que fazer:** levar à UBS, pedir que o pedido fique no prontuário e pedir o **encaminhamento com protocolo**.
- ⭐ **Mensagem-chave:** *"Não espere o laudo para começar a estimular. As atividades do app podem começar hoje."*

### Etapa 2: Avaliação e laudo
- Quem diagnostica: neuropediatra, psiquiatra infantil ou equipe multiprofissional.
- O caminho no SUS: UBS → regulação → CER, CAPSi ou ambulatório especializado.
- O que levar: o diário do app (relatório médico), vídeos da criança, a caderneta da criança e relatórios da escola.
- **O que um bom laudo deve conter:**
  - diagnóstico (CID);
  - nível de suporte;
  - **terapias recomendadas com a carga horária semanal**, o que é essencial para conseguir no plano ou na Justiça;
  - a necessidade de profissional de apoio escolar, se for o caso.

### Etapa 3: Montar o plano terapêutico
- No SUS, pedir o **Projeto Terapêutico Singular (PTS)**.
- As terapias com mais evidência:
  - intervenções comportamentais e naturalísticas (ABA de qualidade, ESDM, JASPER);
  - fonoaudiologia;
  - terapia ocupacional;
  - treinamento de pais.
- Definir **metas claras e mensuráveis**, como "pedir água com palavra ou gesto em 3 meses".
- Não há ABA ou terapia disponível? Ver as alternativas gratuitas: clínicas-escola de universidades, APAE, AMA, ONGs, o CST/SUS e as atividades do app.

### Etapa 4: Escolher bons profissionais (checklist)
✅ Tem registro no conselho (consulte no site do conselho)
✅ Define metas com a família e mostra a evolução
✅ Envolve os pais e ensina o que fazer em casa
✅ Entrega relatórios periódicos
✅ Explica o que faz e por quê
✅ Respeita a criança, sem punição, gritos ou contenção desnecessária
✅ Respeita o jeito autista (stims, interesses) e foca em autonomia e bem-estar

🚩 **Sinais de alerta (fuja):**
- promete cura ou "tirar do espectro";
- vende produtos milagrosos;
- não deixa os pais assistirem a nenhuma sessão;
- não tem metas;
- a criança volta com medo ou machucada.

### Etapa 5: A casa como parte da terapia
- 15 a 20 minutos por dia de brincadeira guiada (trilha de atividades).
- Rotina visual (Módulo 2).
- Registro no diário para levar ao terapeuta.
- Pedir ao terapeuta uma "tarefa de casa" a cada sessão.

### Etapa 6: Acompanhar a evolução
- Reavaliação a cada 6 meses, levando o relatório do diário.
- Perguntas a fazer: "Quais metas foram alcançadas? O que muda no plano?"
- Se não houver evolução em 6 meses, revisar o plano ou o profissional.

### Etapa 7: Garantir os direitos (ligado ao módulo Direitos)
- Plano de saúde: cobertura das terapias prescritas, negativa por escrito e reclamação na ANS.
- SUS: protocolo e regulação.
- Escola: matrícula garantida e profissional de apoio quando houver necessidade comprovada.
- BPC, CIPTEA, passe livre e prioridades.

### Etapa 8: Cuidar de você
- Sem uma mãe bem, não há tratamento que se sustente.
- Clã, check-in emocional, CAPS e CVV.

### Etapa 9: Pensando no futuro
- Adolescência, puberdade, vida adulta, trabalho e autonomia.
- Planejamento: curatela ou tomada de decisão apoiada, e planejamento financeiro.

---

## 12. Módulos extras

Funcionalidades adicionais que respondem às dores levantadas na pesquisa.

| # | Módulo | O que faz | Por quê |
|---|---|---|---|
| 1 | 🆘 **SOS Crise** | Uma tela calma, com fundo escuro e sem som, e um passo a passo: segurança → reduzir estímulos → não exigir conversa → esperar → acolher. Inclui o "o que acalma o meu filho" (vindo do diário), um exercício de respiração para a mãe e, ao final, "registrar a crise". | As crises são a maior fonte de estresse dos pais. |
| 2 | 📇 **Cartão da criança + Rede de ajuda próxima** | Uma carteirinha digital com QR code para emergências, escola e passeios (mostra também a CIPTEA, se a família tiver), mais um botão "Pedir ajuda perto de mim" que mostra **parceiros, mães do clã e serviços públicos próximos** para ligar na hora. | Quase metade das crianças autistas tenta fugir ou se perder pelo menos uma vez, e a mãe precisa de ajuda rápida por perto. |
| 3 | ⚖️ **Direitos e modelos** | Checklist de direitos com o passo a passo e **modelos prontos**: pedido de negativa por escrito ao plano, reclamação na ANS, requerimento na UBS, pedido de profissional de apoio à escola e roteiro para a Defensoria. | A burocracia é a dor nº 3 da pesquisa. |
| 4 | 🗂️ **Cofre de documentos** | Guarda laudos, receitas, relatórios, protocolos e negativas, organizados e com busca, e alerta quando um laudo está vencendo. | As mães vivem carregando pastas de papel. |
| 5 | 📅 **Agenda e lembretes** | Terapias, consultas, remédios, renovação de laudo e prazos de processos. | Organização da rotina da família. |
| 6 | 🗺️ **Mapa de serviços gratuitos** | CER, CAPSi, APAE, AMA, **clínicas-escola de universidades**, Defensoria, CRAS e lugares "amigos do autista". As próprias mães indicam e avaliam. | A falta de terapia acessível é a dor nº 1. |
| 7 | 📖 **Histórias sociais** | Histórias ilustradas para preparar a criança: ir ao dentista, cortar o cabelo, tomar vacina, viajar, primeiro dia na escola. A mãe pode criar a sua com fotos reais. | Antecipação reduz a ansiedade. |
| 8 | 🗣️ **Comunicação simples** | Uma prancha de comunicação básica (quero, não quero, dor, banheiro, água) e uma indicação de apps de comunicação alternativa (CAA), como o Matraquinha. | Uma criança que não fala precisa se comunicar. |
| 9 | 💜 **Cuidar de quem cuida** | Check-in emocional semanal, áudios de respiração de 3 minutos, "pequenas pausas", divisão de tarefas com o parceiro e encaminhamento para CAPS ou CVV quando necessário. | 68% das mães não têm tempo para si. |
| 10 | 👨‍👩‍👧 **Família conectada** | O pai, os avós e a babá acessam a rotina, o diário e o cartão da criança, com permissões. | Dividir a carga e alinhar todos os cuidadores. |
| 11 | 🏫 **Ponte com a escola** | Relatório escolar, modelo de PEI (plano educacional individualizado), diário compartilhado com o professor ou mediador e checklist de direitos na escola. | A inclusão escolar é a dor nº 6. |
| 12 | 💼 **Trabalho e renda para mães** | Vagas flexíveis, cursos e empreendedorismo, em parceria com empresas. | Muitas mães saem do emprego. |
| 13 | 🌱 **Linha do futuro** | Conteúdo sobre adolescência, puberdade, vida adulta e planejamento. | 79% se preocupam com o futuro. |
| 14 | 🤖 **Assistente de dúvidas (futuro)** | Uma IA que responde **só com base no conteúdo revisado do app**, mostrando as fontes, sem diagnosticar e encaminhando ao profissional quando necessário. | As mães têm dúvidas a toda hora, e a desinformação é enorme. |

### 12.1 Detalhamento dos módulos prioritários

#### A. 🆘 SOS Crise
**Onde fica:** um botão vermelho-suave **sempre visível** no topo de todas as telas, inclusive no modo criança (só a mãe consegue abrir), e um atalho na tela inicial do celular.

**Ao tocar, abre uma tela calma:** fundo escuro, letras grandes, sem som, com o mínimo de texto. Ela segue 5 passos, um de cada vez, e a mãe avança com "Próximo":

| Passo | O que a tela diz |
|---|---|
| 1. **Segurança** | "Afaste objetos perigosos. Se houver risco de se machucar, proteja a cabeça e o corpo da criança. Você não precisa conter à força." |
| 2. **Menos estímulo** | "Diminua luz, barulho e pessoas em volta. Fale pouco, com voz baixa." |
| 3. **O que acalma o [nome]** | Uma lista personalizada que vem do diário. Exemplo: "abafador (ajudou 6x), colo apertado (4x), música 'Ondas' (3x)", com um botão para tocar a música do Cantinho da calma. |
| 4. **Espere e respire junto** | Uma animação de respiração para **a mãe**: "Inspire em 4... solte em 6". "A crise vai passar. Você está fazendo o seu melhor." |
| 5. **Depois da crise** | "Ofereça água e um lugar tranquilo. Não é hora de bronca nem de explicação." Botão: **"Registrar esta crise"**, que abre o diário já com a data, a hora e a duração preenchidas pelo cronômetro. |

**Botões fixos no rodapé do SOS:**
- 📞 **Pedir ajuda perto de mim**, que abre a Rede de ajuda próxima (ver B).
- 🚑 **SAMU 192** quando houver risco à vida ou ferimento grave.
- ⏱️ **Cronômetro** da crise, que conta o tempo automaticamente.

**Regras:**
- O SOS funciona **100% offline**.
- O SOS **nunca mostra anúncios**.
- O conteúdo é revisado pelo conselho científico.
- O texto é personalizável pela mãe com orientações do terapeuta da criança.

---

#### B. 📇 Cartão da criança com QR code + 📍 Rede de ajuda próxima

**B.1 O cartão**
- É a **carteirinha digital** da criança. A mãe escolhe o que aparece:
  - foto e apelido;
  - "Sou autista" e o tipo de comunicação ("não falo, mas entendo", "uso gestos");
  - **o que fazer e o que não fazer** ("não toque sem avisar", "fale devagar", "deixe-o segurar o brinquedo");
  - alergias, medicação de uso contínuo e condições de saúde (como epilepsia);
  - a CIPTEA, se a família tiver;
  - botões para **ligar para os responsáveis**.
- **QR code:** quem escanear (policial, segurança do shopping, professor, socorrista ou um desconhecido que encontrou a criança) vê uma **página de emergência** com essas informações e botões para ligar e mandar WhatsApp aos responsáveis, **sem precisar instalar o app**.
- **Formatos do QR:**
  - no celular da mãe;
  - impresso (PDF para plastificar, colocar na mochila ou na carteira);
  - **pulseira, etiqueta para roupa, chaveiro ou adesivo de tênis** com o QR, vendidos por **parceiros** do Hub, com desconto para as famílias e também como fonte de receita.
- **Alerta de leitura:** quando alguém escaneia o QR, a mãe recebe uma notificação. Se quem escaneou permitir, ela recebe também a localização aproximada de onde foi lido.
- **Privacidade:**
  - nunca mostra endereço nem o nome completo, a menos que a mãe escolha;
  - o link pode ser **desativado e trocado** a qualquer momento (caso o cartão seja perdido);
  - o diagnóstico detalhado e os laudos **não** aparecem no QR.

> Por que isso importa: num estudo com 1.218 crianças autistas (Pediatrics, 2012), **49% tentaram fugir ou se afastar pelo menos uma vez depois dos 4 anos**, e mais da metade dessas crianças ficou desaparecida tempo suficiente para causar preocupação séria.

**B.2 Rede de ajuda próxima ("Pedir ajuda perto de mim")**

Quando a mãe precisa de ajuda **agora**, seja por uma crise forte, por estar sozinha, pela criança ter se perdido ou por não saber o que fazer, o app mostra quem pode ajudar **perto dela**, em 4 camadas:

| Camada | Quem | Como funciona |
|---|---|---|
| 1. **Minha rede** | Pai, avó, vizinha, madrinha: contatos de confiança cadastrados pela mãe | Ligar ou mandar WhatsApp com um toque. Opção de **enviar uma mensagem pronta com a localização**: "Preciso de ajuda com o Davi, estou aqui: [mapa]". |
| 2. **Mães do clã por perto** | Mães do clã que se cadastraram como **"Mão amiga"** (voluntárias, opt-in) e estão na mesma região | A mãe dispara um pedido ("preciso de alguém que ajude por 1 hora" ou "preciso conversar agora") e as Mãos amigas próximas recebem um aviso. **Nenhuma localização exata é exibida**, só "a cerca de 2 km". |
| 3. **Parceiros de plantão** | Terapeutas, clínicas e psicólogos **verificados** que se comprometem com um **plantão de acolhimento** (orientação por telefone ou vídeo durante a crise, em horários definidos) | Lista ordenada por **distância e disponibilidade agora**, com o botão "Ligar". O primeiro contato de orientação é gratuito, e o parceiro ganha visibilidade no Hub como contrapartida (ver a seção 9.1). |
| 4. **Serviços públicos** | **SAMU 192**, Bombeiros 193, Polícia 190 (criança desaparecida), **CVV 188** (para a mãe), CAPSi, CAPS e UPA mais próximos | Sempre visíveis, **sempre no topo quando há risco**, com endereço e rota. |

**Regras importantes:**
- **Em emergência, nunca há ranking pago.** A ordem é sempre por risco, depois por distância e disponibilidade. Os serviços públicos aparecem primeiro quando há risco à vida.
- A **localização só é usada no momento do pedido** e não fica salva no histórico, a não ser que a mãe permita.
- Mãos amigas e parceiros de plantão passam por **verificação** (identidade e, para profissionais, registro no conselho) e aceitam um termo de conduta.
- Toda ajuda pode ser **avaliada** depois. Um parceiro mal avaliado perde o selo de plantão.
- Há um **modo "criança desaparecida"**, com um passo a passo:
  1. ligar para o 190;
  2. avisar a rede e as mães próximas;
  3. compartilhar a foto e o cartão com quem está ajudando;
  4. verificar os lugares que a criança costuma procurar, como lugares com água e com o que ela gosta.

---

#### C. 📅 Agenda e lembretes
- **Compromissos:** terapias recorrentes (por exemplo, "fono toda terça às 14h"), consultas, exames, reuniões da escola e perícias do INSS.
- **Remédios:** horário e dose, com um botão **"Dei o remédio ✔"** que registra automaticamente no diário. Se não for confirmado, o app manda um novo lembrete gentil.
- **Prazos e vencimentos:**
  - renovação de laudo, receitas, CIPTEA e revisão do BPC;
  - prazo de resposta do plano de saúde e do protocolo na ANS;
  - prazos de processos.
- **Check-in depois da consulta:** "Como foi a consulta? O que o médico disse?". A resposta vira um registro no diário, com a opção de anexar a receita ao Cofre.
- **Agenda compartilhada** com a família (ver D). Cada compromisso tem um responsável: "quem leva o Davi na terapia hoje?".
- **Lembretes** por notificação e, no futuro, por WhatsApp.
- **Antecipação para a criança:** um compromisso pode virar um card na Rotina e uma História social. Por exemplo: "amanhã tem dentista" gera a história "Indo ao dentista".

---

#### D. 👨‍👩‍👧 Família conectada e 🏫 contato com a escola

**D.1 Papéis e permissões**

| Papel | Exemplos | O que pode fazer |
|---|---|---|
| **Responsável principal** | Mãe | Tudo, inclusive convidar e remover pessoas e excluir dados |
| **Corresponsável** | Pai | Tudo, menos excluir a conta |
| **Cuidador** | Avós, babá, tia | Ver a rotina, o cartão, o SOS e a agenda; registrar no diário. **Não vê** documentos jurídicos nem o relatório de processos. |
| **Escola** | Professor, mediador, coordenação | Receber o relatório escolar e o cartão; usar o bilhete digital (ver D.3). Não vê o diário completo. |
| **Terapeuta** | Fono, TO, psicólogo | Receber um relatório ou um **link temporário** (expira em 7 dias); no futuro, deixar anotações e "tarefas de casa". |

**D.2 Dividir a carga**
- **Quadro "Quem faz o quê"**, dividindo terapias, remédios, escola, banho e noite.
- **Resumo semanal da carga**, que mostra quantas tarefas cada um fez na semana. Isso ajuda a tornar visível o trabalho invisível da mãe, sem culpar ninguém.
- Notificações para o responsável do dia ("Hoje é você quem leva o Davi na fono, às 14h").

**D.3 Contato com a escola**
- **Bilhete digital:** a escola preenche em 1 minuto como foi o dia (humor, alimentação, crises, conquistas, um recado). A escola acessa **por link, sem precisar criar conta**. O bilhete entra no diário da criança.
- **Recados família ↔ escola**, com histórico e confirmação de leitura.
- **Relatório escolar em PDF** (seção 7.3) e o **cartão da criança** para a escola.
- **Modelo de PEI** (Plano Educacional Individualizado) para preencher junto com a escola.
- **Checklist de direitos na escola:** matrícula, profissional de apoio, adaptações e avaliação adaptada, com modelos de pedido formal.
- **Agenda escolar:** reuniões, eventos e mudanças de rotina, como passeios e festas. Isso evita surpresas para a criança.

---

#### E. 💜 Cuidado com a saúde da mãe e 💼 trabalho e renda

**E.1 Cuidar de quem cuida**
- **Check-in semanal de 1 minuto:** "Como você está de 0 a 10?", "Dormiu bem?", "Teve algum momento para você?".
  - Opcionalmente, usa **questionários curtos validados** de ansiedade e humor, sempre com o aviso de que **não é diagnóstico**.
  - Se o resultado indicar sofrimento, o app oferece apoio e encaminhamento.
- **Trilha "Cuidar de mim"** com áudios de 3 a 5 minutos: respiração, como lidar com a culpa, autocompaixão, sono da mãe, como pedir ajuda e luto pelo filho idealizado.
- **"Pausa garantida":** a mãe pede ao clã ou à família uma folga de 2 horas por semana, e o app ajuda a organizar quem fica com a criança.
- **Apoio profissional:**
  - psicólogos **parceiros com preço social para mães**;
  - grupos terapêuticos online;
  - encaminhamento para a UBS e o CAPS.
- **Sinais de alerta:** se a mãe relatar desesperança ou pensar em se machucar, o app mostra imediatamente o **CVV 188**, o CAPS mais próximo e a opção de avisar alguém de confiança.

**E.2 Trabalho e renda**
- **Vagas flexíveis:** empresas parceiras publicam vagas em home office, meio período ou com horário flexível, e ganham o selo de "Empresa amiga das mães atípicas".
- **Cursos gratuitos e capacitação:** curadoria de cursos de instituições parceiras, como o Sistema S e plataformas de ensino.
- **Feira das mães:** uma vitrine para as mães do app venderem seus produtos e serviços (doces, artesanato, costura, serviços), com destaque gratuito.
- **Orientação sobre direitos ligados ao trabalho e à renda:**
  - BPC e o que acontece se a família passar a ter renda;
  - **horário especial para servidores públicos** com filho com deficiência (Lei 13.370/2016);
  - outros direitos, com revisão jurídica.
- **Mentoria de recolocação** com voluntários de RH de empresas parceiras.

---

#### F. 🤖 Assistente com IA (futuro, fase 3)
- **Como funciona:** a IA responde **só com base no conteúdo revisado do app** (blog, guia, atividades, direitos). Essa técnica se chama RAG, ou busca em base própria. Toda resposta mostra **de qual conteúdo veio**, com um link.
- **Exemplos de uso:**
  - "Meu filho só come arroz branco, o que posso tentar?";
  - "Como peço a negativa do plano por escrito?";
  - "O que levar na consulta com o neuropediatra?".
- **O que ela NÃO faz:**
  - não diagnostica;
  - não indica nem ajusta remédios ou doses;
  - não substitui o terapeuta;
  - não responde sobre assuntos fora da base revisada. Nesse caso, diz "não tenho essa informação revisada" e sugere a quem perguntar.
- **Segurança:**
  - se detectar risco (crise grave, criança desaparecida, mãe em sofrimento), a IA **abre o SOS ou a Rede de ajuda próxima** e mostra os telefones de emergência;
  - as conversas não são usadas para anúncios;
  - os dados de saúde não são enviados sem consentimento.
- **Qualidade:**
  - o conselho científico testa a IA antes do lançamento com uma lista de perguntas difíceis;
  - as respostas podem ser avaliadas ("ajudou" ou "não ajudou");
  - as respostas mal avaliadas são revisadas por pessoas.
- **Opção do diário (com permissão):** a mãe pode pedir "resuma os últimos 30 dias do Davi para eu levar ao médico", e a IA usa os registros dela para montar o resumo.

---

## 13. Modelo de negócio

**Objetivo do negócio:** ter o **máximo de clientes** possível para valorizar e vender a empresa a médio e longo prazo.
**Modelo principal:** assinatura mensal acessível, complementada por parceiros, empresas, governo e editais.

### Planos (proposta inicial, a validar com as mães)

| Plano | Preço | O que inclui |
|---|---|---|
| **Teste grátis** | 7 dias | Tudo do plano Completo |
| **Básico** (porta de entrada) | **R$ 9,90/mês** | Hoje, Rotina, Atividades, Diário (registros e gráficos), Agenda e lembretes, Aprender (blog) |
| **Essencial** | **R$ 29,90/mês** | Tudo do Básico + relatórios em PDF, Clã, Guia do tratamento completo, Família conectada e descontos do Hub de parceiros |
| **Completo** | **R$ 49,90/mês** | Tudo do Essencial + mãe-guia e encontros semanais, ponte com a escola, relatório jurídico, cofre de documentos, Rede de ajuda completa e, no futuro, o assistente com IA |
| **Assinatura patrocinada** | R$ 0 para a família | Plano pago por empresas, projetos ESG ou prefeituras para famílias de baixa renda (por exemplo, inscritas no CadÚnico) |

**Sempre grátis, mesmo sem assinatura:** SOS Crise e Cartão da criança com QR code (página de emergência). São recursos de segurança e também **ferramentas de divulgação**: cada cartão lido mostra a marca do app.

> **Atenção ao preço:** 73% das famílias já citam o custo do tratamento como problema (Genial Care, 2023). Por isso o plano de R$ 9,90, o teste grátis, a assinatura patrocinada e os descontos dos parceiros são importantes. **Testar o preço nas entrevistas da fase 0**, perguntando às mães quanto pagariam e por quais recursos.

### Estratégia de crescimento (para maximizar a base)
- **Entrada barata:** o plano de R$ 9,90 e 7 dias grátis reduzem a barreira para começar.
- **Recursos grátis que espalham a marca:** o SOS e o cartão com QR.
- **Indicação entre mães:** convidar outra mãe dá 1 mês grátis para as duas.
- **Canais parceiros:** clínicas, terapeutas, escolas e associações (AMA, APAE) indicam o app às famílias.
- **Venda em grupo:** empresas (benefício corporativo) e prefeituras trazem muitas famílias de uma vez.
- **Conteúdo:** o blog e as redes sociais atraem mães que buscam informação confiável.
- **Plano anual com desconto** (opcional): aumenta a permanência.

### O que valoriza a empresa numa venda futura
- **Mães ativas por mês** e crescimento da base.
- **Assinantes pagantes** e **receita recorrente mensal** (MRR).
- **Cancelamento** baixo (churn) e tempo médio de assinatura.
- **Custo para conquistar cada mãe** (CAC) comparado ao quanto ela paga ao longo do tempo (LTV).
- **Marca confiável**, conteúdo revisado por profissionais e **dados protegidos pela LGPD**.
- **Possíveis compradores:** healthtechs, redes de clínicas, operadoras de saúde e empresas de benefícios corporativos.

> **Importante sobre dados:** os dados de saúde das crianças **nunca** podem ser vendidos separadamente. Numa venda da empresa, quem compra assume as mesmas obrigações da LGPD e precisa respeitar o consentimento dado pelas famílias. A confiança das mães é o que dá valor ao app.

### Fontes de receita complementares

| Fonte | Como funciona | Quando |
|---|---|---|
| **Hub de parceiros** | Mensalidade da vitrine por plano (Básico e Destaque), anúncio patrocinado na categoria e comissão por cupom resgatado ou consulta agendada | A partir da fase 2 |
| **Patrocínio institucional / ESG** | Empresas patrocinam clãs, trilhas, eventos ou "bolsas de terapia" | A partir da fase 1 |
| **Benefício corporativo (B2B)** | Empresas pagam por funcionário para oferecer o app e os descontos aos pais | Fase 2 e 3 |
| **Governo (B2G)** | Prefeituras e secretarias de saúde e de educação licenciam o app para as famílias do município, com um painel de dados anônimos | Fase 3 |
| **Editais e fundações** | FAPESP PIPE, Finep, fundações de impacto e aceleradoras sociais | Desde o início |
| **Apoiador voluntário** | Quem pode contribui com um valor mensal opcional, que paga a assinatura de outra família | Fase 2 |

### O que NÃO fazer
- Vender dados das famílias.
- Cobrar pelo SOS Crise ou pelo cartão de emergência.
- Apagar ou bloquear os registros do diário de quem cancelar a assinatura: a mãe sempre pode ver e baixar o que já registrou.
- Aceitar anunciantes que violem a política da seção 9.5.

---

## 14. Segurança, ética e LGPD

### Dados sensíveis
Dados de saúde de criança são **dados sensíveis** e **dados de criança** pela LGPD (art. 11 e 14). Isso exige:
- **consentimento específico** do responsável, em linguagem simples;
- **minimização:** coletar só o necessário;
- **criptografia** em trânsito e armazenada;
- **separação total** entre os dados de saúde (diário) e o sistema de parceiros e anúncios;
- o direito de **baixar e apagar todos os dados** com um botão;
- um encarregado de dados (DPO) nomeado e uma política de privacidade clara;
- um relatório de impacto (RIPD) antes do lançamento.

### Avisos clínicos
- O app **não diagnostica** e **não substitui** profissionais. Isso aparece no cadastro, no PDF, no M-CHAT e nas atividades.
- As atividades são orientações educativas, revisadas pelo conselho científico.

### Proteção da criança
- Fotos de crianças ficam só em espaços fechados.
- Nenhuma criança tem perfil próprio. O perfil é sempre do responsável.
- Há um canal de denúncia para suspeita de maus-tratos (Disque 100).

### Respeito à comunidade autista
- Adultos autistas participam do conselho científico e da revisão do conteúdo.
- A linguagem é respeitosa: "criança autista" ou "criança com TEA", conforme a preferência da família, e nunca "doença" ou "sofre de autismo".

---

## 15. Tecnologia

### Escolha: PWA (aplicativo web instalável) na primeira versão
- **Mais acessível:** abre por um link no WhatsApp e se instala na tela inicial, sem loja e sem ocupar muito espaço.
- **Funciona offline:** a rotina, o diário, as atividades baixadas e o SOS funcionam sem internet e sincronizam depois.
- **Um código só:** Android, iPhone e computador.
- **Depois:** publicar nas lojas com Capacitor ou TWA, usando o mesmo código.

### Arquitetura sugerida

| Camada | Tecnologia sugerida |
|---|---|
| Interface | React + TypeScript (Vite ou Next.js), com design acessível e fonte grande |
| Armazenamento offline | IndexedDB, com sincronização |
| Back-end | Supabase (banco Postgres, login por celular, arquivos, regras de segurança por linha) ou Firebase |
| PDF | Gerado no aparelho (pdf-lib, jsPDF ou react-pdf) |
| Notificações | Web Push (no iPhone, só depois de instalar o app) e lembretes por WhatsApp no futuro |
| Blog | Um gerenciador de conteúdo para a equipe editorial (Markdown ou CMS headless) |
| Vídeo e áudio | Arquivos leves, comprimidos, com opção de baixar para usar offline |
| Moderação | Filtro automático, fila de denúncias e painel do moderador |
| Painel administrativo | Gestão de parceiros, cupons, conteúdo, clãs e métricas |

### Principais entidades de dados
- **Família:** responsáveis, convidados e permissões.
- **Criança:** perfil, cartão e preferências sensoriais.
- **Registro do diário:** tipo, data, campos do tipo e anexos.
- **Rotina:** etapas, pictogramas, horários e conclusões.
- **Atividade:** objetivo, idade, passos, mídia e conclusões.
- **Clã:** integrantes, mãe-guia, posts, pedidos de ajuda e encontros.
- **Parceiro:** verificação, ofertas, cupons, resgates e avaliações.
- **Artigo:** seção, semáforo, fontes, revisor e data de revisão.
- **Documento:** um arquivo no cofre, com tipo e validade.
- **Cartão:** campos visíveis escolhidos pela mãe, link público revogável e histórico de leituras do QR.
- **Contato de ajuda:** a rede pessoal, as Mãos amigas (voluntárias verificadas, com região aproximada) e os parceiros de plantão (horários e disponibilidade).
- **Pedido de ajuda:** tipo, momento e quem respondeu. A localização é usada só no momento do pedido.
- **Compromisso:** tipo (terapia, consulta, remédio, prazo), recorrência, responsável e confirmação.
- **Check-in da mãe:** respostas semanais, que são privadas e nunca são compartilhadas com o clã nem com parceiros.

---

## 16. Roteiro de lançamento

### Fase 0: Validação (antes de programar)
- [ ] Entrevistar de 15 a 20 mães (SUS e plano, capital e interior), incluindo **quanto pagariam** e por quais recursos.
- [ ] Fazer um protótipo clicável (Figma) das telas Hoje, Rotina, Diário e Clã e testar com 5 mães.
- [ ] Montar o conselho científico (de 4 a 6 pessoas, incluindo um adulto autista).
- [ ] Recrutar de 3 a 5 mães-guia para o piloto.
- [ ] Conseguir de 5 a 10 parceiros piloto para o hub, na mesma cidade.
- [ ] Definir o nome, registrar no INPI e criar a identidade visual.
- [ ] Fazer a revisão jurídica de LGPD e dos termos de uso.

### Fase 1: MVP (primeira versão no ar)
- [ ] Cadastro rápido e perfil da criança.
- [ ] **Hoje** (tela inicial).
- [ ] **Rotina** com modelos, timer, modo criança e músicas de rotina.
- [ ] **Atividades:** as 30 primeiras.
- [ ] **Diário** com os registros de crise, sono, alimentação, conquista e medicação.
- [ ] **Relatórios em PDF:** os modelos médico, escola e resumo.
- [ ] **SOS Crise**, completo e offline.
- [ ] **Cartão da criança com QR code**, com a página de emergência e o PDF para imprimir.
- [ ] **Rede de ajuda próxima** com as camadas 1 (minha rede) e 4 (serviços públicos).
- [ ] **Agenda e lembretes**, incluindo remédios com "Dei o remédio ✔".
- [ ] **Família conectada**, com os papéis de responsável, corresponsável e cuidador.
- [ ] **Cuidar de quem cuida**: check-in semanal, áudios curtos e encaminhamento ao CVV ou ao CAPS.
- [ ] **Clã:** piloto com 5 clãs e mães-guia.
- [ ] **Aprender:** os 20 primeiros posts e o Guia do tratamento.
- [ ] Piloto **gratuito** com 100 a 300 famílias em 1 ou 2 cidades, para validar o produto.

### Fase 2: Crescimento
- [ ] **Início das assinaturas** (Básico R$ 9,90, Essencial R$ 29,90 e Completo R$ 49,90), com teste de 7 dias, programa de indicação e assinatura patrocinada.
- [ ] **Hub de parceiros e benefícios**, com cupons, vitrine e avaliações.
- [ ] **Rede de ajuda próxima**, com as camadas 2 (Mães "Mão amiga") e 3 (**parceiros de plantão**), e o modo "criança desaparecida".
- [ ] Alerta de leitura do QR code e venda de pulseiras e etiquetas com QR pelos parceiros.
- [ ] **Contato com a escola:** bilhete digital, recados e modelo de PEI.
- [ ] **Trabalho e renda:** vagas flexíveis, cursos e Feira das mães.
- [ ] Relatório jurídico, **Direitos e modelos** e **Cofre de documentos**.
- [ ] **Mapa de serviços gratuitos**.
- [ ] Agenda e lembretes, e **Família conectada**.
- [ ] Fórum aberto, clãs temáticos e banco de trocas.
- [ ] Histórias sociais e prancha de comunicação.
- [ ] Expansão para mais cidades.

### Fase 3: Escala e impacto
- [ ] Ponte com a escola e diário compartilhado com terapeutas.
- [ ] Feedback por vídeo (a mãe filma a brincadeira e recebe orientação).
- [ ] Assistente com IA baseado no conteúdo revisado (seção 12.1-F).
- [ ] Parcerias com prefeituras e com o programa CST do Ministério da Saúde.
- [ ] Estudo de impacto com uma universidade.
- [ ] Publicação nas lojas (Google Play e App Store).

---

## 17. Métricas de sucesso

| Área | Métrica | Meta inicial |
|---|---|---|
| Ativação | Mães que fazem o 1º registro no diário em até 24 horas | > 60% |
| Uso | Registros no diário por família por semana | ≥ 4 |
| Uso | Atividades concluídas por semana | ≥ 3 |
| Retenção | Mães ativas 30 dias depois do cadastro | > 40% |
| Comunidade | Mães que participam do clã pelo menos 1x por semana | > 50% |
| Comunidade | Pedidos de ajuda respondidos em até 2 horas | > 80% |
| Valor | Relatórios em PDF gerados por mês | Acompanhar |
| Impacto | Estresse da mãe (escala curta), na entrada e após 3 meses | Redução |
| Impacto | Direitos conquistados com ajuda do app (BPC, CIPTEA, terapia) | Acompanhar |
| Satisfação | NPS (quanto a mãe recomendaria o app) | > 60 |
| Negócio | Mães ativas por mês (crescimento da base) | Acompanhar |
| Negócio | Conversão do teste grátis para um plano pago | > 20% |
| Negócio | Cancelamento mensal (churn) | < 8% |
| Negócio | Receita recorrente mensal, custo de aquisição (CAC) e valor do cliente ao longo do tempo (LTV) | LTV > 3x CAC |
| Negócio | Parceiros ativos e cupons resgatados | Acompanhar |

---

## 18. Riscos

| Risco | Como reduzir |
|---|---|
| Desinformação ou "curas" na comunidade | Política clara, moderação em 3 camadas, semáforo de evidência e posts de mitos e verdades |
| Anunciantes antiéticos | Política de parceiros, selo de verificação, avaliações das mães e lista de proibições |
| Vazamento de dados de saúde | Criptografia, separação dos dados, LGPD desde o início e auditoria |
| Mães-guia sobrecarregadas | Limite de clãs por guia, treinamento, apoio da equipe e bolsa ou benefícios |
| Abandono do app | Tarefas de 3 toques, conteúdo curto, clã ativo e lembretes gentis (sem culpa) |
| Celular simples e pouca internet | PWA leve, modo offline e mídia comprimida |
| Preço afastar famílias de baixa renda | Plano de R$ 9,90, teste grátis, assinatura patrocinada, descontos dos parceiros e SOS e cartão sempre grátis |
| Sustentabilidade financeira | Assinaturas mais receitas complementares (parceiros, ESG, B2B, B2G e editais) |
| Conteúdo clínico errado | Conselho científico, revisão obrigatória e data de revisão visível |
| Mau uso da Rede de ajuda próxima (alguém mal-intencionado se passando por "Mão amiga" ou parceiro) | Verificação de identidade e do registro profissional, localização sempre aproximada, termo de conduta, avaliação após cada ajuda e botão de denúncia |
| QR code do cartão expor dados da criança | A mãe escolhe os campos, não há endereço nem laudo, o link é revogável e há alerta de leitura |
| IA dar uma resposta errada ou perigosa | Respostas só da base revisada, bloqueio de diagnóstico e de doses, testes do conselho científico e revisão humana |
| Crítica da comunidade autista | Adultos autistas no conselho, linguagem respeitosa e foco em bem-estar, não em "normalizar" |

---

## 19. Próximos passos

1. **Revisar este documento** e decidir o que fica, o que sai e o que muda de prioridade.
2. **Escolher o nome** do app.
3. **Validar com as mães:** entrevistas e um protótipo das telas principais.
4. **Montar o conselho científico** e as primeiras mães-guia.
5. **Começar a programar o MVP** (fase 1) como PWA.

---

## 20. Fontes

**Intervenção mediada pelos pais e CST**
- Meta-análise de intervenção mediada pelos pais: https://pmc.ncbi.nlm.nih.gov/articles/PMC8078204
- Intervenção online mediada pelos pais (revisão de ensaios): https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9600965/
- Programa CST da OMS: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6859468/
- CST remoto no Brasil: https://public-pages-files-2025.frontiersin.org/journals/education/articles/10.3389/feduc.2025.1651973/text
- CST em Curitiba (UFPR): https://acervodigital.ufpr.br/handle/1884/76709
- Investimento do Ministério da Saúde no CST: https://viva.com.br/saude-e-bem-estar/tea-ministerio-da-saude-preve-r-13-mi-para-formar-familias-e-cuidadores.html
- Telessaúde com terapeuta x sem acompanhamento: https://insar.confex.com/insar/2018/webprogram/Paper27415.html
- NDBIs mediadas pelos pais (meta-análise em rede, 2024): https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11044316/
- PASS / PASS Plus: https://www.isrctn.com/ISRCTN21454676

**Exercício físico**
- Meta-análise de 2025 (ensaios randomizados): https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11903732/
- Exercício e comportamento repetitivo (2025): https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2025.1579345/pdf
- Meta-análise em rede (2023): https://link.springer.com/10.1007/s40489-023-00418-x
- Meta-análise de 2020: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7142971/

**Música e sensorial**
- Revisão Cochrane 2022 (musicoterapia): https://cochranelibrary.com/cdsr/doi/10.1002/14651858.CD004381.pub4/pdf/CDSR/CD004381/CD004381_abstract.pdf
- Estudo TIME-A (JAMA 2017): https://eprints.lse.ac.uk/84028
- Hiperacusia no autismo: https://entandaudiologynews.com/media/37240/entja24-danesh-final.pdf
- Abafadores de ruído: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6863142/

**Segurança: fuga e desaparecimento**
- Anderson et al., *Pediatrics* 2012, sobre fuga em crianças autistas (49% tentaram pelo menos uma vez): https://sciencedaily.com/releases/2012/10/121008082650.htm · https://iacc.hhs.gov/publications/summary-of-advances/2012/question5.shtml

**Falsas curas**
- Alerta da Anvisa sobre o MMS: https://www.jb.com.br/ciencia_e_tecnologia/2019/05/1001626-vendida-como-cura-milagrosa-para-autismo---mms--gera-alerta-entre-pais-e-governo.html
- Checagem "É falso que MMS cura autismo": https://www.aosfatos.org/noticias/falso-mms-cura-autismo-cancer/

**Dados sobre as famílias:** ver `pesquisa-dores-pais-de-autistas.md`.
