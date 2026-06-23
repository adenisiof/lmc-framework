# LMC-EDU — Especificação Educacional da Linguagem de Marcação Conceitual

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo educacional
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-EDU.md`

---

## 1. Definição

A **LMC-EDU** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à organização de processos educacionais com apoio de Inteligência Artificial.

Sua função é estruturar solicitações relacionadas ao ensino, aprendizagem, planejamento, avaliação, recuperação, intervenção pedagógica, relatórios escolares e acompanhamento do desenvolvimento dos estudantes.

A LMC-EDU não se limita à geração de textos escolares. Ela organiza o raciocínio pedagógico por meio de blocos como turma, conteúdo, habilidade, objetivo de aprendizagem, diagnóstico, dificuldade, metodologia, intervenção, avaliação e evidências.

A LMC-EDU pode ser combinada com a LMC-DOC para produzir documentos educacionais formais, como relatórios docentes, planos de aula e pareceres pedagógicos.

---

## 2. Finalidade da LMC-EDU

A LMC-EDU tem como finalidade auxiliar professores, coordenadores, gestores e profissionais da educação a organizar melhor suas demandas pedagógicas antes de solicitar apoio da IA.

Ela pode ser usada para criar:

```txt
planos de aula
sequências didáticas
relatórios docentes
relatórios de turma
relatórios individuais
atividades avaliativas
atividades de recuperação
intervenções pedagógicas
roteiros de aula
projetos educacionais
análise de desempenho
rubricas
critérios de avaliação
adaptações para alunos com dificuldades
registros de acompanhamento
```

A LMC-EDU busca transformar observações pedagógicas dispersas em uma estrutura clara, permitindo que a IA ajude na organização, escrita, análise ou planejamento sem substituir a decisão profissional do professor.

---

## 3. Problema que a LMC-EDU busca resolver

Demandas educacionais costumam envolver muitos elementos ao mesmo tempo: turma, conteúdo, habilidade, nível dos alunos, dificuldade observada, objetivo da aula, estratégia, avaliação e intervenção.

Quando o pedido é feito apenas em linguagem natural aberta, podem ocorrer problemas como:

```txt
plano de aula genérico
atividade fora do nível da turma
relatório com linguagem inadequada
objetivo de aprendizagem pouco claro
intervenção desconectada da dificuldade real
avaliação sem critério definido
excesso de termos pedagógicos vazios
criação de informações não observadas pelo professor
confusão entre diagnóstico, intervenção e resultado
```

A LMC-EDU reduz esses problemas ao organizar a solicitação em campos pedagógicos claros.

---

## 4. Relação com a LMC-CORE

A LMC-EDU herda as regras gerais da **LMC-CORE**, especialmente:

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[CONTEXTO]
[PAPEL_DA_IA]
[PÚBLICO_ALVO]
[ENTRADA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

A LMC-EDU acrescenta tags específicas para o contexto educacional:

```txt
[ETAPA_ESCOLAR]
[ANO_SERIE]
[COMPONENTE_CURRICULAR]
[TURMA]
[CONTEÚDO]
[HABILIDADES]
[OBJETIVOS_DE_APRENDIZAGEM]
[CONHECIMENTOS_PREVIOS]
[DIAGNOSTICO]
[DIFICULDADES]
[METODOLOGIA]
[INTERVENÇÃO_PEDAGÓGICA]
[ATIVIDADE]
[AVALIAÇÃO]
[RECUPERAÇÃO]
[EVIDÊNCIAS]
[RELATÓRIO_PEDAGÓGICO]
```

---

## 5. Princípios da LMC-EDU

### P1. Aprendizagem antes da atividade

Antes de criar uma atividade, a IA deve compreender o que o aluno precisa aprender.

### P2. Diagnóstico antes da intervenção

Antes de propor recuperação ou intervenção, a dificuldade observada deve estar descrita.

### P3. Contexto da turma

A IA deve considerar etapa escolar, ano/série, componente curricular e perfil da turma.

### P4. Clareza pedagógica

Objetivos, estratégias e avaliações devem estar alinhados.

### P5. Professor como validador

A IA pode sugerir, organizar e redigir, mas a decisão pedagógica final é do professor.

### P6. Não inventar dados de alunos

A IA não deve criar informações sobre estudantes, turma, comportamento ou desempenho que não tenham sido fornecidas.

### P7. Linguagem adequada

A linguagem deve se ajustar ao público: aluno, família, gestão, coordenação ou equipe docente.

### P8. Intervenção coerente

Toda intervenção deve estar ligada a uma dificuldade identificada.

### P9. Avaliação verificável

A avaliação deve indicar como será observado se houve aprendizagem.

### P10. Inclusão e adaptação

Quando solicitado, a IA deve propor adaptações sem rotular ou expor o estudante.

---

## 6. Estrutura mínima da LMC-EDU

A estrutura mínima é:

```txt
[OBJETIVO]
    o que precisa ser produzido ou organizado

[CONTEXTO]
    situação pedagógica

[SAÍDA]
    produto esperado
```

Exemplo:

```txt
[OBJETIVO]
    Criar uma atividade de recuperação sobre equações do 1º grau.

[CONTEXTO]
    A turma apresenta dificuldade em interpretar problemas e montar a equação correspondente.

[SAÍDA]
    gerar uma atividade com 5 questões progressivas e gabarito comentado.
```

---

## 7. Estrutura recomendada da LMC-EDU

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[ETAPA_ESCOLAR]
[ANO_SERIE]
[COMPONENTE_CURRICULAR]
[TURMA]
[CONTEÚDO]
[HABILIDADES]
[OBJETIVOS_DE_APRENDIZAGEM]
[CONHECIMENTOS_PREVIOS]
[DIAGNOSTICO]
[DIFICULDADES]
[METODOLOGIA]
[INTERVENÇÃO_PEDAGÓGICA]
[ATIVIDADE]
[AVALIAÇÃO]
[RECUPERAÇÃO]
[EVIDÊNCIAS]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Nem todas as tags precisam ser usadas em toda solicitação. Para relatórios, algumas tags podem ser mais importantes; para planos de aula, outras.

---

## 8. [ETAPA_ESCOLAR]

Define a etapa de ensino.

Exemplos:

```txt
Educação Infantil
Ensino Fundamental I
Ensino Fundamental II
Ensino Médio
Educação de Jovens e Adultos
Ensino Técnico
Ensino Superior
```

Exemplo:

```txt
[ETAPA_ESCOLAR]
    Ensino Fundamental II
```

---

## 9. [ANO_SERIE]

Define o ano ou série dos estudantes.

Exemplo:

```txt
[ANO_SERIE]
    8º ano
```

---

## 10. [COMPONENTE_CURRICULAR]

Define a disciplina ou área do conhecimento.

Exemplos:

```txt
Matemática
Língua Portuguesa
Ciências
História
Geografia
Arte
Educação Física
Tecnologia
Projeto de Vida
```

Exemplo:

```txt
[COMPONENTE_CURRICULAR]
    Matemática
```

---

## 11. [TURMA]

Define informações gerais da turma.

Modelo:

```txt
[TURMA]
    identificação>
        8º ano B

    perfil>
        turma participativa, mas com dificuldades em interpretação de problemas

    observações>
        parte dos alunos apresenta defasagem em operações básicas
```

A tag `[TURMA]` não deve conter dados sensíveis ou identificação desnecessária de alunos.

---

## 12. [CONTEÚDO]

Define o conteúdo trabalhado.

Exemplo:

```txt
[CONTEÚDO]
    equações do 1º grau
```

Outro exemplo:

```txt
[CONTEÚDO]
    porcentagem, razão e proporção
```

---

## 13. [HABILIDADES]

Define habilidades curriculares ou competências a serem desenvolvidas.

Exemplo:

```txt
[HABILIDADES]
    resolver problemas envolvendo equações do 1º grau
    interpretar situações-problema
    representar informações por meio de expressões algébricas
```

Quando o código oficial da habilidade não for informado, a IA não deve inventar códigos. Pode apenas descrever a habilidade em linguagem pedagógica.

---

## 14. [OBJETIVOS_DE_APRENDIZAGEM]

Define o que os estudantes devem aprender.

Modelo:

```txt
[OBJETIVOS_DE_APRENDIZAGEM]
    objetivo>
        compreender o conceito de equação como igualdade

    objetivo>
        resolver equações simples usando operações inversas

    objetivo>
        interpretar problemas e montar equações correspondentes
```

Os objetivos devem ser observáveis e relacionados ao conteúdo.

---

## 15. [CONHECIMENTOS_PREVIOS]

Define conhecimentos necessários para a aula ou atividade.

Exemplo:

```txt
[CONHECIMENTOS_PREVIOS]
    operações básicas
    noção de igualdade
    leitura e interpretação de enunciados
    uso de letras para representar valores desconhecidos
```

Essa tag ajuda a IA a perceber lacunas que podem prejudicar a aprendizagem.

---

## 16. [DIAGNOSTICO]

Define a leitura inicial feita pelo professor sobre a turma, aluno ou situação.

Exemplo:

```txt
[DIAGNOSTICO]
    Os alunos conseguem realizar cálculos simples, mas apresentam dificuldade em interpretar o enunciado e transformar a situação em expressão matemática.
```

O diagnóstico deve se basear em observações reais do professor.

---

## 17. [DIFICULDADES]

Define dificuldades específicas observadas.

Modelo:

```txt
[DIFICULDADES]

    dificuldade>
        descrição>
            dificuldade em interpretar o que o problema pede

        possível_causa>
            leitura superficial do enunciado

        impacto>
            o aluno não consegue montar a equação corretamente
```

Exemplo compacto:

```txt
[DIFICULDADES]
    dificuldade em interpretar problemas
    dificuldade em usar operações inversas
    dificuldade em justificar o raciocínio
```

---

## 18. [METODOLOGIA]

Define como o ensino será conduzido.

Exemplos:

```txt
aula expositiva dialogada
resolução de problemas
roda de discussão
investigação guiada
aprendizagem por projetos
atividade em grupo
intervenção individual
uso de perguntas norteadoras
```

Exemplo:

```txt
[METODOLOGIA]
    investigação guiada com perguntas norteadoras, partindo de situações-problema antes da apresentação da fórmula
```

---

## 19. [PERGUNTAS_NORTEADORAS]

Define perguntas usadas para conduzir a reflexão do aluno.

Exemplo:

```txt
[PERGUNTAS_NORTEADORAS]
    O que o problema está pedindo?
    Quais informações são importantes?
    O que é desconhecido?
    Como podemos representar essa informação?
    Existe uma relação de igualdade?
    Como podemos verificar se a resposta faz sentido?
```

Essa tag é especialmente importante para metodologias baseadas em investigação, Pólya, resolução de problemas e construção progressiva do raciocínio.

---

## 20. [INTERVENÇÃO_PEDAGÓGICA]

Define ações para superar dificuldades.

Modelo:

```txt
[INTERVENÇÃO_PEDAGÓGICA]

    intervenção>
        dificuldade_relacionada>
            interpretação de problemas

        ação>
            propor leitura guiada do enunciado com identificação de dados relevantes

        objetivo>
            ajudar o aluno a reconhecer informações importantes antes de calcular
```

A intervenção deve estar ligada ao diagnóstico e às dificuldades observadas.

---

## 21. [ATIVIDADE]

Define uma atividade a ser produzida ou organizada.

Modelo:

```txt
[ATIVIDADE]
    tipo>
        lista de exercícios

    quantidade_questões>
        5

    nível>
        progressivo

    orientação>
        começar com questões simples e avançar para problemas contextualizados

    incluir_gabarito>
        sim

    incluir_comentários>
        sim
```

---

## 22. [AVALIAÇÃO]

Define como a aprendizagem será verificada.

Modelo:

```txt
[AVALIAÇÃO]
    tipo>
        formativa

    critérios>
        interpretação correta do problema
        montagem adequada da equação
        resolução correta
        justificativa do raciocínio

    instrumento>
        atividade escrita e observação durante a aula
```

A avaliação deve estar alinhada aos objetivos de aprendizagem.

---

## 23. [RECUPERAÇÃO]

Define ações de retomada para alunos com dificuldade.

Exemplo:

```txt
[RECUPERAÇÃO]
    retomar conhecimentos prévios
    usar exemplos resolvidos passo a passo
    propor questões com menor carga textual
    aumentar gradualmente a complexidade
    acompanhar a resolução com perguntas orientadoras
```

---

## 24. [EVIDÊNCIAS]

Define quais sinais indicam aprendizagem, dificuldade ou progresso.

Exemplo:

```txt
[EVIDÊNCIAS]
    aluno identifica o que o problema pede
    aluno separa dados relevantes
    aluno monta a equação corretamente
    aluno resolve usando operações inversas
    aluno explica o raciocínio com suas palavras
```

Essa tag ajuda a transformar observações do professor em critérios verificáveis.

---

## 25. [RELATÓRIO_PEDAGÓGICO]

Define informações para geração de relatório educacional.

Modelo:

```txt
[RELATÓRIO_PEDAGÓGICO]
    tipo>
        relatório de turma

    finalidade>
        registrar desempenho e dificuldades observadas

    foco>
        aprendizagem, participação e intervenções realizadas

    tom>
        formal, objetivo e pedagógico
```

A LMC-EDU pode usar essa tag junto com a LMC-DOC para gerar relatórios mais formais.

---

## 26. [ADAPTAÇÕES]

Define adaptações pedagógicas quando necessário.

Exemplo:

```txt
[ADAPTAÇÕES]
    reduzir quantidade de questões
    usar enunciados mais objetivos
    permitir apoio visual
    oferecer exemplo resolvido antes da atividade
    acompanhar a leitura do enunciado
```

As adaptações devem ser descritas sem exposição indevida do aluno.

---

## 27. [BNCC_REFERÊNCIA]

Define referência curricular, quando informada pelo professor.

Exemplo:

```txt
[BNCC_REFERÊNCIA]
    habilidade informada pelo professor ou descrição da habilidade trabalhada
```

Regra:

```txt
se o código da habilidade não for informado, a IA não deve inventar código oficial
```

A IA pode sugerir uma descrição aproximada, mas deve deixar claro quando não houver código fornecido.

---

## 28. [LINGUAGEM_DO_RELATÓRIO]

Define o tom usado em relatórios escolares.

Exemplos:

```txt
formal
objetivo
pedagógico
acolhedor
descritivo
institucional
sem julgamento pessoal
```

Exemplo:

```txt
[LINGUAGEM_DO_RELATÓRIO]
    formal, objetiva, pedagógica e sem exposição indevida dos estudantes
```

---

## 29. Modelo mínimo

```txt
[OBJETIVO]
    finalidade da solicitação pedagógica

[CONTEXTO]
    situação educacional

[SAÍDA]
    produto esperado
```

---

## 30. Modelo padrão

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar material educacional

    escopo>
        responder somente ao que foi solicitado

[PROJETO]
    nome_do_projeto

[ETAPA_ESCOLAR]
    etapa de ensino

[ANO_SERIE]
    ano ou série

[COMPONENTE_CURRICULAR]
    disciplina ou área

[TURMA]
    identificação>
        turma

    perfil>
        características gerais

[CONTEÚDO]
    conteúdo trabalhado

[HABILIDADES]
    habilidades ou competências trabalhadas

[OBJETIVOS_DE_APRENDIZAGEM]
    objetivo>
        objetivo 1

    objetivo>
        objetivo 2

[CONHECIMENTOS_PREVIOS]
    conhecimentos necessários

[DIAGNOSTICO]
    observação pedagógica inicial

[DIFICULDADES]
    dificuldades observadas

[METODOLOGIA]
    estratégia de ensino

[INTERVENÇÃO_PEDAGÓGICA]
    ações de intervenção

[AVALIAÇÃO]
    forma de verificar a aprendizagem

[CONTROLE]
    nivel>
        moderado

    saida>
        markdown

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não criar dados de alunos
    não inventar códigos de habilidades
    não usar linguagem acusatória
    não expor estudantes

[FORMATO]
    organização da resposta

[SAÍDA]
    produto final esperado
```

---

## 31. Exemplo — plano de aula de matemática

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        criar plano de aula

    escopo>
        responder somente com o plano solicitado

[PROJETO]
    plano_aula_equacao_primeiro_grau

[ETAPA_ESCOLAR]
    Ensino Fundamental II

[ANO_SERIE]
    8º ano

[COMPONENTE_CURRICULAR]
    Matemática

[CONTEÚDO]
    equações do 1º grau

[OBJETIVOS_DE_APRENDIZAGEM]
    objetivo>
        compreender equação como uma relação de igualdade

    objetivo>
        resolver equações simples usando operações inversas

    objetivo>
        interpretar situações-problema e representar valores desconhecidos

[CONHECIMENTOS_PREVIOS]
    operações básicas
    noção de igualdade
    leitura de enunciados
    representação de valores desconhecidos por letras

[DIAGNOSTICO]
    Os alunos apresentam dificuldade em interpretar problemas e transformar informações do enunciado em uma equação.

[DIFICULDADES]
    dificuldade em identificar o que o problema pede
    dificuldade em selecionar dados relevantes
    dificuldade em representar o valor desconhecido

[METODOLOGIA]
    resolução de problemas com investigação guiada e perguntas norteadoras

[PERGUNTAS_NORTEADORAS]
    O que o problema está pedindo?
    Qual informação é desconhecida?
    Quais dados são importantes?
    Como podemos representar o valor desconhecido?
    Existe uma relação de igualdade?
    Como podemos verificar se a resposta faz sentido?

[AVALIAÇÃO]
    tipo>
        formativa

    critérios>
        interpretação do enunciado
        montagem da equação
        resolução correta
        explicação do raciocínio

[CONTROLE]
    nivel>
        moderado

    saida>
        markdown

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não usar linguagem excessivamente técnica
    não criar habilidade BNCC com código não informado
    não propor atividade fora do nível do 8º ano

[FORMATO]
    organizar em: tema, objetivos, conhecimentos prévios, desenvolvimento, perguntas norteadoras, avaliação e recuperação

[SAÍDA]
    gerar um plano de aula completo e objetivo
```

---

## 32. Exemplo — relatório pedagógico de turma

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar relatório pedagógico

    escopo>
        responder somente com o relatório solicitado

[PROJETO]
    relatorio_turma_matematica

[ETAPA_ESCOLAR]
    Ensino Fundamental II

[ANO_SERIE]
    8º ano

[COMPONENTE_CURRICULAR]
    Matemática

[TURMA]
    identificação>
        8º ano

    perfil>
        turma com participação irregular e dificuldades na interpretação de problemas

[CONTEÚDO]
    porcentagem, razão e proporção

[DIAGNOSTICO]
    Parte dos alunos apresenta dificuldade em interpretar situações-problema, reconhecer relações proporcionais e justificar os procedimentos utilizados.

[DIFICULDADES]
    dificuldade em interpretar enunciados
    dificuldade em relacionar grandezas
    dificuldade em aplicar procedimentos de porcentagem
    dificuldade em explicar o raciocínio

[INTERVENÇÃO_PEDAGÓGICA]
    retomada dos conhecimentos prévios
    resolução comentada de problemas
    uso de perguntas norteadoras
    atividades progressivas
    acompanhamento durante a resolução

[EVIDÊNCIAS]
    alguns estudantes passaram a identificar melhor os dados principais
    parte da turma ainda necessita de apoio para organizar o raciocínio
    houve maior participação durante atividades guiadas

[LINGUAGEM_DO_RELATÓRIO]
    formal, objetiva, pedagógica e sem exposição de alunos individualmente

[CONTROLE]
    nivel>
        rigido

    saida>
        texto_limpo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não citar nomes de alunos
    não inventar resultados
    não usar linguagem negativa ou acusatória
    não criar dados que não foram informados
    não usar tópicos no relatório final

[FORMATO]
    texto em parágrafos curtos
    linguagem formal
    tom pedagógico
    adequado para registro escolar

[SAÍDA]
    gerar relatório pedagógico de turma
```

---

## 33. Regras de interpretação específicas da LMC-EDU

Ao receber uma instrução LMC-EDU, a IA deve:

1. Identificar o objetivo pedagógico da solicitação.
2. Considerar etapa escolar, ano/série e componente curricular.
3. Usar o contexto informado para limitar a resposta.
4. Não inventar dados sobre alunos, turma ou escola.
5. Não criar códigos oficiais de habilidades se não forem fornecidos.
6. Relacionar atividades aos objetivos de aprendizagem.
7. Relacionar intervenções às dificuldades diagnosticadas.
8. Adaptar a linguagem ao público-alvo.
9. Evitar linguagem acusatória, expositiva ou discriminatória.
10. Priorizar clareza pedagógica.
11. Preservar o papel do professor como validador final.
12. Quando houver relatório, usar tom formal, objetivo e institucional.
13. Quando houver atividade, respeitar nível de ensino e conteúdo.
14. Quando houver avaliação, apresentar critérios observáveis.
15. Quando houver recuperação, propor ações coerentes com as dificuldades.
16. Quando houver adaptação, evitar exposição indevida do estudante.
17. Respeitar as restrições fornecidas.
18. Produzir somente o que estiver definido em `[SAÍDA]`.

---

## 34. Critérios de qualidade educacional

Uma saída gerada com LMC-EDU deve ser avaliada pelos seguintes critérios:

```txt
aderência ao objetivo pedagógico
adequação à etapa escolar
adequação ao nível da turma
clareza dos objetivos de aprendizagem
coerência entre diagnóstico e intervenção
coerência entre conteúdo e atividade
qualidade das perguntas norteadoras
adequação da avaliação
linguagem respeitosa e profissional
ausência de dados inventados
respeito às restrições
utilidade prática para o professor
```

---

## 35. Relação com outros módulos

A LMC-EDU pode ser combinada com outros módulos da LMC.

Exemplos:

```txt
LMC-EDU + LMC-DOC
    relatórios escolares, planos de aula, pareceres e documentos pedagógicos

LMC-EDU + LMC-TEST
    avaliação de atividades, planos e relatórios gerados por IA

LMC-EDU + LMC-CODE
    criação de ferramentas educacionais, simuladores e atividades interativas

LMC-EDU + LMC-REQ
    levantamento de requisitos para sistemas educacionais

LMC-EDU + LMC-PROCESS
    organização de processos escolares, recuperação contínua e acompanhamento de aprendizagem
```

---

## 36. Limites da LMC-EDU

A LMC-EDU não substitui o professor, a coordenação pedagógica ou a análise institucional.

Ela não deve ser usada para criar diagnósticos clínicos, laudos ou afirmações sobre condições individuais de estudantes.

A LMC-EDU pode auxiliar na organização de observações pedagógicas, mas decisões sobre avaliação, promoção, adaptação curricular, encaminhamentos e intervenções devem ser validadas por profissionais responsáveis.

---

## 37. Definição acadêmica da LMC-EDU

A LMC-EDU pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à estruturação de processos educacionais mediados por Inteligência Artificial, organizando etapa escolar, turma, conteúdo, habilidades, objetivos de aprendizagem, conhecimentos prévios, diagnóstico, dificuldades, metodologias, intervenções, avaliações e evidências, com o objetivo de reduzir ambiguidades, melhorar a coerência pedagógica e apoiar o planejamento, a documentação e a tomada de decisão docente.

---

## 38. Síntese

A LMC-EDU organiza solicitações educacionais em blocos claros.

Sua função é ajudar o professor a comunicar melhor para a IA:

```txt
quem são os alunos
qual é o conteúdo
qual é o objetivo de aprendizagem
quais dificuldades foram observadas
quais conhecimentos prévios são necessários
qual metodologia será usada
qual intervenção faz sentido
como avaliar a aprendizagem
qual produto educacional deve ser gerado
```

A LMC-EDU não substitui o olhar pedagógico humano. Ela organiza esse olhar para que a IA auxilie com mais clareza, coerência e responsabilidade.

---

**Fim da especificação LMC-EDU**
