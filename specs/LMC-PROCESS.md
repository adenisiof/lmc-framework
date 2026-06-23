# LMC-PROCESS — Especificação para Organização e Melhoria de Processos com Inteligência Artificial

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo de processos
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-PROCESS.md`

---

## 1. Definição

A **LMC-PROCESS** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à organização, descrição, análise, melhoria e padronização de processos com apoio de Inteligência Artificial.

Sua função é transformar uma atividade, rotina, fluxo de trabalho ou problema operacional em uma estrutura clara, permitindo que a IA ajude o usuário a compreender etapas, entradas, saídas, responsáveis, recursos, riscos, gargalos, indicadores e oportunidades de melhoria.

A LMC-PROCESS pode ser usada em processos educacionais, administrativos, industriais, comerciais, operacionais, técnicos, pedagógicos, produtivos ou organizacionais.

Fluxo conceitual:

```txt id="3sq93v"
Situação ou rotina
↓
LMC-PROCESS
↓
Processo estruturado
↓
Análise de gargalos
↓
Melhoria proposta
↓
Validação humana
```

A LMC-PROCESS não substitui a análise humana do processo. Ela organiza as informações para que a IA possa auxiliar com mais clareza, rastreabilidade e controle.

---

## 2. Finalidade da LMC-PROCESS

A LMC-PROCESS tem como finalidade estruturar processos de forma clara, verificável e melhorável.

Ela pode ser usada para organizar:

```txt id="vpu84l"
rotinas escolares
fluxos administrativos
processos industriais
processos de atendimento
processos de produção
processos de manutenção
processos de recuperação pedagógica
processos de aplicação de avaliações
processos de correção
processos de documentação
processos de desenvolvimento
processos de melhoria contínua
processos operacionais simples
```

A LMC-PROCESS ajuda o usuário a sair de uma descrição informal do tipo “fazemos assim” para uma estrutura mais clara:

```txt id="5dlj9m"
o que entra
quem faz
como faz
em qual ordem faz
com quais recursos
com quais regras
qual saída é esperada
como medir se funcionou
onde estão os problemas
como melhorar
```

---

## 3. Problema que a LMC-PROCESS busca resolver

Muitos processos existem apenas na prática, mas não estão bem descritos.

Isso gera problemas como:

```txt id="0113uc"
cada pessoa executa de um jeito
etapas ficam implícitas
responsabilidades não ficam claras
faltam critérios de qualidade
faltam indicadores
retrabalho não é identificado
gargalos são percebidos tarde
melhorias são feitas sem controle
a IA recebe uma descrição incompleta do processo
```

A LMC-PROCESS busca reduzir esses problemas por meio da estruturação explícita do fluxo de trabalho.

---

## 4. Relação com a LMC-CORE

A LMC-PROCESS herda as regras gerais da **LMC-CORE**, especialmente:

```txt id="makn9b"
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

A LMC-PROCESS acrescenta tags específicas para processos:

```txt id="mracjr"
[PROCESSO]
[TIPO_DE_PROCESSO]
[PROBLEMA_DO_PROCESSO]
[OBJETIVO_DO_PROCESSO]
[ESCOPO_DO_PROCESSO]
[ENTRADAS_DO_PROCESSO]
[SAÍDAS_DO_PROCESSO]
[ETAPAS]
[FLUXO]
[RESPONSÁVEIS]
[RECURSOS]
[REGRAS_OPERACIONAIS]
[PADRÃO_DE_EXECUÇÃO]
[INDICADORES]
[GARGALOS]
[RISCOS]
[MELHORIAS]
[VALIDAÇÃO]
[CICLO_DE_MELHORIA]
```

---

## 5. Princípios da LMC-PROCESS

### P1. Processo antes da solução

Antes de propor melhoria, é necessário compreender como o processo funciona atualmente.

### P2. Entrada, atividade e saída

Todo processo deve ser analisado considerando o que entra, o que é feito e o que sai.

### P3. Ordem das etapas

As etapas devem estar organizadas em sequência lógica.

### P4. Responsabilidade explícita

Sempre que possível, deve estar claro quem executa, acompanha ou valida cada etapa.

### P5. Padrão antes da melhoria

Antes de melhorar um processo, é necessário entender qual é o padrão atual ou desejado.

### P6. Gargalos visíveis

Pontos de atraso, retrabalho, erro ou perda devem ser registrados.

### P7. Indicadores verificáveis

Um processo deve possuir critérios ou indicadores que permitam avaliar se está funcionando.

### P8. Melhoria controlada

Melhorias devem estar ligadas a problemas identificados, não a suposições soltas.

### P9. Simplicidade operacional

A estrutura do processo deve ser simples o suficiente para ser usada por pessoas que executam o trabalho real.

### P10. Validação humana

A IA pode organizar e sugerir melhorias, mas a validação final deve ser feita por quem conhece o processo.

---

## 6. Estrutura mínima da LMC-PROCESS

A estrutura mínima é:

```txt id="zeqnx0"
[PROCESSO]
    nome do processo

[OBJETIVO]
    o que deve ser organizado ou melhorado

[SAÍDA]
    produto esperado
```

Exemplo:

```txt id="w2opez"
[PROCESSO]
    aplicação de avaliação escolar

[OBJETIVO]
    Organizar o processo de aplicação, recolhimento e correção das avaliações.

[SAÍDA]
    gerar fluxo do processo com etapas, responsáveis, riscos e melhorias.
```

---

## 7. Estrutura recomendada da LMC-PROCESS

```txt id="caamei"
[PROTOCOLO_DE_USO]
[PROJETO]
[PROCESSO]
[TIPO_DE_PROCESSO]
[PROBLEMA_DO_PROCESSO]
[OBJETIVO_DO_PROCESSO]
[CONTEXTO]
[ESCOPO_DO_PROCESSO]
[ENTRADAS_DO_PROCESSO]
[SAÍDAS_DO_PROCESSO]
[ETAPAS]
[FLUXO]
[RESPONSÁVEIS]
[RECURSOS]
[REGRAS_OPERACIONAIS]
[PADRÃO_DE_EXECUÇÃO]
[INDICADORES]
[GARGALOS]
[RISCOS]
[MELHORIAS]
[VALIDAÇÃO]
[CICLO_DE_MELHORIA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Nem todas as tags precisam ser usadas em todo processo. Para processos simples, a estrutura pode ser reduzida.

---

## 8. [PROCESSO]

A tag `[PROCESSO]` define o nome do processo analisado.

Exemplo:

```txt id="k8ulk9"
[PROCESSO]
    recuperação contínua em matemática
```

Outro exemplo:

```txt id="a00k1v"
[PROCESSO]
    atendimento de solicitação de manutenção
```

---

## 9. [TIPO_DE_PROCESSO]

A tag `[TIPO_DE_PROCESSO]` classifica o processo.

Valores possíveis:

```txt id="p4jtf6"
educacional
administrativo
industrial
operacional
comercial
técnico
pedagógico
produtivo
logístico
documental
desenvolvimento
melhoria contínua
```

Exemplo:

```txt id="kwcz34"
[TIPO_DE_PROCESSO]
    educacional
```

---

## 10. [PROBLEMA_DO_PROCESSO]

A tag `[PROBLEMA_DO_PROCESSO]` descreve o problema, falha, dificuldade ou necessidade de melhoria.

Exemplo:

```txt id="nwhnio"
[PROBLEMA_DO_PROCESSO]
    Os alunos apresentam dificuldades recorrentes em matemática, mas as ações de recuperação nem sempre são registradas, acompanhadas ou avaliadas de forma organizada.
```

Essa tag deve explicar o motivo da análise do processo.

---

## 11. [OBJETIVO_DO_PROCESSO]

A tag `[OBJETIVO_DO_PROCESSO]` define o que o processo deve alcançar.

Exemplo:

```txt id="555dxm"
[OBJETIVO_DO_PROCESSO]
    Organizar um fluxo de recuperação contínua que permita diagnosticar dificuldades, planejar intervenções, aplicar atividades e registrar evidências de aprendizagem.
```

---

## 12. [ESCOPO_DO_PROCESSO]

A tag `[ESCOPO_DO_PROCESSO]` define o que faz parte do processo.

Exemplo:

```txt id="8pzbqk"
[ESCOPO_DO_PROCESSO]
    diagnóstico das dificuldades
    planejamento da intervenção
    aplicação das atividades
    acompanhamento dos estudantes
    registro das evidências
    avaliação dos resultados
```

Quando necessário, pode incluir também o que fica fora do processo:

```txt id="h56ebz"
fora_do_escopo>
    atendimento clínico
    laudo diagnóstico
    decisões de promoção ou retenção
```

---

## 13. [ENTRADAS_DO_PROCESSO]

A tag `[ENTRADAS_DO_PROCESSO]` define os elementos necessários para iniciar o processo.

Exemplo:

```txt id="795rex"
[ENTRADAS_DO_PROCESSO]
    resultados de avaliações
    observações do professor
    atividades realizadas
    registros de participação
    dificuldades identificadas
```

As entradas podem ser dados, documentos, materiais, solicitações, pessoas, recursos ou informações.

---

## 14. [SAÍDAS_DO_PROCESSO]

A tag `[SAÍDAS_DO_PROCESSO]` define o que deve ser produzido ao final do processo.

Exemplo:

```txt id="y255xt"
[SAÍDAS_DO_PROCESSO]
    plano de intervenção
    atividade de recuperação
    relatório de acompanhamento
    evidências de aprendizagem
    encaminhamentos pedagógicos
```

As saídas devem ser observáveis ou registráveis.

---

## 15. [ETAPAS]

A tag `[ETAPAS]` define as partes do processo em ordem lógica.

Modelo:

```txt id="zluzwt"
[ETAPAS]

    etapa>
        id>
            E01

        nome>
            diagnóstico

        descrição>
            identificar dificuldades dos alunos

        responsável>
            professor

        entrada>
            avaliações e observações

        saída>
            lista de dificuldades identificadas
```

Exemplo compacto:

```txt id="cg6512"
[ETAPAS]
    E01 - diagnosticar dificuldades
    E02 - planejar intervenção
    E03 - aplicar atividade
    E04 - acompanhar resolução
    E05 - registrar evidências
    E06 - avaliar progresso
```

---

## 16. [FLUXO]

A tag `[FLUXO]` descreve a sequência do processo.

Exemplo:

```txt id="1hhg58"
[FLUXO]
    diagnóstico
    ↓
    planejamento da intervenção
    ↓
    aplicação da atividade
    ↓
    acompanhamento
    ↓
    registro
    ↓
    avaliação do progresso
```

Também pode ser usado em formato textual:

```txt id="308u8b"
[FLUXO]
    primeiro o professor identifica as dificuldades, depois planeja a intervenção, aplica atividades, acompanha os alunos e registra evidências.
```

---

## 17. [RESPONSÁVEIS]

A tag `[RESPONSÁVEIS]` define quem participa do processo.

Modelo:

```txt id="6o2bwp"
[RESPONSÁVEIS]

    responsável>
        papel>
            professor

        função>
            diagnosticar, aplicar intervenção e registrar evidências

    responsável>
        papel>
            coordenação

        função>
            acompanhar o processo e orientar ajustes
```

Responsáveis podem ser pessoas, equipes, setores ou papéis.

---

## 18. [RECURSOS]

A tag `[RECURSOS]` define materiais, ferramentas ou condições necessárias.

Exemplo:

```txt id="0axucm"
[RECURSOS]
    atividades impressas
    quadro
    caderno dos alunos
    planilha de acompanhamento
    resultados de avaliações
    tempo de aula
```

---

## 19. [REGRAS_OPERACIONAIS]

A tag `[REGRAS_OPERACIONAIS]` define normas, regras ou condições que o processo deve seguir.

Exemplo:

```txt id="i6mgn7"
[REGRAS_OPERACIONAIS]
    registrar apenas informações pedagógicas relevantes
    não expor alunos individualmente em relatórios coletivos
    aplicar intervenção vinculada à dificuldade diagnosticada
    acompanhar progresso por evidências observáveis
```

Essas regras orientam a execução do processo.

---

## 20. [PADRÃO_DE_EXECUÇÃO]

A tag `[PADRÃO_DE_EXECUÇÃO]` define como o processo deve ser executado para manter regularidade.

Modelo:

```txt id="a5qs0q"
[PADRÃO_DE_EXECUÇÃO]
    frequência>
        semanal

    forma_de_registro>
        planilha ou relatório curto

    critério_de_execução>
        cada intervenção deve estar relacionada a uma dificuldade identificada

    critério_de_qualidade>
        a saída deve permitir verificar se houve avanço
```

O padrão de execução evita que o processo dependa apenas da memória ou da prática informal.

---

## 21. [INDICADORES]

A tag `[INDICADORES]` define como medir o funcionamento do processo.

Modelo:

```txt id="uw8n2m"
[INDICADORES]

    indicador>
        nome>
            participação dos alunos

        forma_de_medida>
            observação durante a atividade

        resultado_esperado>
            aumento da participação nas discussões e resoluções

    indicador>
        nome>
            melhoria na resolução de problemas

        forma_de_medida>
            comparação entre atividade diagnóstica e atividade posterior

        resultado_esperado>
            maior número de alunos conseguindo interpretar o enunciado
```

Indicadores podem ser quantitativos ou qualitativos.

---

## 22. [GARGALOS]

A tag `[GARGALOS]` identifica pontos que atrasam, dificultam ou prejudicam o processo.

Modelo:

```txt id="1vs160"
[GARGALOS]

    gargalo>
        descrição>
            alunos não compreendem o enunciado da atividade

        impacto>
            a resolução não avança mesmo quando o conteúdo já foi explicado

        possível_causa>
            dificuldade de leitura e interpretação
```

Gargalos ajudam a direcionar melhorias.

---

## 23. [RISCOS]

A tag `[RISCOS]` registra situações que podem comprometer o processo.

Modelo:

```txt id="crcbkk"
[RISCOS]

    risco>
        descrição>
            falta de tempo para concluir a intervenção

        impacto>
            processo fica incompleto

        mitigação>
            dividir a intervenção em etapas menores
```

---

## 24. [MELHORIAS]

A tag `[MELHORIAS]` registra ações para melhorar o processo.

Modelo:

```txt id="k3s6y5"
[MELHORIAS]

    melhoria>
        problema_relacionado>
            dificuldade em interpretar problemas

        ação_proposta>
            incluir perguntas norteadoras antes da resolução

        impacto_esperado>
            alunos identificarem melhor dados e objetivos do problema
```

A melhoria deve estar ligada a um problema, gargalo ou indicador.

---

## 25. [VALIDAÇÃO]

A tag `[VALIDAÇÃO]` define como verificar se o processo funcionou.

Exemplo:

```txt id="c0k6cq"
[VALIDAÇÃO]
    comparar desempenho antes e depois da intervenção
    observar participação dos alunos
    analisar registros produzidos
    verificar se os objetivos foram alcançados
    revisar o processo com base nos resultados
```

---

## 26. [CICLO_DE_MELHORIA]

A tag `[CICLO_DE_MELHORIA]` organiza o processo como ciclo contínuo.

Modelo:

```txt id="uv674c"
[CICLO_DE_MELHORIA]
    planejar>
        definir objetivo e intervenção

    executar>
        aplicar a atividade ou ação

    verificar>
        observar resultados e evidências

    ajustar>
        corrigir o processo para nova aplicação
```

Essa estrutura pode ser usada em processos inspirados na lógica de melhoria contínua.

---

## 27. Níveis de uso da LMC-PROCESS

### Nível 1 — Descrição simples

Indicado para registrar um processo básico.

```txt id="o87nuh"
[PROCESSO]
[OBJETIVO_DO_PROCESSO]
[SAÍDA]
```

---

### Nível 2 — Processo estruturado

Indicado para organizar etapas, entradas e saídas.

```txt id="vlymwl"
[PROCESSO]
[ENTRADAS_DO_PROCESSO]
[ETAPAS]
[SAÍDAS_DO_PROCESSO]
[RESPONSÁVEIS]
[SAÍDA]
```

---

### Nível 3 — Processo analisado

Indicado para encontrar problemas e propor melhorias.

```txt id="39xkns"
[PROCESSO]
[PROBLEMA_DO_PROCESSO]
[ETAPAS]
[GARGALOS]
[RISCOS]
[MELHORIAS]
[SAÍDA]
```

---

### Nível 4 — Processo padronizado

Indicado para criar padrão de execução.

```txt id="nv9gef"
[PROCESSO]
[REGRAS_OPERACIONAIS]
[PADRÃO_DE_EXECUÇÃO]
[INDICADORES]
[VALIDAÇÃO]
[SAÍDA]
```

---

### Nível 5 — Melhoria contínua

Indicado para processos cíclicos.

```txt id="ra20c9"
[PROCESSO]
[CICLO_DE_MELHORIA]
[INDICADORES]
[GARGALOS]
[MELHORIAS]
[VALIDAÇÃO]
```

---

## 28. Modelo mínimo

```txt id="77nn7j"
[PROCESSO]
    nome do processo

[OBJETIVO_DO_PROCESSO]
    objetivo do processo

[SAÍDA]
    produto esperado
```

---

## 29. Modelo padrão

```txt id="ikq13y"
[PROTOCOLO_DE_USO]
    tipo>
        análise

    ação>
        organizar e analisar processo

    escopo>
        não criar sistema nem documento final sem solicitação

[PROJETO]
    nome_do_projeto

[PROCESSO]
    nome do processo

[TIPO_DE_PROCESSO]
    tipo do processo

[PROBLEMA_DO_PROCESSO]
    problema ou necessidade identificada

[OBJETIVO_DO_PROCESSO]
    o que o processo deve alcançar

[CONTEXTO]
    situação em que o processo ocorre

[ESCOPO_DO_PROCESSO]
    o que faz parte do processo

[ENTRADAS_DO_PROCESSO]
    elementos necessários para iniciar o processo

[SAÍDAS_DO_PROCESSO]
    resultados esperados

[ETAPAS]
    sequência de etapas

[FLUXO]
    representação da sequência do processo

[RESPONSÁVEIS]
    papéis envolvidos

[RECURSOS]
    recursos necessários

[REGRAS_OPERACIONAIS]
    regras que devem orientar a execução

[PADRÃO_DE_EXECUÇÃO]
    frequência, registro e critérios de qualidade

[INDICADORES]
    formas de medir o funcionamento do processo

[GARGALOS]
    problemas ou pontos de atraso

[RISCOS]
    riscos e formas de mitigação

[MELHORIAS]
    melhorias propostas

[VALIDAÇÃO]
    como verificar se o processo funcionou

[CICLO_DE_MELHORIA]
    planejar, executar, verificar e ajustar

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
    não inventar dados
    não criar responsáveis não informados como definitivos
    não propor melhoria sem relação com problema ou gargalo
    não gerar código nesta etapa

[FORMATO]
    organizar em seções claras
    separar fluxo, etapas, gargalos, riscos e melhorias

[CRITÉRIOS_DE_ACEITAÇÃO]
    processo deve estar descrito em etapas
    entradas e saídas devem estar claras
    gargalos devem estar identificados
    melhorias devem estar relacionadas aos problemas
    validação deve ser verificável

[SAÍDA]
    gerar análise estruturada do processo
```

---

## 30. Exemplo — processo de recuperação contínua em matemática

```txt id="09g3n0"
[PROTOCOLO_DE_USO]
    tipo>
        análise

    ação>
        organizar processo pedagógico

    escopo>
        não gerar relatório final nesta etapa

[PROJETO]
    recuperacao_continua_matematica

[PROCESSO]
    recuperação contínua em matemática

[TIPO_DE_PROCESSO]
    educacional | pedagógico

[PROBLEMA_DO_PROCESSO]
    Os alunos apresentam dificuldades recorrentes em conteúdos matemáticos, mas o acompanhamento das intervenções e evidências de aprendizagem precisa ser mais organizado.

[OBJETIVO_DO_PROCESSO]
    Organizar um processo de recuperação contínua que permita identificar dificuldades, planejar intervenções, aplicar atividades, acompanhar os alunos e registrar evidências de progresso.

[CONTEXTO]
    O processo ocorre durante o bimestre, com turmas que apresentam dificuldades em interpretação de problemas, operações básicas e organização do raciocínio matemático.

[ESCOPO_DO_PROCESSO]
    diagnóstico das dificuldades
    planejamento das intervenções
    aplicação de atividades
    acompanhamento durante a resolução
    registro de evidências
    avaliação do progresso

[ENTRADAS_DO_PROCESSO]
    resultados de avaliações
    observações em sala de aula
    atividades diagnósticas
    participação dos alunos
    registros de dificuldades

[SAÍDAS_DO_PROCESSO]
    plano de intervenção
    atividades de recuperação
    registros de acompanhamento
    evidências de aprendizagem
    ajustes no planejamento

[ETAPAS]

    etapa>
        id>
            E01

        nome>
            diagnóstico

        descrição>
            identificar as principais dificuldades dos alunos

        responsável>
            professor

        entrada>
            avaliações e observações

        saída>
            lista de dificuldades prioritárias

    etapa>
        id>
            E02

        nome>
            planejamento da intervenção

        descrição>
            definir estratégias e atividades relacionadas às dificuldades identificadas

        responsável>
            professor

        entrada>
            lista de dificuldades

        saída>
            plano de intervenção

    etapa>
        id>
            E03

        nome>
            aplicação da atividade

        descrição>
            aplicar atividade com questões progressivas e perguntas norteadoras

        responsável>
            professor

        entrada>
            plano de intervenção

        saída>
            atividade realizada

    etapa>
        id>
            E04

        nome>
            acompanhamento

        descrição>
            observar como os alunos resolvem as atividades e onde apresentam novas dificuldades

        responsável>
            professor

        entrada>
            atividade realizada

        saída>
            observações pedagógicas

    etapa>
        id>
            E05

        nome>
            registro de evidências

        descrição>
            registrar avanços, dificuldades persistentes e necessidade de novas intervenções

        responsável>
            professor

        entrada>
            observações pedagógicas

        saída>
            evidências de aprendizagem

    etapa>
        id>
            E06

        nome>
            ajuste do planejamento

        descrição>
            redefinir ações com base nos resultados observados

        responsável>
            professor

        entrada>
            evidências de aprendizagem

        saída>
            novo ciclo de intervenção

[FLUXO]
    diagnóstico
    ↓
    planejamento da intervenção
    ↓
    aplicação da atividade
    ↓
    acompanhamento
    ↓
    registro de evidências
    ↓
    ajuste do planejamento

[RESPONSÁVEIS]

    responsável>
        papel>
            professor

        função>
            diagnosticar, planejar, aplicar, acompanhar e registrar o processo

    responsável>
        papel>
            coordenação pedagógica

        função>
            acompanhar registros e apoiar ajustes quando necessário

[RECURSOS]
    avaliações anteriores
    atividades diagnósticas
    listas de exercícios progressivos
    perguntas norteadoras
    quadro
    caderno dos alunos
    planilha de acompanhamento

[REGRAS_OPERACIONAIS]
    toda intervenção deve estar vinculada a uma dificuldade observada
    os registros devem ser pedagógicos e objetivos
    não expor alunos individualmente em documentos coletivos
    as atividades devem respeitar o nível da turma
    os ajustes devem considerar evidências observadas

[PADRÃO_DE_EXECUÇÃO]
    frequência>
        semanal ou conforme necessidade da turma

    forma_de_registro>
        registro curto por intervenção realizada

    critério_de_execução>
        cada intervenção deve ter objetivo, atividade e evidência esperada

    critério_de_qualidade>
        o processo deve permitir identificar se houve avanço ou persistência da dificuldade

[INDICADORES]

    indicador>
        nome>
            participação dos alunos

        forma_de_medida>
            observação durante atividades e discussões

        resultado_esperado>
            aumento da participação e tentativa de resolução

    indicador>
        nome>
            interpretação de problemas

        forma_de_medida>
            comparação entre respostas antes e depois da intervenção

        resultado_esperado>
            maior capacidade de identificar dados relevantes e objetivo da questão

    indicador>
        nome>
            resolução matemática

        forma_de_medida>
            análise das atividades realizadas

        resultado_esperado>
            maior número de alunos concluindo procedimentos corretamente

[GARGALOS]

    gargalo>
        descrição>
            parte dos alunos não compreende o enunciado

        impacto>
            dificuldade para iniciar a resolução

        possível_causa>
            leitura superficial e dificuldade de interpretação

    gargalo>
        descrição>
            alguns alunos apresentam defasagem em operações básicas

        impacto>
            mesmo compreendendo a ideia, não conseguem concluir o cálculo

        possível_causa>
            lacunas de aprendizagem anteriores

[RISCOS]

    risco>
        descrição>
            falta de tempo para aplicar intervenções completas

        impacto>
            processo pode ficar fragmentado

        mitigação>
            dividir intervenções em etapas menores

    risco>
        descrição>
            registros ficarem genéricos

        impacto>
            dificuldade para comprovar progresso

        mitigação>
            registrar evidências objetivas e observáveis

[MELHORIAS]

    melhoria>
        problema_relacionado>
            dificuldade em interpretar problemas

        ação_proposta>
            iniciar atividades com perguntas norteadoras antes dos cálculos

        impacto_esperado>
            alunos identificarem melhor dados, objetivos e relações matemáticas

    melhoria>
        problema_relacionado>
            defasagem em operações básicas

        ação_proposta>
            inserir retomadas curtas antes das atividades principais

        impacto_esperado>
            reduzir bloqueios durante a resolução

[VALIDAÇÃO]
    verificar se os alunos conseguem identificar o que o problema pede
    verificar se conseguem separar dados relevantes
    comparar desempenho entre atividade diagnóstica e atividade posterior
    observar participação nas discussões
    registrar avanços e dificuldades persistentes

[CICLO_DE_MELHORIA]
    planejar>
        definir dificuldade prioritária e intervenção

    executar>
        aplicar atividade guiada

    verificar>
        observar desempenho e registrar evidências

    ajustar>
        modificar estratégia para o próximo ciclo

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
    não citar nomes
    não gerar relatório final nesta etapa
    não propor intervenção desconectada das dificuldades
    não usar linguagem acusatória

[FORMATO]
    organizar em processo, etapas, fluxo, responsáveis, gargalos, riscos, melhorias e validação

[CRITÉRIOS_DE_ACEITAÇÃO]
    o processo deve conter etapas claras
    entradas e saídas devem estar identificadas
    gargalos devem estar relacionados ao contexto
    melhorias devem estar ligadas aos gargalos
    indicadores devem ser verificáveis
    validação deve permitir análise do progresso

[SAÍDA]
    gerar análise estruturada do processo de recuperação contínua em matemática
```

---

## 31. Exemplo — processo operacional de execução de serviço

```txt id="7sekgk"
[PROTOCOLO_DE_USO]
    tipo>
        análise

    ação>
        organizar processo operacional

    escopo>
        não gerar orçamento nesta etapa

[PROJETO]
    processo_servico_pintura

[PROCESSO]
    execução de serviço de pintura residencial

[TIPO_DE_PROCESSO]
    operacional | produtivo

[PROBLEMA_DO_PROCESSO]
    A execução do serviço pode sofrer atrasos, retrabalho e falta de controle quando as etapas, responsáveis, materiais e critérios de qualidade não estão claramente definidos.

[OBJETIVO_DO_PROCESSO]
    Organizar o processo de pintura residencial em etapas claras, com entradas, saídas, responsáveis, recursos, riscos e critérios de validação.

[ENTRADAS_DO_PROCESSO]
    local do serviço
    medidas da área
    tipo de superfície
    materiais necessários
    equipe disponível
    prazo combinado
    padrão de acabamento esperado

[SAÍDAS_DO_PROCESSO]
    superfície preparada
    pintura aplicada
    acabamento revisado
    ambiente limpo
    serviço entregue ao cliente

[ETAPAS]
    E01 - vistoria do local
    E02 - medição da área
    E03 - preparação da superfície
    E04 - aplicação de selador ou fundo
    E05 - correção com massa, se necessário
    E06 - lixamento
    E07 - aplicação da tinta
    E08 - revisão do acabamento
    E09 - limpeza final
    E10 - entrega do serviço

[RESPONSÁVEIS]
    pintor responsável
    ajudante
    cliente para validação final

[RECURSOS]
    tinta
    massa
    selador
    lixas
    rolos
    pincéis
    bandejas
    lona de proteção
    escadas
    equipamentos de segurança

[REGRAS_OPERACIONAIS]
    proteger piso e móveis antes de iniciar
    corrigir imperfeições antes da pintura final
    respeitar tempo de secagem
    revisar acabamento antes da entrega
    registrar mudanças solicitadas pelo cliente

[INDICADORES]
    prazo de execução
    consumo de material
    retrabalho identificado
    qualidade do acabamento
    satisfação do cliente

[GARGALOS]
    atraso na compra de materiais
    superfície mal preparada
    tempo de secagem não respeitado
    mudança de escopo durante a execução

[RISCOS]
    falta de material
    chuva em pintura externa
    cliente solicitar alteração fora do combinado
    retrabalho por falha de preparação

[MELHORIAS]
    criar checklist antes de iniciar
    registrar medidas e materiais por ambiente
    validar preparação antes da pintura final
    criar checklist de entrega

[VALIDAÇÃO]
    verificar cobertura da pintura
    verificar acabamento
    conferir limpeza final
    validar entrega com cliente

[SAÍDA]
    gerar processo operacional estruturado para execução de serviço de pintura residencial
```

---

## 32. Regras de interpretação específicas da LMC-PROCESS

Ao receber uma instrução LMC-PROCESS, a IA deve:

1. Identificar o processo antes de sugerir melhoria.
2. Diferenciar processo, problema, objetivo e solução.
3. Identificar entradas e saídas do processo.
4. Organizar etapas em sequência lógica.
5. Diferenciar etapa, responsável, recurso e regra operacional.
6. Não propor melhoria sem relação com problema, gargalo ou risco.
7. Não inventar dados críticos não fornecidos.
8. Não transformar processo em sistema ou código sem solicitação.
9. Registrar gargalos quando houver dificuldade, atraso ou retrabalho.
10. Registrar riscos quando houver possibilidade de falha.
11. Sugerir indicadores verificáveis.
12. Relacionar melhorias aos problemas identificados.
13. Manter linguagem clara e operacional.
14. Adaptar o nível técnico ao público-alvo.
15. Preservar a validação humana antes da adoção do processo.

---

## 33. Critérios de qualidade de processo

Uma saída gerada com LMC-PROCESS deve ser avaliada pelos seguintes critérios:

```txt id="f8wqvu"
clareza do processo
clareza do objetivo do processo
entradas identificadas
saídas identificadas
etapas organizadas
responsáveis definidos
recursos identificados
regras operacionais claras
gargalos identificados
riscos registrados
melhorias relacionadas aos problemas
indicadores verificáveis
validação definida
utilidade prática para execução
```

---

## 34. Relação com outros módulos

A LMC-PROCESS pode ser combinada com outros módulos da LMC.

Exemplos:

```txt id="mnzsx9"
LMC-PROCESS + LMC-REQ
    transformar processos em requisitos de sistema

LMC-PROCESS + LMC-AGILE
    organizar melhorias de processo em backlog, tarefas e sprints

LMC-PROCESS + LMC-DOC
    gerar procedimentos, manuais, relatórios e documentos institucionais

LMC-PROCESS + LMC-EDU
    organizar recuperação contínua, avaliações, intervenções e rotinas pedagógicas

LMC-PROCESS + LMC-CODE
    automatizar etapas de processos por meio de sistemas ou scripts

LMC-PROCESS + LMC-TEST
    avaliar se uma saída respeitou o processo definido
```

---

## 35. Limites da LMC-PROCESS

A LMC-PROCESS não garante que o processo será executado corretamente.

Ela organiza a análise, mas não substitui:

```txt id="lul6ug"
observação da realidade
experiência dos profissionais
validação em campo
ajustes operacionais
treinamento da equipe
gestão humana
tomada de decisão
```

Processos reais podem mudar conforme ambiente, recursos, equipe, prazos e imprevistos.

Por isso, a LMC-PROCESS deve ser usada como ferramenta de estruturação, análise e melhoria, não como substituta da gestão real.

---

## 36. Definição acadêmica da LMC-PROCESS

A LMC-PROCESS pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à estruturação de processos mediados por Inteligência Artificial, organizando problema, objetivo, escopo, entradas, saídas, etapas, fluxo, responsáveis, recursos, regras operacionais, indicadores, gargalos, riscos, melhorias e validação, com o objetivo de reduzir ambiguidades, padronizar a comunicação sobre processos e apoiar a análise, execução e melhoria contínua em diferentes contextos organizacionais.

---

## 37. Síntese

A LMC-PROCESS organiza processos em blocos claros.

Sua função é ajudar o usuário a comunicar para a IA:

```txt id="n1cezu"
qual processo será analisado
qual problema existe
qual objetivo precisa ser alcançado
quais entradas são necessárias
quais etapas compõem o processo
quem participa
quais recursos são usados
quais regras precisam ser seguidas
quais saídas são esperadas
quais gargalos existem
quais riscos podem ocorrer
quais melhorias fazem sentido
como validar se o processo funcionou
```

A LMC-PROCESS não substitui o conhecimento prático humano. Ela organiza esse conhecimento para que a IA auxilie na análise, padronização e melhoria de processos com mais clareza e controle.

---

**Fim da especificação LMC-PROCESS**
