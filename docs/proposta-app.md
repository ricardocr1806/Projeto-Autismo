# Proposta do app: apoio gratuito para famílias de autistas sem plano de saúde

> Documento de produto baseado em evidências científicas. Complementa `pesquisa-dores-pais-de-autistas.md`.

## 1. Para quem é

Para **famílias que dependem do SUS** e não podem pagar plano ou terapia particular. Elas estão na fila do diagnóstico ou da terapia, ou recebem poucas horas de atendimento.
O usuário principal é **a mãe**, que costuma ter:
- celular Android simples;
- pouco espaço no aparelho e internet limitada;
- muito pouco tempo e muito cansaço.

**Promessa do app:** *"Enquanto a terapia não chega, e mesmo depois que chegar, você não está sozinha. Aqui você aprende a ajudar seu filho em casa, sabe exatamente qual é o próximo passo e garante os direitos dele de graça."*

## 2. O que os estudos nos ensinam e como isso vira produto

| Evidência | O que diz | Decisão de produto |
|---|---|---|
| **Intervenção mediada pelos pais** (meta-análise de 12 ensaios randomizados com 964 crianças; PACT) | Pais treinados conseguem melhorar a comunicação e o comportamento da criança. O efeito médio é de cerca de 0,76, e o PACT mostrou efeito duradouro anos depois. | O centro do app é **ensinar os pais a estimular a criança no dia a dia**, e não apenas oferecer conteúdo informativo. |
| **Programa CST da OMS** (Caregiver Skills Training) | Foi pilotado em Curitiba (UFPR), com redução média de 11,3 pontos na escala ATEC e 28 de 37 famílias concluindo. A versão remota foi bem aceita no Brasil. O Ministério da Saúde prevê cerca de R$ 13 milhões até 2030 para levá-lo ao SUS. | A trilha de treinamento segue a **estrutura do CST**: brincar, comunicação, rotina e comportamento. Há uma **oportunidade de parceria** para ser o apoio digital do CST no SUS. |
| **Divisão de tarefas** (PASS na Índia e no Paquistão; PASS Plus) | Profissionais que não são especialistas, quando treinados, conseguem aplicar a intervenção com os pais. | Criar a figura da **mãe-guia**: mães mais experientes, treinadas, que acompanham grupos pequenos. |
| **Programas sem acompanhamento humano** (revisão de telessaúde) | Quando os pais seguem o programa sozinhos, a **satisfação é menor e o abandono é maior** do que quando há um terapeuta junto. | O app **não pode ser só conteúdo**. Precisa de grupo, mentora e encontros ao vivo. |
| **Barreiras do CST remoto no Brasil** | Dificuldade com tecnologia e **sobrecarga dos cuidadores**. | Lições de **5 a 10 minutos**, em áudio ou vídeo curto, que funcionam offline, com linguagem simples e sem exigir cadastro longo. |
| **Feedback por vídeo** (PACT e PASS) | O pai filma a brincadeira e recebe orientação. Esse é o mecanismo central do PACT. | Na fase 2, a mãe grava 2 minutos de brincadeira e recebe o retorno de uma mãe-guia ou de um terapeuta voluntário. |
| **Desinformação** (FGV, 2025) | Cuidadores fragilizados são alvo de "curas" falsas. | Todo o conteúdo é **revisado por profissionais**, com as fontes visíveis e um alerta contra falsas curas. |

## 3. Módulos

### MVP (fase 1): os itens que resolvem as dores mais urgentes
1. **Meu caminho.** Uma trilha personalizada conforme a fase da família:
   - suspeita → UBS → regulação → CER ou CAPSi → laudo → terapia;
   - em cada passo, o que levar, o que pedir e como **pegar o protocolo**.
2. **Direitos grátis.** Checklist e guias para BPC/LOAS (CadÚnico), CIPTEA, passe livre, prioridade de atendimento, escola (matrícula e profissional de apoio) e **Defensoria Pública**. Inclui modelos de requerimento prontos para copiar ou imprimir.
3. **Aprender em casa.** Uma trilha semanal inspirada no CST, com uma lição curta e uma "missão da semana" (por exemplo, 10 minutos de brincadeira guiada por dia). Temas:
   - brincar junto e comunicação;
   - rotina visual (com pictogramas imprimíveis);
   - crises: entender o gatilho e o que fazer;
   - seletividade alimentar, sono e higiene/desfralde.
4. **Diário da criança.** Registro de crises, sono, alimentação e conquistas com poucos toques, que gera um **relatório em PDF** para levar à consulta, à escola ou à Defensoria.
5. **Onde tem atendimento grátis.** Mapa de CER, CAPSi, APAE, AMA, **clínicas-escola de universidades** (psicologia, fono e TO com atendimento gratuito) e ONGs.

### Fase 2: o apoio humano que a evidência pede
6. **Grupos com mãe-guia.** Grupos pequenos (8 a 10 mães), moderados, com um encontro online por semana.
7. **Feedback por vídeo** da brincadeira.
8. **Cuidar de quem cuida.** Check-in emocional, sinais de esgotamento e encaminhamento para o CAPS ou o CVV.
9. **Ponte com a escola.** Diário compartilhado com o professor ou mediador.

### Fase 3: escala
10. Parceria com secretarias de saúde e com o programa CST do Ministério da Saúde.
11. Estudo de impacto com uma universidade, para gerar evidência própria e acessar financiamento público.

## 4. Decisões técnicas sugeridas

- **PWA (aplicativo web instalável)** como primeira versão:
  - abre pelo link do WhatsApp, sem passar pela loja e sem ocupar espaço;
  - funciona offline (as lições e o diário ficam salvos no aparelho);
  - um único código serve para Android, iPhone e computador;
  - pode virar app de loja depois, com Capacitor ou TWA.
- **Login simples** por número de celular, ou uso anônimo no começo.
- **LGPD:** dados de saúde de criança são **dados sensíveis** (art. 11 e 14). Isso exige:
  - consentimento claro do responsável;
  - armazenamento local por padrão;
  - criptografia e nenhuma venda de dados.
- **Acessibilidade:** fonte grande, áudio em todas as lições e leitura fácil para baixa escolaridade.

## 5. Sustentabilidade (gratuito para a família)

- Editais de inovação e impacto social: FAPESP PIPE, Finep, fundações (por exemplo, a Fundação Banco do Brasil, que apoiou o Mapa Autismo Brasil) e programas de aceleração de impacto.
- Licença institucional para prefeituras e secretarias de saúde e de educação.
- Patrocínio ESG de empresas, que podem oferecer o app a funcionários pais.
- **Nunca** cobrar da família pelo essencial.

## 6. Cuidados éticos

- O app **não diagnostica** e **não substitui a terapia**. Ele orienta e prepara a família, e isso deve ficar claro em todas as telas.
- O conteúdo clínico deve ser **validado por um conselho de profissionais** (fono, TO, psicólogo e neuropediatra), e é importante incluir **adultos autistas** na revisão.
- Os materiais do CST da OMS têm licença própria. Antes de adaptar, é preciso **verificar a licença e buscar parceria** (OMS/OPAS, Ministério da Saúde, UFPR).

## 7. Como medir se está funcionando

- Quantas famílias concluem a trilha semanal (meta: mais de 60%, comparável aos 76% de conclusão do CST em Curitiba).
- Quantos direitos foram conquistados com ajuda do app (BPC, CIPTEA, vaga de terapia).
- O estresse da mãe antes e depois, medido por uma escala curta.
- A evolução da criança relatada pelos pais (diário e questionário simples).

## Fontes

- OMS, desenvolvimento do CST: [PMC6859468](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6859468/)
- CST remoto no Brasil: [Frontiers in Education, 2025](https://public-pages-files-2025.frontiersin.org/journals/education/articles/10.3389/feduc.2025.1651973/text)
- Ensaio do CST em Curitiba: [UFPR](https://acervodigital.ufpr.br/handle/1884/76709)
- Investimento do Ministério da Saúde no CST: [Viva](https://viva.com.br/saude-e-bem-estar/tea-ministerio-da-saude-preve-r-13-mi-para-formar-familias-e-cuidadores.html)
- CST online da OMS: [HPN](https://hpnonline.com/patient-satisfaction/patient-engagement-educational-programs/article/21262752/WHO’s training for caregivers of children with autism goes online)
- Capacitação de cuidadores no SUS (Mackenzie): [Psicologia: Teoria e Prática](https://pepsic.bvsalud.org/pdf/ptp/v24n3/0102-3772-ptp-24-03-ePTPCP14196.pdf)
- Meta-análise de intervenção mediada pelos pais: [PMC8078204](https://pmc.ncbi.nlm.nih.gov/articles/PMC8078204)
- Intervenção online mediada pelos pais (revisão de ensaios): [PMC9600965](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9600965/)
- Telessaúde com acompanhamento vs. sem acompanhamento: [INSAR 2018](https://insar.confex.com/insar/2018/webprogram/Paper27415.html)
- Cochrane, intervenção por telessaúde (protocolo): [CD014793](https://cochranelibrary.com/cdsr/doi/10.1002/14651858.CD014793)
- PASS / PASS Plus: [ISRCTN21454676](https://www.isrctn.com/ISRCTN21454676) · [NAMASTE](https://sites.manchester.ac.uk/namaste) · [Frontiers in Psychiatry, 2022](https://www.frontiersin.org/journals/psychiatry/articles/10.3389/fpsyt.2022.903341/full)
- App coreano de treinamento parental baseado em ABA: [JMIR Human Factors, 2024](https://humanfactors.jmir.org/2024/1/e52295)
- Ensaios de apps para pais: [NCT04992169](https://clinicaltrials.gov/study/NCT04992169) · [NCT05927116](https://clinicaltrials.gov/study/NCT05927116)
