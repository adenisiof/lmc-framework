# LMC-CORE — Núcleo da Linguagem de Marcação Conceitual

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** especificação central
**Status:** versão inicial em desenvolvimento
**Arquivo:** `specs/LMC-CORE.md`

---

## 1. Definição

A **LMC-CORE** é o núcleo da **LMC — Linguagem de Marcação Conceitual**.

Ela define as regras gerais de estruturação da comunicação entre seres humanos e sistemas de Inteligência Artificial, funcionando como uma camada intermediária entre a intenção humana e a interpretação da IA.

A LMC-CORE não pertence a um domínio específico, como documentos, código, educação, requisitos ou processos ágeis. Sua função é definir a base comum que será reutilizada por todos os módulos da LMC.

Fluxo conceitual:

```txt
Humano
↓
LMC
↓
IA
↓
Resultado estruturado
↓
Humano
```

Modelo ampliado:

```txt
Intenção humana
↓
Estruturação em LMC
↓
Interpretação pela IA
↓
Resposta organizada
↓
Validação humana
↓
Uso, revisão ou encaminhamento para outro humano
```

A LMC parte do princípio de que a comunicação futura será cada vez mais mediada por sistemas de IA. Nesse cenário, a comunicação deixa de ser apenas humano-humano e passa a ocorrer no fluxo:

```txt
Humano → IA → Humano
```

ou:

```txt
Humano → IA → Sistema → Humano
```

Por isso, a LMC busca ajudar o usuário a organizar objetivos, contexto, limites, critérios e formatos de saída antes da execução da tarefa pela IA.

---

## 2. Problema que a LMC busca resolver

A linguagem natural humana é flexível, rica e adaptável, mas também pode ser ambígua.

Em muitos casos, uma pessoa acredita ter explicado uma ideia de forma clara, mas o ouvinte pode interpretar de outra maneira. Isso acontece porque pessoas diferentes processam informações de formas diferentes, possuem repertórios distintos, fazem inferências próprias e completam lacunas de acordo com sua experiência.

Quando a comunicação ocorre com uma IA, esse problema continua existindo. A IA interpreta o pedido a partir das informações fornecidas, do contexto disponível, das restrições indicadas e das lacunas presentes na instrução.

Prompts escritos apenas em linguagem natural podem gerar problemas como:

* ambiguidade;
* falta de contexto;
* objetivo pouco definido;
* ausência de critérios de saída;
* excesso de liberdade interpretativa;
* criação de informações não solicitadas;
* mudança de foco durante a resposta;
* dificuldade de testar se a IA seguiu o pedido;
* dificuldade de reaproveitar a mesma instrução em outro contexto.

A LMC busca reduzir esses problemas por meio de uma estrutura simples, organizada em blocos semânticos.

---

## 3. Finalidade da LMC-CORE

A finalidade da LMC-CORE é criar uma base comum para que qualquer módulo da LMC consiga estruturar uma interação humano–IA de forma clara, verificável e reutilizável.

A LMC-CORE deve permitir que o usuário informe:

* o que deseja fazer;
* por que deseja fazer;
* em qual contexto a tarefa ocorre;
* qual papel a IA deve assumir;
* quais limites devem ser respeitados;
* qual grau de liberdade a IA possui;
* qual formato de saída é esperado;
* como a resposta será avaliada;
* se a IA deve executar, revisar, testar, analisar ou consolidar.

A LMC-CORE não substitui o raciocínio humano. Ela organiza o raciocínio humano para que a IA tenha melhores condições de interpretar e executar a solicitação.

---

## 4. O que a LMC não é

A LMC não é apenas um prompt.

A LMC não é uma linguagem de programação tradicional.

A LMC não é uma garantia absoluta de que todas as IAs responderão da mesma forma.

A LMC não elimina completamente a interpretação da IA.

A LMC não deve tornar a instrução mais complexa do que a tarefa que se deseja realizar.

A LMC é uma linguagem de estruturação conceitual para comunicação humano–IA, baseada em blocos, tags, subtags, propriedades, controle de escopo e critérios de saída.

---

## 5. Diferença entre prompt comum e LMC

| Prompt comum                              | LMC                                         |
| ----------------------------------------- | ------------------------------------------- |
| Escrito em linguagem natural livre        | Escrito em linguagem natural estruturada    |
| Pode misturar objetivo, contexto e pedido | Separa objetivo, contexto, controle e saída |
| Pode gerar múltiplas interpretações       | Reduz a variação interpretativa             |
| Difícil de testar                         | Pode ser avaliado por critérios             |
| Pouco reutilizável                        | Pode ser reutilizado e versionado           |
| Depende muito da inferência da IA         | Orienta explicitamente a atuação da IA      |
| Geralmente não registra limites           | Define restrições e nível de controle       |
| Pode antecipar etapas                     | Permite progressão controlada               |

---

## 6. Princípios da LMC-CORE

### P1. Intenção antes da execução

A IA deve compreender primeiro a intenção do usuário antes de produzir a resposta.

### P2. Objetivo explícito

Toda instrução LMC deve deixar claro o objetivo principal da tarefa.

### P3. Contexto delimitado

A IA deve usar o contexto informado para limitar a interpretação da solicitação.

### P4. Controle do usuário

A IA deve seguir a estrutura definida pelo usuário e não substituir o planejamento humano sem autorização.

### P5. Separação de blocos

Objetivo, contexto, restrições, formato, controle e saída devem ser separados sempre que possível.

### P6. Progressão controlada

A IA não deve avançar para etapas não solicitadas.

### P7. Inferência limitada

A IA pode inferir informações apenas quando isso não contrariar o objetivo, o contexto, as restrições e o nível de controle informado.

### P8. Reutilização

Uma estrutura LMC deve poder ser reaproveitada, adaptada e versionada.

### P9. Verificabilidade

A saída da IA deve poder ser comparada com a instrução original.

### P10. Clareza operacional

A LMC deve ser simples o suficiente para ajudar o usuário, e não para criar uma barreira de uso.

### P11. Redução de ambiguidade

A LMC não promete eliminar toda ambiguidade, mas deve reduzir a margem de interpretação indevida.

### P12. Validação humana

A resposta da IA deve ser entendida como produto intermediário ou final dependente de validação humana, principalmente em contextos técnicos, educacionais, científicos, jurídicos, médicos, financeiros ou organizacionais.

---

## 7. Sintaxe geral da LMC

A LMC utiliza três níveis principais:

1. Tags principais;
2. Subtags conceituais;
3. Propriedades.

---

## 8. Tags principais

As tags principais são blocos maiores da instrução.

Devem ser escritas entre colchetes e preferencialmente em letras maiúsculas.

Exemplo:

```txt
[OBJETIVO]
[CONTEXTO]
[CONTROLE]
[RESTRIÇÕES]
[SAÍDA]
```

As tags principais indicam à IA a função de cada bloco.

---

## 9. Subtags conceituais

As subtags organizam partes internas de um bloco.

Devem terminar com o símbolo `>`.

Exemplo:

```txt
tipo>
ação>
escopo>
nivel>
saida>
conteudo>
extrapolacao>
```

---

## 10. Propriedades

As propriedades definem características específicas de uma tag ou subtag.

Forma recomendada:

```txt
propriedade>
    valor
```

Forma compacta permitida:

```txt
propriedade>valor
```

Exemplo:

```txt
nivel>
    moderado

saida>
    markdown

conteudo>
    baseado_no_lmc
```

---

## 11. Indentação

A indentação deve ser usada para indicar dependência entre elementos.

Exemplo:

```txt
[CONTROLE]
    nivel>
        moderado

    saida>
        markdown

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa
```

A indentação não precisa seguir uma quantidade fixa de espaços, mas deve manter coerência visual.

---

## 12. Tags universais da LMC-CORE

As tags universais são aquelas que podem ser usadas por todos os módulos da LMC.

Tags universais principais:

```txt
[NOTA]
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[CONTEXTO]
[PAPEL_DA_IA]
[PÚBLICO_ALVO]
[ENTRADA]
[ESTRUTURA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
[DEVOLUTIVA]
[REVISÃO]
[TESTE]
[CONSOLIDAÇÃO]
```

Nem todas as tags precisam aparecer em toda solicitação. O usuário deve escolher o nível de detalhamento de acordo com a complexidade da tarefa.

---

## 13. [NOTA]

A tag `[NOTA]` registra informações gerais sobre o bloco LMC.

Pode conter metadados, observações, versão, categoria ou orientação inicial.

Exemplo:

```txt
[NOTA]
    tipo = LMC
    categoria = instrução_estruturada
    modulo = LMC-CORE
    status = experimental
```

---

## 14. [PROTOCOLO_DE_USO]

A tag `[PROTOCOLO_DE_USO]` define o que a IA deve fazer com o bloco LMC recebido.

Essa tag é uma das mais importantes da LMC-CORE, porque evita a ambiguidade entre explicar, executar, revisar, testar, devolver análise ou consolidar partes.

Modelo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        executar a tarefa solicitada

    escopo>
        responder somente ao que foi solicitado
```

Tipos de uso recomendados:

```txt
especificação
execução
revisão
teste
devolutiva
consolidação
planejamento
comparação
diagnóstico
```

---

## 15. Tipo: especificação

Usado quando o usuário deseja documentar, analisar ou melhorar a própria LMC ou algum modelo de instrução.

A IA deve:

* analisar a estrutura;
* verificar coerência;
* sugerir melhorias;
* não executar uma tarefa final, a menos que isso seja solicitado.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        especificação

    ação>
        avaliar a estrutura do módulo LMC-CODE
```

---

## 16. Tipo: execução

Usado quando o usuário deseja que a IA execute a tarefa definida.

A IA deve:

* seguir o objetivo;
* respeitar o contexto;
* aplicar restrições;
* entregar a saída solicitada.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar o resultado final
```

---

## 17. Tipo: revisão

Usado quando o usuário deseja corrigir ou melhorar algo já produzido.

A IA deve:

* preservar a intenção original;
* corrigir somente os pontos solicitados;
* evitar reescrever tudo sem necessidade;
* informar quando uma alteração modificar o sentido original.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        revisão

    ação>
        corrigir clareza e coerência
```

---

## 18. Tipo: teste

Usado quando o usuário deseja verificar se uma saída respeitou a estrutura LMC.

A IA deve:

* comparar a saída gerada com a instrução original;
* apontar aderências;
* apontar desvios;
* avaliar restrições, formato e objetivo;
* sugerir ajustes.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        comparar saída gerada com o LMC original
```

---

## 19. Tipo: devolutiva

Usado quando o usuário deseja análise sem execução completa.

A IA deve:

* avaliar;
* comentar;
* apontar riscos;
* sugerir melhorias;
* não avançar para a produção final sem autorização.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        devolutiva

    ação>
        avaliar clareza da proposta
```

---

## 20. Tipo: consolidação

Usado quando o usuário deseja unir partes já aprovadas.

A IA deve:

* reunir blocos existentes;
* preservar a intenção dos blocos originais;
* evitar criar novas ideias centrais;
* organizar a saída final conforme solicitado.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        consolidação

    ação>
        unir os blocos aprovados em uma versão final
```

---

## 21. [PROJETO]

A tag `[PROJETO]` identifica o projeto, módulo, linha de trabalho ou contexto geral.

Exemplo:

```txt
[PROJETO]
    LMC-FRAMEWORK
```

Também pode indicar uma ramificação específica:

```txt
[PROJETO]
    lmc_code_calculadora
```

A tag `[BRANCH]` pode ser usada como sinônimo técnico de `[PROJETO]`, especialmente em contextos de versionamento, testes e desenvolvimento.

---

## 22. [OBJETIVO]

A tag `[OBJETIVO]` define o que deve ser alcançado.

Ela deve responder:

```txt
O que esta solicitação precisa realizar?
```

Exemplo:

```txt
[OBJETIVO]
    Criar a especificação central da LMC-CORE.
```

O objetivo deve ser claro, direto e preferencialmente único.

Quando houver mais de um objetivo, recomenda-se separar em objetivo principal e objetivos secundários.

Modelo:

```txt
[OBJETIVO]
    principal>
        Criar uma estrutura de comunicação humano-IA.

    secundários>
        reduzir ambiguidades
        melhorar organização
        permitir testes de aderência
```

---

## 23. [CONTEXTO]

A tag `[CONTEXTO]` apresenta a situação que motiva a solicitação.

Ela deve informar à IA o cenário de uso, o problema, a necessidade ou as condições relevantes.

Exemplo:

```txt
[CONTEXTO]
    O projeto busca criar uma linguagem de instrução para melhorar a comunicação entre humanos e sistemas de IA em processos de projeto, documentação, software e métodos ágeis.
```

O contexto deve limitar a interpretação da IA.

---

## 24. [PAPEL_DA_IA]

A tag `[PAPEL_DA_IA]` define como a IA deve atuar.

Exemplos:

```txt
[PAPEL_DA_IA]
    atuar como revisora técnica

[PAPEL_DA_IA]
    atuar como assistente de engenharia de requisitos

[PAPEL_DA_IA]
    atuar como avaliadora de aderência à especificação
```

Essa tag ajuda a alinhar o comportamento da IA ao tipo de tarefa.

---

## 25. [PÚBLICO_ALVO]

A tag `[PÚBLICO_ALVO]` define para quem a saída será produzida.

Exemplo:

```txt
[PÚBLICO_ALVO]
    desenvolvedores, professores, pesquisadores e profissionais de projetos
```

A IA deve adaptar linguagem, profundidade e exemplos ao público informado.

---

## 26. [ENTRADA]

A tag `[ENTRADA]` registra os dados, textos, requisitos, exemplos, arquivos ou informações que serão usados pela IA.

Exemplo:

```txt
[ENTRADA]
    texto_base>
        Inserir aqui o texto que será revisado.

    dados>
        Inserir aqui os dados que orientarão a resposta.
```

A IA deve diferenciar claramente o que foi fornecido pelo usuário do que será produzido como saída.

---

## 27. [ESTRUTURA]

A tag `[ESTRUTURA]` define a organização interna esperada para a resposta.

A estrutura pode variar conforme o módulo.

Exemplos:

No módulo documental:

```txt
[ESTRUTURA]
    seção>
        titulo>
            Introdução

        objetivo>
            apresentar o tema
```

No módulo de requisitos:

```txt
[ESTRUTURA]
    requisito>
        tipo>
            funcional

        descrição>
            o sistema deve permitir cadastro de usuários
```

No módulo de código:

```txt
[ESTRUTURA]
    arquivo>
        nome>
            index.html

        função>
            estruturar a interface principal
```

---

## 28. [CONTROLE]

A tag `[CONTROLE]` define o grau de liberdade da IA.

Modelo:

```txt
[CONTROLE]
    nivel>
        moderado

    saida>
        markdown

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa
```

A tag `[CONTROLE]` evita que o usuário precise escrever muitas restrições repetidas.

---

## 29. Controle de nível

### nivel>livre

A IA pode organizar, complementar e desenvolver com maior liberdade.

Indicado para:

* brainstorm;
* ideias iniciais;
* rascunhos;
* exploração criativa.

Exemplo:

```txt
[CONTROLE]
    nivel>
        livre
```

---

### nivel>moderado

A IA deve respeitar objetivo, contexto, estrutura e restrições principais, mas pode melhorar fluidez, clareza e organização.

Indicado para:

* documentos;
* requisitos iniciais;
* planos;
* textos educacionais;
* organização de ideias.

Exemplo:

```txt
[CONTROLE]
    nivel>
        moderado
```

---

### nivel>rigido

A IA deve seguir apenas o que foi informado, evitando novas ideias principais.

Indicado para:

* testes comparativos;
* documentos formais;
* requisitos sensíveis;
* instruções técnicas;
* revisão controlada.

Exemplo:

```txt
[CONTROLE]
    nivel>
        rigido
```

---

## 30. Controle de saída

### saida>texto_limpo

A IA deve entregar apenas o conteúdo final, sem comentários extras.

Exemplo:

```txt
[CONTROLE]
    saida>
        texto_limpo
```

---

### saida>markdown

A IA pode usar formatação Markdown.

Exemplo:

```txt
[CONTROLE]
    saida>
        markdown
```

---

### saida>documento_formatado

A IA pode criar uma apresentação textual organizada, com títulos, subtítulos e separações visuais.

Exemplo:

```txt
[CONTROLE]
    saida>
        documento_formatado
```

---

### saida>codigo

A IA deve entregar código, respeitando o módulo ou linguagem solicitada.

Exemplo:

```txt
[CONTROLE]
    saida>
        codigo
```

---

### saida>tabela

A IA deve organizar a resposta em tabela.

Exemplo:

```txt
[CONTROLE]
    saida>
        tabela
```

---

## 31. Controle de conteúdo

### conteudo>restrito

A IA deve usar apenas as informações fornecidas.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        restrito
```

---

### conteudo>baseado_no_lmc

A IA deve usar principalmente as informações do LMC, podendo melhorar clareza e coesão.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        baseado_no_lmc
```

---

### conteudo>expandido

A IA pode acrescentar ideias coerentes com o objetivo e o contexto.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        expandido
```

---

## 32. Controle de extrapolação

### extrapolacao>baixa

A IA deve evitar ideias novas e manter alta fidelidade ao LMC.

### extrapolacao>media

A IA pode acrescentar pequenos complementos para melhorar a resposta.

### extrapolacao>alta

A IA pode desenvolver a resposta com maior liberdade criativa, desde que não contradiga o objetivo.

Exemplo:

```txt
[CONTROLE]
    extrapolacao>
        baixa
```

---

## 33. [RESTRIÇÕES]

A tag `[RESTRIÇÕES]` define limites específicos.

Exemplo:

```txt
[RESTRIÇÕES]
    não criar informações não fornecidas
    não mudar o objetivo
    não criar novas seções
    não usar linguagem informal
    não avançar para a próxima etapa
```

As restrições devem ter prioridade sobre estilo, fluidez e expansão.

Quando houver conflito entre uma restrição e outra parte da instrução, a IA deve apontar o conflito antes de executar.

---

## 34. [FORMATO]

A tag `[FORMATO]` define a apresentação da resposta.

Exemplo:

```txt
[FORMATO]
    usar Markdown
    organizar em seções curtas
    usar exemplos em blocos de código
    evitar comentários fora da saída
```

Diferença entre `[FORMATO]` e `[CONTROLE]`:

```txt
[FORMATO] define aparência e organização.
[CONTROLE] define liberdade interpretativa.
```

---

## 35. [CRITÉRIOS_DE_ACEITAÇÃO]

A tag `[CRITÉRIOS_DE_ACEITAÇÃO]` define como avaliar se a resposta cumpriu o pedido.

Exemplo:

```txt
[CRITÉRIOS_DE_ACEITAÇÃO]
    deve respeitar todas as tags informadas
    deve manter o objetivo original
    deve usar apenas os módulos solicitados
    deve entregar no formato definido
    deve evitar extrapolação não autorizada
```

Essa tag é importante para testes, validação e comparação entre diferentes IAs.

---

## 36. [SAÍDA]

A tag `[SAÍDA]` define o produto final esperado.

Exemplo:

```txt
[SAÍDA]
    criar a especificação inicial do módulo LMC-CORE em Markdown
```

A IA deve produzir somente o que estiver definido em `[SAÍDA]`, respeitando o protocolo de uso, o controle e as restrições.

---

## 37. [DEVOLUTIVA]

A tag `[DEVOLUTIVA]` solicita análise da IA sem execução completa.

Exemplo:

```txt
[DEVOLUTIVA]
    avaliar se a estrutura está clara, coerente e reutilizável
```

Quando essa tag estiver presente, a IA deve analisar e não avançar para uma produção final sem autorização.

---

## 38. [REVISÃO]

A tag `[REVISÃO]` define o tipo de correção esperada.

Exemplos:

```txt
[REVISÃO]
    corrigir ortografia e clareza sem alterar o sentido

[REVISÃO]
    revisar coerência técnica e apontar inconsistências
```

---

## 39. [TESTE]

A tag `[TESTE]` define uma verificação de aderência.

Exemplo:

```txt
[TESTE]
    comparar a saída gerada com o LMC original
    verificar objetivo, estrutura, controle, restrições e formato
```

---

## 40. [CONSOLIDAÇÃO]

A tag `[CONSOLIDAÇÃO]` solicita união de blocos já aprovados.

Exemplo:

```txt
[CONSOLIDAÇÃO]
    unir os trechos aprovados em uma versão final sem acrescentar novas ideias centrais
```

---

## 41. Ordem recomendada da LMC-CORE

Ordem sugerida:

```txt
[NOTA]
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[CONTEXTO]
[PAPEL_DA_IA]
[PÚBLICO_ALVO]
[ENTRADA]
[ESTRUTURA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

Ordem complementar para evolução:

```txt
[DEVOLUTIVA]
[REVISÃO]
[TESTE]
[CONSOLIDAÇÃO]
```

Nem todas as tags são obrigatórias. A escolha depende da complexidade da tarefa.

---

## 42. Base mínima da LMC

Modelo mínimo:

```txt
[OBJETIVO]
    finalidade principal da solicitação

[CONTEXTO]
    situação que orienta a interpretação

[SAÍDA]
    resultado esperado
```

Exemplo:

```txt
[OBJETIVO]
    Criar uma explicação clara sobre a LMC.

[CONTEXTO]
    O texto será usado no README do projeto.

[SAÍDA]
    gerar um parágrafo introdutório em linguagem simples.
```

---

## 43. Base recomendada da LMC

Modelo recomendado:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        executar a tarefa solicitada

    escopo>
        responder somente ao que foi pedido

[PROJETO]
    nome_do_projeto

[OBJETIVO]
    objetivo principal

[CONTEXTO]
    contexto da solicitação

[PAPEL_DA_IA]
    papel esperado da IA

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
    limites específicos

[FORMATO]
    forma da resposta

[SAÍDA]
    produto final esperado
```

---

## 44. Modelo completo da LMC-CORE

```txt
[NOTA]
    tipo = LMC
    modulo = LMC-CORE
    categoria = instrucao_estruturada
    status = experimental

[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        executar a tarefa solicitada

    escopo>
        responder somente ao que foi solicitado

[PROJETO]
    nome_do_projeto

[OBJETIVO]
    principal>
        objetivo principal

    secundários>
        objetivo secundário 1
        objetivo secundário 2

[CONTEXTO]
    situação, problema ou necessidade que orienta a solicitação

[PAPEL_DA_IA]
    papel que a IA deve assumir

[PÚBLICO_ALVO]
    público que receberá a saída

[ENTRADA]
    dados, texto, exemplos ou informações de base

[ESTRUTURA]
    organização esperada da resposta

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
    limite 1
    limite 2
    limite 3

[FORMATO]
    formato esperado da resposta

[CRITÉRIOS_DE_ACEITAÇÃO]
    critério 1
    critério 2
    critério 3

[SAÍDA]
    produto final esperado
```

---

## 45. Regras de interpretação para a IA

Ao receber uma instrução em LMC, a IA deve:

1. Identificar o `[PROTOCOLO_DE_USO]`.
2. Verificar se deve executar, revisar, testar, analisar, planejar ou consolidar.
3. Ler o `[OBJETIVO]` antes de gerar qualquer resposta.
4. Usar o `[CONTEXTO]` para limitar a interpretação.
5. Assumir o papel definido em `[PAPEL_DA_IA]`, quando informado.
6. Considerar o `[PÚBLICO_ALVO]` para ajustar linguagem e profundidade.
7. Usar `[ENTRADA]` como base da resposta.
8. Respeitar a ordem e a organização indicadas em `[ESTRUTURA]`.
9. Aplicar o grau de liberdade definido em `[CONTROLE]`.
10. Priorizar `[RESTRIÇÕES]` em caso de conflito.
11. Seguir o `[FORMATO]` informado.
12. Verificar os `[CRITÉRIOS_DE_ACEITAÇÃO]`.
13. Produzir apenas o que estiver solicitado em `[SAÍDA]`.
14. Não criar novas etapas sem autorização.
15. Não alterar o objetivo original.
16. Não inventar dados, referências, resultados ou decisões não informadas quando o controle for restrito ou rígido.
17. Declarar incertezas quando uma informação essencial estiver ausente.
18. Solicitar esclarecimento quando a ausência de informação impedir a execução responsável.
19. Sugerir melhoria somente quando o protocolo ou a devolutiva permitirem.
20. Preservar a validação humana como etapa final em tarefas relevantes.

---

## 46. Níveis de uso da LMC

### Nível 1 — Básico

Usa:

```txt
[OBJETIVO]
[SAÍDA]
```

Indicado para tarefas simples.

---

### Nível 2 — Contextual

Usa:

```txt
[OBJETIVO]
[CONTEXTO]
[SAÍDA]
```

Indicado para tarefas que precisam de orientação mínima.

---

### Nível 3 — Estruturado

Usa:

```txt
[PROTOCOLO_DE_USO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA]
[RESTRIÇÕES]
[SAÍDA]
```

Indicado para respostas organizadas.

---

### Nível 4 — Controlado

Usa:

```txt
[PROTOCOLO_DE_USO]
[OBJETIVO]
[CONTEXTO]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

Indicado para tarefas que exigem maior fidelidade.

---

### Nível 5 — Verificável

Usa:

```txt
[TESTE]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA_GERADA]
[BASE_DE_REFERÊNCIA]
```

Indicado para comparar saídas de IA e avaliar aderência.

---

## 47. Relação entre LMC-CORE e módulos

A LMC-CORE define as regras gerais.

Os demais módulos especializam essas regras para contextos específicos.

Módulos previstos:

```txt
LMC-DOC      → documentos, relatórios, artigos, planos, atas e roteiros
LMC-CODE     → software, código, interfaces, validações e arquitetura
LMC-REQ      → requisitos, regras de negócio, stakeholders e critérios de aceitação
LMC-AGILE    → épicos, histórias de usuário, sprint, backlog e tarefas
LMC-PROCESS  → processos, fluxos, melhorias, indicadores e operações
LMC-EDU      → educação, planos de aula, metodologias, avaliações e relatórios pedagógicos
LMC-TEST     → testes, comparação de saídas e avaliação de aderência
```

Cada módulo pode criar tags próprias, desde que respeite os princípios da LMC-CORE.

---

## 48. Regra de herança dos módulos

Todo módulo da LMC deve herdar da LMC-CORE:

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[CONTEXTO]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

Cada módulo pode acrescentar tags específicas.

Exemplo:

No LMC-DOC:

```txt
[DOCUMENTO]
[ESTRUTURA]
seção>
parágrafo>
```

No LMC-CODE:

```txt
[SISTEMA]
[ARQUIVOS]
[FUNCIONALIDADES]
[TESTES]
```

No LMC-REQ:

```txt
[STAKEHOLDERS]
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
```

---

## 49. Custo de especificação

A LMC deve respeitar o princípio do custo de especificação.

Isso significa que a estrutura LMC não deve ser mais difícil, demorada ou confusa do que a própria tarefa que se deseja realizar.

Quando a tarefa for simples, o usuário deve usar uma estrutura simples.

Quando a tarefa for complexa, a LMC pode usar mais tags, controle e critérios de aceitação.

Regra prática:

```txt
Tarefa simples → LMC simples
Tarefa média → LMC estruturada
Tarefa crítica → LMC controlada e verificável
```

---

## 50. Definição acadêmica da LMC-CORE

A LMC-CORE pode ser definida como o núcleo de uma linguagem de marcação conceitual voltada à estruturação de instruções em interações humano–IA, organizando objetivos, contexto, papéis, entradas, restrições, níveis de controle, critérios de aceitação e formatos de saída, com o propósito de reduzir ambiguidades da linguagem natural, melhorar a aderência da resposta da IA à intenção humana e favorecer processos comunicacionais verificáveis no fluxo humano–IA–humano.

---

## 51. Síntese da LMC-CORE

A LMC-CORE estabelece que uma boa comunicação com IA deve explicitar:

```txt
o que fazer
por que fazer
em qual contexto fazer
qual papel a IA deve assumir
quais informações usar
quais limites respeitar
qual liberdade interpretativa é permitida
qual formato entregar
como avaliar se a resposta cumpriu o pedido
```

A LMC não pretende substituir a linguagem natural, mas organizá-la.

Sua função é transformar uma intenção humana aberta em uma instrução estruturada, interpretável, reutilizável e verificável.

---

**Fim da especificação LMC-CORE**
