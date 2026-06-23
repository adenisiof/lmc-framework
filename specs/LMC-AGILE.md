# LMC-AGILE — Especificação para Organização de Processos Ágeis com Inteligência Artificial

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo de processos ágeis
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-AGILE.md`

---

## 1. Definição

A **LMC-AGILE** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à organização de projetos, tarefas, entregas, sprints, backlog, histórias de usuário e processos ágeis com apoio de Inteligência Artificial.

Sua função é transformar ideias, requisitos, problemas ou objetivos de projeto em uma estrutura de trabalho organizada, priorizada, verificável e executável.

A LMC-AGILE pode ser usada em projetos de software, educação, processos administrativos, documentação, automação, pesquisa, produção de conteúdo e organização de tarefas.

Fluxo conceitual:

```txt
Ideia ou requisito
↓
LMC-REQ
↓
Requisitos organizados
↓
LMC-AGILE
↓
Backlog, histórias, tarefas e sprint
↓
Execução humana ou assistida por IA
↓
Validação da entrega
```

A LMC-AGILE não substitui metodologias ágeis como Scrum, Kanban ou XP. Ela organiza a comunicação com a IA para que esses conceitos sejam usados de forma mais clara, simples e adaptável ao contexto do usuário.

---

## 2. Finalidade da LMC-AGILE

A LMC-AGILE tem como finalidade estruturar o planejamento e a execução de projetos por meio de blocos claros.

Ela pode ser usada para organizar:

```txt
visão do produto
MVP
backlog
épicos
histórias de usuário
critérios de aceitação
tarefas
sprints
prioridades
dependências
riscos
definition of ready
definition of done
entregas
retrospectivas
melhorias
acompanhamento de progresso
```

A LMC-AGILE ajuda o usuário a transformar uma intenção ampla em ações menores, compreensíveis e executáveis.

---

## 3. Problema que a LMC-AGILE busca resolver

Muitos projetos começam com objetivos amplos, mas sem divisão clara de trabalho.

Exemplos:

```txt
quero criar um sistema de provas
quero organizar meu projeto no GitHub
quero criar uma linguagem LMC
quero fazer um site
quero melhorar um processo de trabalho
```

Essas frases mostram uma intenção, mas ainda não definem:

```txt
quais entregas são prioritárias
quais tarefas vêm primeiro
quais requisitos pertencem ao MVP
quais histórias de usuário precisam ser criadas
quais critérios indicam que a tarefa ficou pronta
quais dependências existem
quais riscos podem impedir a entrega
como validar se a sprint foi concluída
```

A LMC-AGILE busca reduzir esse problema estruturando o trabalho em unidades menores, organizadas e verificáveis.

---

## 4. Relação com a LMC-CORE

A LMC-AGILE herda as regras gerais da **LMC-CORE**, especialmente:

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

A LMC-AGILE acrescenta tags específicas para processos ágeis:

```txt
[METODO_AGIL]
[PRODUTO]
[VISÃO_DO_PRODUTO]
[MVP]
[BACKLOG]
[ÉPICO]
[HISTÓRIA_DE_USUÁRIO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[DEFINITION_OF_READY]
[DEFINITION_OF_DONE]
[SPRINT]
[TAREFAS]
[PRIORIZAÇÃO]
[DEPENDÊNCIAS]
[RISCOS]
[ENTREGA]
[REVIEW]
[RETROSPECTIVA]
[MELHORIAS]
```

---

## 5. Princípios da LMC-AGILE

### P1. Entrega antes da complexidade

O projeto deve ser organizado para gerar entregas úteis, mesmo que pequenas.

### P2. Trabalho em partes menores

Ideias grandes devem ser quebradas em épicos, histórias, tarefas e entregas.

### P3. Critério antes da conclusão

Uma tarefa só deve ser considerada concluída quando houver critério claro de aceite.

### P4. Priorização explícita

A IA deve diferenciar o que é obrigatório, desejável e futuro.

### P5. Backlog como estrutura viva

O backlog pode ser atualizado, reorganizado e refinado conforme o projeto evolui.

### P6. MVP antes da versão completa

A primeira entrega deve priorizar o mínimo necessário para validar a ideia.

### P7. Dependências visíveis

A IA deve apontar quando uma tarefa depende de outra.

### P8. Riscos identificados

Problemas possíveis devem ser registrados antes da execução.

### P9. Adaptação ao contexto

A LMC-AGILE pode usar Scrum, Kanban ou uma adaptação simples, conforme a necessidade do projeto.

### P10. Validação humana

A IA pode organizar, sugerir e dividir tarefas, mas a decisão final sobre prioridade e execução pertence ao usuário.

---

## 6. Estrutura mínima da LMC-AGILE

A estrutura mínima é:

```txt
[PROJETO]
    nome do projeto

[OBJETIVO]
    objetivo do trabalho

[SAÍDA]
    produto esperado
```

Exemplo:

```txt
[PROJETO]
    LMC-FRAMEWORK

[OBJETIVO]
    Organizar os próximos módulos da LMC em um backlog de desenvolvimento.

[SAÍDA]
    gerar backlog inicial com épicos, tarefas e prioridades.
```

---

## 7. Estrutura recomendada da LMC-AGILE

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[METODO_AGIL]
[PRODUTO]
[VISÃO_DO_PRODUTO]
[MVP]
[OBJETIVO]
[CONTEXTO]
[BACKLOG]
[ÉPICO]
[HISTÓRIA_DE_USUÁRIO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[DEFINITION_OF_READY]
[DEFINITION_OF_DONE]
[SPRINT]
[TAREFAS]
[PRIORIZAÇÃO]
[DEPENDÊNCIAS]
[RISCOS]
[ENTREGA]
[REVIEW]
[RETROSPECTIVA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Nem todas as tags precisam ser usadas ao mesmo tempo. Para projetos simples, a estrutura pode ser reduzida.

---

## 8. [METODO_AGIL]

A tag `[METODO_AGIL]` define o método ou abordagem usada para organizar o trabalho.

Exemplos:

```txt
Scrum
Kanban
Scrum simplificado
Kanban pessoal
Sprint semanal
Sprint quinzenal
Backlog priorizado
Método adaptado
```

Exemplo:

```txt
[METODO_AGIL]
    Scrum simplificado
```

---

## 9. [PRODUTO]

A tag `[PRODUTO]` define o produto, sistema, documento, processo ou entrega principal.

Exemplo:

```txt
[PRODUTO]
    LMC-FRAMEWORK
```

Outro exemplo:

```txt
[PRODUTO]
    sistema web de provas escolares
```

---

## 10. [VISÃO_DO_PRODUTO]

A tag `[VISÃO_DO_PRODUTO]` define a ideia geral do produto e o valor que ele deve entregar.

Modelo:

```txt
[VISÃO_DO_PRODUTO]
    produto>
        nome do produto

    público>
        público principal

    necessidade>
        problema que o produto resolve

    valor>
        benefício esperado
```

Exemplo:

```txt
[VISÃO_DO_PRODUTO]
    produto>
        LMC-FRAMEWORK

    público>
        usuários que utilizam IA para organizar documentos, código, requisitos e processos

    necessidade>
        reduzir ambiguidades na comunicação humano-IA

    valor>
        permitir instruções mais claras, reutilizáveis e verificáveis
```

---

## 11. [MVP]

A tag `[MVP]` define a primeira versão mínima útil do projeto.

Modelo:

```txt
[MVP]
    objetivo>
        entregar a menor versão funcional do projeto

    inclui>
        item 1
        item 2
        item 3

    não_inclui>
        item futuro 1
        item futuro 2
```

Exemplo:

```txt
[MVP]
    objetivo>
        publicar uma versão inicial do LMC-FRAMEWORK no GitHub

    inclui>
        README
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE

    não_inclui>
        site completo
        interpretador automático
        schemas JSON
        artigo científico final
```

---

## 12. [BACKLOG]

A tag `[BACKLOG]` organiza os itens de trabalho do projeto.

Modelo:

```txt
[BACKLOG]

    item>
        id>
            B01

        nome>
            criar LMC-CORE

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído
```

Exemplo compacto:

```txt
[BACKLOG]
    B01 - criar LMC-CORE - alta - concluído
    B02 - criar LMC-DOC - alta - concluído
    B03 - criar LMC-CODE - alta - concluído
    B04 - criar LMC-AGILE - alta - em andamento
```

---

## 13. [ÉPICO]

A tag `[ÉPICO]` define uma grande entrega ou conjunto de funcionalidades.

Modelo:

```txt
[ÉPICO]
    id>
        EP01

    nome>
        estruturar módulos principais da LMC

    objetivo>
        criar as especificações centrais do framework

    inclui>
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE
```

Épicos agrupam histórias e tarefas relacionadas.

---

## 14. [HISTÓRIA_DE_USUÁRIO]

A tag `[HISTÓRIA_DE_USUÁRIO]` descreve uma necessidade do ponto de vista do usuário.

Modelo:

```txt
[HISTÓRIA_DE_USUÁRIO]
    id>
        US01

    como>
        tipo de usuário

    quero>
        necessidade ou ação

    para>
        benefício esperado

    prioridade>
        alta | média | baixa

    status>
        pendente | em andamento | concluída
```

Exemplo:

```txt
[HISTÓRIA_DE_USUÁRIO]
    id>
        US01

    como>
        usuário que utiliza IA

    quero>
        estruturar minhas solicitações em blocos claros

    para>
        obter respostas mais aderentes ao que pedi

    prioridade>
        alta

    status>
        em andamento
```

Forma compacta permitida:

```txt
Como usuário que utiliza IA, quero estruturar minhas solicitações em blocos claros para obter respostas mais aderentes ao que pedi.
```

---

## 15. [CRITÉRIOS_DE_ACEITAÇÃO]

A tag `[CRITÉRIOS_DE_ACEITAÇÃO]` define as condições para aceitar uma história, tarefa ou entrega.

Modelo:

```txt
[CRITÉRIOS_DE_ACEITAÇÃO]
    critério>
        a especificação deve conter definição, finalidade, tags, modelos, exemplos e regras de interpretação

    critério>
        o texto deve estar em Markdown

    critério>
        o módulo deve seguir a estrutura herdada da LMC-CORE
```

Critérios de aceitação devem ser verificáveis.

---

## 16. [DEFINITION_OF_READY]

A tag `[DEFINITION_OF_READY]` define quando uma tarefa ou história está pronta para começar.

Exemplo:

```txt
[DEFINITION_OF_READY]
    objetivo definido
    contexto informado
    escopo delimitado
    critérios de aceitação definidos
    dependências identificadas
```

Essa tag evita iniciar uma tarefa antes de ela estar clara.

---

## 17. [DEFINITION_OF_DONE]

A tag `[DEFINITION_OF_DONE]` define quando uma tarefa pode ser considerada concluída.

Exemplo:

```txt
[DEFINITION_OF_DONE]
    conteúdo criado
    estrutura revisada
    critérios de aceitação atendidos
    arquivo salvo no local correto
    pronto para commit no GitHub
```

Essa tag evita considerar concluído algo que ainda não foi revisado ou validado.

---

## 18. [SPRINT]

A tag `[SPRINT]` define um ciclo de trabalho.

Modelo:

```txt
[SPRINT]
    nome>
        Sprint 01

    duração>
        7 dias

    objetivo>
        finalizar os módulos principais da LMC

    itens>
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE
```

Exemplo:

```txt
[SPRINT]
    nome>
        Sprint inicial do framework

    duração>
        sem prazo fixo

    objetivo>
        criar as especificações mínimas dos módulos principais

    entrega>
        arquivos Markdown na pasta specs
```

---

## 19. [TAREFAS]

A tag `[TAREFAS]` divide histórias ou entregas em ações menores.

Modelo:

```txt
[TAREFAS]

    tarefa>
        id>
            T01

        nome>
            criar arquivo LMC-AGILE.md

        descrição>
            escrever a especificação inicial do módulo ágil

        responsável>
            usuário + IA

        status>
            em andamento

        prioridade>
            alta
```

Exemplo compacto:

```txt
[TAREFAS]
    T01 - criar estrutura do módulo - alta - concluído
    T02 - escrever tags principais - alta - em andamento
    T03 - revisar exemplos - média - pendente
```

---

## 20. [PRIORIZAÇÃO]

A tag `[PRIORIZAÇÃO]` define a ordem de importância dos itens.

Modelo:

```txt
[PRIORIZAÇÃO]
    obrigatórios>
        itens que precisam entrar agora

    desejáveis>
        itens importantes, mas não essenciais

    futuros>
        itens para versões posteriores
```

Exemplo:

```txt
[PRIORIZAÇÃO]
    obrigatórios>
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE

    desejáveis>
        exemplos práticos
        matriz de testes

    futuros>
        site completo
        artigo científico
        interpretador automático
```

---

## 21. [DEPENDÊNCIAS]

A tag `[DEPENDÊNCIAS]` define o que precisa existir antes de uma tarefa ou entrega.

Exemplo:

```txt
[DEPENDÊNCIAS]
    LMC-AGILE depende da LMC-CORE
    LMC-CODE pode usar requisitos vindos da LMC-REQ
    exemplos práticos dependem das especificações dos módulos
```

---

## 22. [RISCOS]

A tag `[RISCOS]` registra possíveis problemas durante o desenvolvimento.

Modelo:

```txt
[RISCOS]

    risco>
        descrição>
            criar especificações grandes demais

        impacto>
            dificultar o uso por iniciantes

        mitigação>
            manter modelos mínimos e exemplos simples
```

Outros exemplos:

```txt
[RISCOS]
    excesso de complexidade
    escopo crescer demais
    falta de exemplos práticos
    módulos ficarem repetitivos
    dificuldade de manutenção
```

---

## 23. [ENTREGA]

A tag `[ENTREGA]` define o que será produzido ao final de uma sprint, tarefa ou história.

Exemplo:

```txt
[ENTREGA]
    arquivo specs/LMC-AGILE.md criado
    estrutura revisada
    pronto para commit no GitHub
```

---

## 24. [REVIEW]

A tag `[REVIEW]` registra a avaliação da entrega.

Modelo:

```txt
[REVIEW]
    o_que_foi_entregue>
        especificação inicial do LMC-AGILE

    pontos_corretos>
        estrutura criada
        tags principais definidas
        exemplos incluídos

    ajustes_necessários>
        revisar depois a integração com LMC-REQ e LMC-PROCESS
```

---

## 25. [RETROSPECTIVA]

A tag `[RETROSPECTIVA]` registra aprendizados do ciclo de trabalho.

Modelo:

```txt
[RETROSPECTIVA]
    funcionou_bem>
        criação progressiva dos módulos

    precisa_melhorar>
        reduzir repetições entre especificações

    próxima_ação>
        criar LMC-PROCESS
```

A retrospectiva ajuda a evoluir o próprio framework.

---

## 26. [MELHORIAS]

A tag `[MELHORIAS]` registra melhorias futuras.

Exemplo:

```txt
[MELHORIAS]
    criar modelo visual de backlog
    criar exemplos com sistema real
    criar integração entre LMC-REQ e LMC-AGILE
    criar quadro Kanban em Markdown
```

---

## 27. Níveis de uso da LMC-AGILE

### Nível 1 — Organização simples

Indicado para organizar tarefas básicas.

```txt
[PROJETO]
[OBJETIVO]
[TAREFAS]
[SAÍDA]
```

---

### Nível 2 — Backlog inicial

Indicado para transformar uma ideia em lista de trabalho.

```txt
[PROJETO]
[VISÃO_DO_PRODUTO]
[MVP]
[BACKLOG]
[PRIORIZAÇÃO]
[SAÍDA]
```

---

### Nível 3 — Histórias de usuário

Indicado para organizar funcionalidades ou necessidades.

```txt
[ÉPICO]
[HISTÓRIA_DE_USUÁRIO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[DEFINITION_OF_DONE]
[SAÍDA]
```

---

### Nível 4 — Sprint planejada

Indicado para organizar um ciclo de trabalho.

```txt
[SPRINT]
[OBJETIVO]
[BACKLOG]
[TAREFAS]
[DEPENDÊNCIAS]
[RISCOS]
[ENTREGA]
[SAÍDA]
```

---

### Nível 5 — Ciclo completo

Indicado para planejamento, execução e avaliação.

```txt
[VISÃO_DO_PRODUTO]
[MVP]
[BACKLOG]
[SPRINT]
[TAREFAS]
[REVIEW]
[RETROSPECTIVA]
[MELHORIAS]
```

---

## 28. Modelo mínimo

```txt
[PROJETO]
    nome do projeto

[OBJETIVO]
    objetivo do planejamento ágil

[TAREFAS]
    tarefas principais

[SAÍDA]
    produto esperado
```

---

## 29. Modelo padrão

```txt
[PROTOCOLO_DE_USO]
    tipo>
        planejamento

    ação>
        organizar projeto em estrutura ágil

    escopo>
        não gerar código nesta etapa

[PROJETO]
    nome_do_projeto

[METODO_AGIL]
    Scrum simplificado

[PRODUTO]
    nome do produto

[VISÃO_DO_PRODUTO]
    produto>
        nome do produto

    público>
        público principal

    necessidade>
        problema que será resolvido

    valor>
        benefício esperado

[MVP]
    objetivo>
        primeira versão útil

    inclui>
        item 1
        item 2

    não_inclui>
        item futuro 1
        item futuro 2

[BACKLOG]

    item>
        id>
            B01

        nome>
            nome do item

        tipo>
            épico | história | tarefa | melhoria

        prioridade>
            alta | média | baixa

        status>
            pendente | em andamento | concluído

[ÉPICO]
    id>
        EP01

    nome>
        nome do épico

    objetivo>
        objetivo do épico

[HISTÓRIA_DE_USUÁRIO]
    id>
        US01

    como>
        tipo de usuário

    quero>
        necessidade

    para>
        benefício

    prioridade>
        alta

[CRITÉRIOS_DE_ACEITAÇÃO]
    critério 1
    critério 2
    critério 3

[DEFINITION_OF_READY]
    objetivo definido
    contexto informado
    critérios definidos

[DEFINITION_OF_DONE]
    entrega criada
    critérios atendidos
    revisão concluída

[SPRINT]
    nome>
        nome da sprint

    duração>
        duração prevista

    objetivo>
        objetivo da sprint

[TAREFAS]
    tarefas da sprint

[DEPENDÊNCIAS]
    dependências identificadas

[RISCOS]
    riscos identificados

[ENTREGA]
    entrega esperada

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
    não gerar código
    não criar funcionalidades fora do escopo
    não tratar itens futuros como obrigatórios

[FORMATO]
    organizar em backlog, épicos, histórias, tarefas e sprint

[SAÍDA]
    gerar planejamento ágil do projeto
```

---

## 30. Exemplo — LMC-FRAMEWORK

```txt
[PROTOCOLO_DE_USO]
    tipo>
        planejamento

    ação>
        organizar projeto em estrutura ágil

    escopo>
        não gerar código nesta etapa

[PROJETO]
    LMC-FRAMEWORK

[METODO_AGIL]
    Scrum simplificado

[PRODUTO]
    Linguagem de Marcação Conceitual

[VISÃO_DO_PRODUTO]
    produto>
        LMC-FRAMEWORK

    público>
        usuários que desejam se comunicar melhor com IAs

    necessidade>
        reduzir ambiguidades nas instruções dadas à IA

    valor>
        permitir que humanos organizem melhor objetivos, contexto, restrições e saídas esperadas

[MVP]
    objetivo>
        publicar uma primeira versão funcional do framework no GitHub

    inclui>
        README
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE
        estrutura de pastas

    não_inclui>
        interpretador automático
        schemas JSON
        artigo científico completo
        site final

[BACKLOG]

    item>
        id>
            B01

        nome>
            criar LMC-CORE

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído

    item>
        id>
            B02

        nome>
            criar LMC-DOC

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído

    item>
        id>
            B03

        nome>
            criar LMC-CODE

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído

    item>
        id>
            B04

        nome>
            criar LMC-EDU

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído

    item>
        id>
            B05

        nome>
            criar LMC-REQ

        tipo>
            especificação

        prioridade>
            alta

        status>
            concluído

    item>
        id>
            B06

        nome>
            criar LMC-AGILE

        tipo>
            especificação

        prioridade>
            alta

        status>
            em andamento

    item>
        id>
            B07

        nome>
            criar LMC-PROCESS

        tipo>
            especificação

        prioridade>
            média

        status>
            pendente

    item>
        id>
            B08

        nome>
            criar LMC-TEST

        tipo>
            especificação

        prioridade>
            alta

        status>
            pendente

[ÉPICO]
    id>
        EP01

    nome>
        estruturar módulos principais

    objetivo>
        criar as especificações iniciais dos módulos centrais da LMC

    inclui>
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE
        LMC-PROCESS
        LMC-TEST

[HISTÓRIA_DE_USUÁRIO]
    id>
        US01

    como>
        usuário que utiliza IA para criar projetos

    quero>
        organizar minhas solicitações em módulos estruturados

    para>
        obter respostas mais claras, reutilizáveis e verificáveis

    prioridade>
        alta

    status>
        em andamento

[CRITÉRIOS_DE_ACEITAÇÃO]
    cada módulo deve ter definição
    cada módulo deve explicar sua finalidade
    cada módulo deve herdar regras do LMC-CORE
    cada módulo deve ter tags próprias
    cada módulo deve ter modelo mínimo e modelo padrão
    cada módulo deve ter exemplo de uso
    cada módulo deve ter regras de interpretação
    os arquivos devem estar em Markdown na pasta specs

[DEFINITION_OF_READY]
    objetivo do módulo definido
    relação com LMC-CORE compreendida
    tags principais planejadas
    exemplos possíveis identificados

[DEFINITION_OF_DONE]
    arquivo Markdown criado
    estrutura do módulo completa
    exemplo incluído
    regras de interpretação definidas
    pronto para commit no GitHub

[SPRINT]
    nome>
        Sprint inicial das especificações

    duração>
        ciclo livre até conclusão dos módulos principais

    objetivo>
        finalizar as especificações iniciais dos módulos da LMC

    entrega>
        módulos principais criados na pasta specs

[TAREFAS]

    tarefa>
        id>
            T01

        nome>
            revisar estrutura do projeto

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T02

        nome>
            criar LMC-CORE

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T03

        nome>
            criar LMC-DOC

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T04

        nome>
            criar LMC-CODE

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T05

        nome>
            criar LMC-EDU

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T06

        nome>
            criar LMC-REQ

        status>
            concluído

        prioridade>
            alta

    tarefa>
        id>
            T07

        nome>
            criar LMC-AGILE

        status>
            em andamento

        prioridade>
            alta

[PRIORIZAÇÃO]
    obrigatórios>
        LMC-CORE
        LMC-DOC
        LMC-CODE
        LMC-EDU
        LMC-REQ
        LMC-AGILE
        LMC-TEST

    desejáveis>
        LMC-PROCESS
        exemplos práticos
        matriz comparativa

    futuros>
        artigo científico
        GitHub Pages
        interpretador LMC
        schemas formais

[DEPENDÊNCIAS]
    os módulos dependem do LMC-CORE
    LMC-AGILE pode usar requisitos vindos do LMC-REQ
    LMC-CODE pode usar histórias e tarefas vindas do LMC-AGILE
    LMC-TEST será usado para validar saídas dos demais módulos

[RISCOS]

    risco>
        descrição>
            os módulos ficarem grandes e repetitivos

        impacto>
            dificultar leitura e manutenção

        mitigação>
            manter cada módulo focado em sua função específica

    risco>
        descrição>
            confundir LMC-AGILE com metodologia Scrum completa

        impacto>
            tornar o módulo excessivamente técnico

        mitigação>
            usar Scrum simplificado e linguagem acessível

[ENTREGA]
    arquivo specs/LMC-AGILE.md criado
    estrutura inicial do módulo definida
    exemplo do LMC-FRAMEWORK incluído

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
    não gerar código
    não criar metodologia ágil nova
    não tornar o módulo excessivamente técnico
    não misturar requisitos com implementação

[FORMATO]
    organizar em seções claras
    usar exemplos em blocos de código
    manter linguagem acessível

[SAÍDA]
    gerar planejamento ágil inicial do LMC-FRAMEWORK
```

---

## 31. Exemplo — sistema web de provas escolares

```txt
[PROTOCOLO_DE_USO]
    tipo>
        planejamento

    ação>
        transformar requisitos em backlog ágil

    escopo>
        não gerar código nesta etapa

[PROJETO]
    sistema_web_provas_escolares

[METODO_AGIL]
    Scrum simplificado

[PRODUTO]
    sistema web de provas escolares

[VISÃO_DO_PRODUTO]
    produto>
        sistema web de provas escolares

    público>
        professores e alunos

    necessidade>
        organizar criação, aplicação, correção e acompanhamento de provas escolares

    valor>
        reduzir retrabalho do professor e facilitar análise dos resultados

[MVP]
    objetivo>
        criar primeira versão funcional para aplicação de provas objetivas

    inclui>
        cadastro de turmas
        criação de provas
        questões objetivas
        chave de acesso por aluno
        resposta da prova
        correção automática
        relatório simples

    não_inclui>
        aplicativo mobile
        integração com diário escolar
        correção automática de questões discursivas
        gráficos avançados

[ÉPICO]
    id>
        EP01

    nome>
        aplicação de provas online

    objetivo>
        permitir que professores criem provas e alunos respondam por chave de acesso

[HISTÓRIA_DE_USUÁRIO]
    id>
        US01

    como>
        professor

    quero>
        cadastrar uma prova com questões objetivas

    para>
        aplicar a avaliação aos alunos de forma organizada

    prioridade>
        alta

[CRITÉRIOS_DE_ACEITAÇÃO]
    professor deve conseguir criar uma prova
    professor deve conseguir cadastrar questões objetivas
    professor deve definir gabarito
    prova deve ficar disponível para aplicação

[HISTÓRIA_DE_USUÁRIO]
    id>
        US02

    como>
        aluno

    quero>
        acessar a prova usando uma chave

    para>
        responder a avaliação sem precisar criar conta

    prioridade>
        alta

[CRITÉRIOS_DE_ACEITAÇÃO]
    aluno deve informar nome, turma e chave
    sistema deve validar a chave
    sistema deve liberar a prova correta
    sistema deve bloquear chave inválida

[HISTÓRIA_DE_USUÁRIO]
    id>
        US03

    como>
        professor

    quero>
        visualizar os resultados dos alunos

    para>
        acompanhar o desempenho da turma

    prioridade>
        média

[CRITÉRIOS_DE_ACEITAÇÃO]
    professor deve visualizar respostas
    sistema deve calcular acertos das questões objetivas
    relatório deve mostrar resultado por aluno
    relatório deve permitir análise por turma

[SPRINT]
    nome>
        Sprint 01 — MVP de provas objetivas

    duração>
        15 dias

    objetivo>
        entregar fluxo básico de criação e resposta de provas objetivas

    itens>
        US01
        US02
        US03

[TAREFAS]
    T01 - criar estrutura de cadastro de prova - alta - pendente
    T02 - criar cadastro de questões objetivas - alta - pendente
    T03 - criar geração de chave por aluno - alta - pendente
    T04 - criar tela de acesso do aluno - alta - pendente
    T05 - criar envio de respostas - alta - pendente
    T06 - criar correção automática - alta - pendente
    T07 - criar relatório simples - média - pendente

[DEFINITION_OF_READY]
    requisitos principais definidos
    histórias com critérios de aceitação
    MVP delimitado
    fora do escopo definido

[DEFINITION_OF_DONE]
    fluxo principal funcionando
    critérios de aceitação atendidos
    testes manuais realizados
    entrega revisada pelo professor

[DEPENDÊNCIAS]
    definição dos dados de turma
    definição do modelo de prova
    definição do modelo de chave de acesso

[RISCOS]
    aluno compartilhar chave
    professor cadastrar gabarito incorreto
    prova ficar disponível fora do período esperado

[ENTREGA]
    backlog inicial e sprint 01 definidos para o sistema web de provas escolares

[SAÍDA]
    gerar planejamento ágil inicial do sistema
```

---

## 32. Regras de interpretação específicas da LMC-AGILE

Ao receber uma instrução LMC-AGILE, a IA deve:

1. Identificar o projeto ou produto.
2. Compreender o objetivo antes de organizar tarefas.
3. Diferenciar visão do produto, MVP, backlog, épico, história e tarefa.
4. Não transformar tudo em tarefa sem antes identificar entregas maiores.
5. Criar histórias de usuário com estrutura clara.
6. Criar critérios de aceitação verificáveis.
7. Diferenciar itens obrigatórios, desejáveis e futuros.
8. Não incluir no MVP funcionalidades marcadas como futuras.
9. Apontar dependências quando uma tarefa depender de outra.
10. Registrar riscos quando houver possibilidade de falha.
11. Não gerar código se o protocolo for planejamento.
12. Não criar metodologia ágil nova sem solicitação.
13. Adaptar a linguagem ao nível do usuário.
14. Evitar excesso de termos técnicos quando o usuário for iniciante.
15. Produzir uma saída que possa alimentar LMC-CODE, LMC-REQ, LMC-DOC ou LMC-TEST.
16. Preservar a validação humana antes da execução.

---

## 33. Critérios de qualidade ágil

Uma saída gerada com LMC-AGILE deve ser avaliada pelos seguintes critérios:

```txt
clareza da visão do produto
delimitação do MVP
organização do backlog
clareza dos épicos
qualidade das histórias de usuário
critérios de aceitação verificáveis
tarefas bem divididas
prioridades claras
dependências identificadas
riscos registrados
definition of ready definida
definition of done definida
coerência entre objetivo e entrega
utilidade prática para execução
```

---

## 34. Relação com outros módulos

A LMC-AGILE pode ser combinada com outros módulos da LMC.

Exemplos:

```txt
LMC-AGILE + LMC-REQ
    transformar requisitos em backlog, épicos e histórias de usuário

LMC-AGILE + LMC-CODE
    transformar histórias e tarefas em código ou protótipos

LMC-AGILE + LMC-DOC
    gerar documentação da sprint, relatório de progresso ou ata de reunião

LMC-AGILE + LMC-PROCESS
    organizar processos operacionais em ciclos de melhoria

LMC-AGILE + LMC-TEST
    verificar se a entrega atende aos critérios de aceitação

LMC-AGILE + LMC-EDU
    organizar projetos educacionais, recuperação contínua e intervenções pedagógicas em ciclos
```

---

## 35. Limites da LMC-AGILE

A LMC-AGILE não garante que o projeto será executado corretamente.

Ela organiza o trabalho, mas não substitui:

```txt
tomada de decisão humana
validação com usuários
gestão real de equipe
análise técnica
testes
revisão de prioridade
acompanhamento contínuo
```

A LMC-AGILE deve ser entendida como uma ferramenta de organização e comunicação com IA, não como substituta completa de gestão de projetos.

---

## 36. Definição acadêmica da LMC-AGILE

A LMC-AGILE pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à estruturação de processos ágeis mediados por Inteligência Artificial, organizando visão de produto, MVP, backlog, épicos, histórias de usuário, critérios de aceitação, tarefas, sprints, prioridades, dependências, riscos e entregas, com o objetivo de reduzir ambiguidades entre a intenção do usuário e o planejamento executável de projetos.

---

## 37. Síntese

A LMC-AGILE organiza projetos em blocos de trabalho claros.

Sua função é ajudar o usuário a comunicar para a IA:

```txt
qual produto está sendo criado
qual problema será resolvido
qual é a primeira versão útil
quais entregas são prioritárias
quais histórias de usuário existem
quais critérios indicam que algo está pronto
quais tarefas precisam ser feitas
quais riscos e dependências existem
qual sprint será executada
qual entrega deve ser validada
```

A LMC-AGILE não substitui métodos ágeis tradicionais. Ela adapta a lógica ágil para melhorar a comunicação humano–IA em projetos, tornando o planejamento mais claro, progressivo e verificável.

---

**Fim da especificação LMC-AGILE**
