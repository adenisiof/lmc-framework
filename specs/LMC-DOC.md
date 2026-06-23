# LMC-DOC v2.2 — Linguagem de Marcação Conceitual para Geração de Documentos

**Autor:** Adenísio Pereira de Freitas
**Categoria:** especificação documental
**Finalidade:** estruturar a comunicação humano–IA para geração, revisão, teste e consolidação de documentos
**Status:** versão em desenvolvimento

---

## 1. Definição
A LMC-DOC é uma especificação documental da Linguagem de Marcação Conceitual voltada à organização da comunicação humano–IA, funcionando como um protocolo de uso capaz de indicar não apenas o conteúdo a ser produzido, mas também o comportamento esperado da IA diante de diferentes tipos de solicitação, como execução, revisão, teste, devolutiva e consolidação.

##A **LMC-DOC** é uma especificação da **LMC — Linguagem de Marcação Conceitual** voltada para a geração de documentos com apoio de Inteligência Artificial.##

Seu objetivo é permitir que o usuário organize a criação de textos, relatórios, artigos, planos de aula, roteiros, atas, resumos e documentos institucionais de forma progressiva, clara e controlada.

A LMC-DOC não tem como finalidade fazer a IA escrever tudo de uma vez. Sua função é organizar o processo de escrita para que a IA siga uma sequência lógica, respeitando objetivo, contexto, estrutura, restrições e formato definidos pelo usuário.

A LMC-DOC atua como uma camada intermediária entre a linguagem natural humana e a resposta produzida pela IA.

Fluxo conceitual:

Humano
↓
LMC-DOC
↓
IA
↓
Documento estruturado

---

## 2. Objetivo da LMC-DOC

A LMC-DOC tem como objetivo:

* estruturar a criação de documentos;
* reduzir ambiguidades nas instruções dadas à IA;
* separar objetivo, contexto, estrutura, conteúdo, controle e saída;
* permitir correções por blocos;
* manter o controle do processo nas mãos do usuário;
* facilitar a reutilização de modelos documentais;
* impedir que a IA antecipe etapas não solicitadas;
* melhorar a coerência entre intenção humana e resposta gerada;
* tornar o processo de escrita mais organizado, verificável e corrigível.

---

## 3. Princípios da LMC-DOC

### P1. Um objetivo por documento

Cada documento deve ter um objetivo principal claramente definido.

### P2. Estrutura antes da redação

Antes de escrever o texto final, a estrutura do documento deve estar definida.

### P3. Escrita em blocos

O documento deve ser construído por partes: seção, tópico, parágrafo ou item.

### P4. Controle do usuário

A IA deve seguir a estrutura fornecida pelo usuário e não substituir o planejamento humano.

### P5. Correção localizada

Erros devem ser corrigidos no bloco em que aparecem, sem reescrever todo o documento desnecessariamente.

### P6. Progressão sequencial

A IA deve avançar etapa por etapa, respeitando a ordem definida na LMC.

### P7. Inferência limitada

A IA só deve completar lacunas quando isso não contrariar o objetivo, o contexto, as restrições e o nível de controle definido.

### P8. Reutilização

Toda estrutura LMC-DOC deve poder ser reaproveitada em outros documentos semelhantes.

### P9. Custo de especificação

A LMC-DOC deve evitar que o esforço para escrever a instrução seja maior que o benefício obtido com a organização do documento.

Se a especificação se torna mais complexa do que o próprio texto solicitado, ela perde parte de sua utilidade prática.

### P10. Redução, não eliminação total da variação

A LMC-DOC não deve prometer que todas as IAs produzirão respostas idênticas. Seu objetivo é reduzir a variação interpretativa da linguagem natural, melhorando a estrutura, a coerência e a aderência ao objetivo do usuário.

---

## 4. Diferença entre documentação e execução

A LMC-DOC pode ser usada de maneiras diferentes.

O usuário pode enviar um bloco LMC para:

* explicar uma especificação;
* gerar um documento;
* revisar um texto;
* testar a saída de uma IA;
* comparar resultados;
* consolidar blocos já aprovados.

Por isso, a LMC-DOC deve indicar logo no início qual é o tipo de uso esperado.

---

## 5. Protocolo de uso

O **protocolo de uso** define o que a IA deve fazer com o bloco LMC recebido.

### Tag principal

```txt
[PROTOCOLO_DE_USO]
```

### Modelo

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente ao que foi solicitado
```

---

## 6. Tipos de uso

### especificação

Usado quando o usuário quer documentar, analisar ou melhorar a própria linguagem LMC-DOC.

A IA deve:

* analisar a estrutura;
* avaliar clareza e coerência;
* sugerir melhorias;
* não gerar documento final, a menos que isso seja pedido.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        especificação

    ação>
        avaliar estrutura da linguagem
```

---

### execução

Usado quando o usuário quer que a IA gere o documento solicitado.

A IA deve:

* seguir as tags informadas;
* respeitar a estrutura;
* produzir a saída definida em `[SAÍDA]`.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final
```

---

### revisão

Usado quando o usuário quer corrigir ou melhorar um texto já produzido.

A IA deve:

* revisar sem alterar a intenção original;
* corrigir ortografia, clareza, coesão ou estrutura conforme solicitado;
* não criar novo documento se o pedido for apenas revisão.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        revisão

    ação>
        corrigir clareza e coerência
```

---

### teste

Usado quando o usuário quer verificar se uma saída respeitou o LMC.

A IA deve:

* comparar o resultado com a estrutura original;
* apontar aderências;
* apontar desvios;
* sugerir ajustes na especificação.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        comparar saída gerada com o LMC original
```

---

### devolutiva

Usado quando o usuário quer uma análise sem avançar para a próxima etapa.

A IA deve:

* avaliar;
* comentar;
* sugerir;
* não executar nova produção textual completa.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        devolutiva

    ação>
        avaliar clareza da estrutura
```

---

### consolidação

Usado quando o usuário quer unir blocos já aprovados.

A IA deve:

* reunir partes já produzidas;
* preservar a intenção original;
* não acrescentar novas ideias principais sem solicitação.

Exemplo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        consolidação

    ação>
        unir seções aprovadas
```

---

## 7. Sintaxe geral

A LMC-DOC utiliza três níveis principais de escrita:

1. **Tags principais**
2. **Subtags conceituais**
3. **Propriedades**

---

## 8. Tags principais

As tags principais são escritas entre colchetes.

Exemplo:

```txt
[OBJETIVO]
[DOCUMENTO]
[ESTRUTURA]
[SAÍDA]
```

Elas indicam os blocos maiores da instrução.

---

## 9. Subtags conceituais

As subtags organizam partes internas de um bloco.

Exemplo:

```txt
seção>
parágrafo>
tópico>
item>
```

Elas devem terminar com o símbolo `>`.

---

## 10. Propriedades

As propriedades indicam características específicas de uma tag ou subtag.

Modelo:

```txt
propriedade>
    valor
```

Exemplo:

```txt
titulo>
    Introdução

objetivo>
    apresentar o problema central

quantidade_paragrafos>
    2
```

---

## 11. Regras de escrita

### R1. Tags principais em letras maiúsculas

Exemplo:

```txt
[OBJETIVO]
```

### R2. Subtags com sinal `>`

Exemplo:

```txt
seção>
```

### R3. Propriedades com valor abaixo

Forma recomendada:

```txt
titulo>
    Introdução
```

Forma compacta permitida:

```txt
titulo>Introdução
```

### R4. Hierarquia por indentação

A indentação indica dependência entre os elementos.

Exemplo:

```txt
seção>
    titulo>
        Introdução

    objetivo>
        apresentar o tema principal

    quantidade_paragrafos>
        1
```

### R5. Ordem como orientação

A IA deve considerar a ordem dos blocos como sequência lógica da tarefa.

### R6. Estrutura fechada

Quando a estrutura estiver definida, a IA não deve criar novas seções sem autorização.

### R7. Sugestão apenas quando solicitada

A IA só deve sugerir melhoria estrutural quando o protocolo indicar `devolutiva`, `teste` ou quando houver uma tag solicitando avaliação.

---

## 12. Estrutura recomendada da LMC-DOC

Ordem sugerida:

```txt
[NOTA]
[PROTOCOLO_DE_USO]
[PROJETO]
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[PÚBLICO_ALVO]
[MODO]
[ESTILO]
[ESTRUTURA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Nem todas as tags são obrigatórias em todos os casos. O usuário deve escolher o nível de detalhamento de acordo com a complexidade do documento.

---

## 13. Base mínima

A base mínima da LMC-DOC é:

```txt
[DOCUMENTO]
[OBJETIVO]
[SAÍDA]
```

Exemplo:

```txt
[DOCUMENTO]
    relatório curto

[OBJETIVO]
    Explicar a importância da tecnologia na educação.

[SAÍDA]
    Gerar texto completo em linguagem clara.
```

---

## 14. Base recomendada

A base recomendada é:

```txt
[PROJETO]
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[PÚBLICO_ALVO]
[MODO]
[ESTILO]
[ESTRUTURA]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

---

## 15. Tags de identificação

### [NOTA]

Define orientações iniciais, metadados ou instruções gerais do LMC.

Exemplo:

```txt
[NOTA]
    Siga as orientações deste LMC.
    tipo = LMC
    categoria = gerador_documento
    versao = 2.2
    modo = consulta_orientada_por_campo
```

---

### [PROJETO]

Define o projeto, tema ou linha de trabalho.

Exemplo:

```txt
[PROJETO]
    artigo_lmc_doc
```

Observação:

`[BRANCH]` pode ser usado como sinônimo técnico de `[PROJETO]`, especialmente em projetos com múltiplas ramificações.

Para usuários não técnicos, recomenda-se `[PROJETO]`.

---

### [DOCUMENTO]

Define o tipo de documento que será produzido.

Exemplos:

```txt
relatório
artigo científico
plano de aula
resumo
roteiro
ata
projeto
declaração
parecer
```

Uso:

```txt
[DOCUMENTO]
    artigo científico
```

---

### [OBJETIVO]

Define a finalidade principal do documento.

Deve responder:

> O que este documento precisa alcançar?

Exemplo:

```txt
[OBJETIVO]
    Apresentar a LMC-DOC como uma linguagem estruturada para melhorar a comunicação entre humanos e Inteligência Artificial.
```

---

### [CONTEXTO]

Apresenta a situação que motivou o documento.

Exemplo:

```txt
[CONTEXTO]
    A linguagem natural possui ambiguidades que podem gerar respostas diferentes entre sistemas de IA.
```

---

### [PÚBLICO_ALVO]

Define para quem o documento será escrito.

Exemplo:

```txt
[PÚBLICO_ALVO]
    professores, pesquisadores e estudantes de tecnologia
```

---

### [MODO]

Define como a IA deve atuar.

Valores sugeridos:

```txt
documento
educacional
científico
acadêmico
institucional
revisão
teste
devolutiva
consolidação
```

Exemplo:

```txt
[MODO]
    documento | científico
```

---

### [ESTILO]

Define o tom da escrita.

Valores sugeridos:

```txt
formal
didático
claro
técnico
científico
acadêmico
institucional
argumentativo
descritivo
conversacional
```

Exemplo:

```txt
[ESTILO]
    formal | didático | claro
```

---

## 16. Tags de estrutura textual

### [ESTRUTURA]

Define a organização do documento.

Pode conter:

* seções;
* tópicos;
* capítulos;
* parágrafos;
* itens.

Modelo recomendado:

```txt
[ESTRUTURA]

    seção>
        titulo>
            Introdução

        objetivo>
            Apresentar o tema principal.

        quantidade_paragrafos>
            1

        descrição>
            Explicar quais ideias devem compor essa seção.

        elementos_obrigatórios>
            conceito principal
            contexto
            justificativa
```

---

### seção>

Define uma parte maior do documento.

Modelo:

```txt
seção>
    titulo>
        nome da seção

    objetivo>
        função da seção no documento

    quantidade_paragrafos>
        número de parágrafos esperados

    descrição>
        ideias que devem orientar a escrita

    elementos_obrigatórios>
        termos, ideias ou argumentos que precisam aparecer

    restrições>
        limites específicos da seção
```

---

### parágrafo>

Define um parágrafo específico dentro do documento.

Modelo:

```txt
parágrafo>
    objetivo>
        função do parágrafo

    descrição>
        ideias que devem aparecer

    elementos_obrigatórios>
        termos ou conceitos obrigatórios

    restrições>
        o que o parágrafo não deve fazer
```

---

### tópico>

Define um tópico dentro de uma seção.

Modelo:

```txt
tópico>
    nome>
        nome do tópico

    objetivo>
        função do tópico

    conteúdo>
        ideia central do tópico

    ordem>
        posição dentro da seção
```

---

### item>

Define um elemento simples em lista, checklist ou enumeração.

Modelo:

```txt
item>
    nome>
        nome do item

    descrição>
        explicação do item

    status>
        pendente | concluído | revisar
```

---

## 17. Tags de conteúdo

### descrição>

A propriedade `descrição>` indica a matéria-prima que a IA deve usar para escrever uma seção ou parágrafo.

Ela deve conter as ideias principais, mesmo que estejam escritas de forma simples.

Exemplo:

```txt
descrição>
    Apresentar o papel da tecnologia na escola, indicando como professores e alunos interagem com recursos digitais no processo de ensino e aprendizagem.
```

A IA pode corrigir ortografia e melhorar fluidez, desde que preserve a intenção do usuário.

---

### elementos_obrigatórios>

Define termos, ideias ou argumentos que precisam aparecer no texto.

Exemplo:

```txt
elementos_obrigatórios>
    tecnologia no contexto escolar
    mídias e recursos digitais
    interação entre professor e aluno
    ensino e aprendizagem
```

---

### benefícios>

Define benefícios específicos que devem ser tratados.

Exemplo:

```txt
benefícios>
    benefício_1>
        diversificação das estratégias de ensino

    benefício_2>
        maior assimilação dos conteúdos
```

---

### cuidados>

Define cuidados específicos que devem ser tratados.

Exemplo:

```txt
cuidados>
    cuidado_1>
        uso excessivo da tecnologia

    cuidado_2>
        distração dos alunos
```

---

## 18. Tags de controle

### [CONTROLE]

Define o grau de liberdade que a IA terá para produzir o documento.

Essa tag evita que o usuário precise escrever muitas restrições longas.

Modelo:

```txt
[CONTROLE]
    nivel>
        moderado

    saida>
        texto_limpo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa
```

---

## 19. Níveis de controle

### nivel>livre

A IA pode organizar, complementar e melhorar o texto com maior liberdade.

Indicado para:

* textos criativos;
* ideias iniciais;
* brainstorm;
* rascunhos.

Exemplo:

```txt
[CONTROLE]
    nivel>
        livre
```

---

### nivel>moderado

A IA deve respeitar estrutura, objetivo, contexto e restrições principais, mas pode fazer ajustes de fluidez, coesão e clareza.

Indicado para:

* relatórios;
* planos de aula;
* textos educacionais;
* documentos simples.

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

* documentos institucionais;
* documentos acadêmicos;
* testes comparativos entre IAs;
* textos com alta necessidade de fidelidade.

Exemplo:

```txt
[CONTROLE]
    nivel>
        rigido
```

---

## 20. Tipos de saída

### saida>texto_limpo

A IA deve entregar apenas o texto final, sem comentários extras.

Significa:

* não escrever frase de apresentação;
* não escrever comentários finais;
* não usar markdown decorativo;
* não usar linhas divisórias;
* não usar símbolos como `#`, `##`, `---`;
* usar apenas títulos e parágrafos quando solicitado.

Exemplo:

```txt
[CONTROLE]
    saida>
        texto_limpo
```

---

### saida>markdown

A IA pode usar formatação Markdown.

Permite:

* títulos com `#`;
* subtítulos;
* listas;
* negrito;
* itálico;
* blocos de citação, quando adequado.

Exemplo:

```txt
[CONTROLE]
    saida>
        markdown
```

---

### saida>documento_formatado

A IA pode criar uma apresentação textual mais organizada, incluindo título geral, subtítulos e separação visual.

Indicado quando o usuário quer um documento visualmente mais completo.

Exemplo:

```txt
[CONTROLE]
    saida>
        documento_formatado
```

---

## 21. Controle de conteúdo

### conteudo>baseado_no_lmc

A IA deve usar principalmente as ideias informadas no LMC, podendo fazer ajustes de coesão.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        baseado_no_lmc
```

---

### conteudo>restrito

A IA deve usar apenas as ideias informadas, sem acrescentar novos conceitos principais.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        restrito
```

---

### conteudo>expandido

A IA pode acrescentar ideias coerentes com o objetivo, desde que não contradiga o contexto.

Exemplo:

```txt
[CONTROLE]
    conteudo>
        expandido
```

---

## 22. Controle de extrapolação

### extrapolacao>baixa

A IA deve evitar ideias novas e manter alta fidelidade ao LMC.

### extrapolacao>media

A IA pode acrescentar pequenos complementos para melhorar fluidez e clareza.

### extrapolacao>alta

A IA pode desenvolver o conteúdo com maior liberdade criativa.

Exemplo:

```txt
[CONTROLE]
    extrapolacao>
        baixa
```

---

## 23. Restrições

### [RESTRIÇÕES]

Define o que a IA não pode fazer ou deve evitar.

Exemplo:

```txt
[RESTRIÇÕES]
    não criar referências bibliográficas fictícias
    não fugir do tema
    não criar novas seções
    não alterar os títulos definidos
```

A tag `[RESTRIÇÕES]` deve ser usada para proibições específicas.

Para controle geral da liberdade da IA, recomenda-se usar `[CONTROLE]`.

---

## 24. Formato

### [FORMATO]

Define a forma final do documento.

Exemplo:

```txt
[FORMATO]
    texto organizado em três seções
    cada seção deve ter título
    usar parágrafos curtos
    linguagem clara e objetiva
```

Diferença entre `[FORMATO]` e `[CONTROLE]`:

* `[FORMATO]` define aparência textual e organização.
* `[CONTROLE]` define grau de liberdade da IA.

---

## 25. Saída

### [SAÍDA]

Define o produto final esperado.

Exemplo:

```txt
[SAÍDA]
    gerar o relatório completo seguindo exatamente a estrutura informada
```

A IA deve produzir apenas o que estiver definido em `[SAÍDA]`, respeitando também `[PROTOCOLO_DE_USO]`.

---

## 26. Tags de revisão e evolução

### [DEVOLUTIVA]

Solicita análise da IA sobre o bloco produzido.

A IA deve analisar sem avançar para a próxima etapa.

Exemplo:

```txt
[DEVOLUTIVA]
    avaliar clareza, coerência e aderência ao objetivo
```

---

### [REVISÃO]

Define o tipo de revisão esperada.

Valores sugeridos:

```txt
ortográfica
gramatical
científica
estrutural
argumentativa
coerência
clareza
adequação ao público
```

Exemplo:

```txt
[REVISÃO]
    corrigir clareza e coerência sem alterar o sentido original
```

---

### [CHECKLIST]

Controla o que foi feito e o que falta.

Exemplo:

```txt
[CHECKLIST]
    feito>
        definição do objetivo

    feito>
        definição da estrutura

    falta>
        redação da introdução

    falta>
        revisão final
```

---

### [CONSOLIDAÇÃO]

Solicita união dos blocos já aprovados.

Exemplo:

```txt
[CONSOLIDAÇÃO]
    unir os parágrafos aprovados em uma seção única
```

---

## 27. Regras de interpretação para a IA

A IA deve:

1. Identificar o `[PROTOCOLO_DE_USO]`.
2. Verificar se deve analisar, executar, revisar, testar ou consolidar.
3. Ler o `[DOCUMENTO]`.
4. Ler o `[OBJETIVO]` antes de gerar qualquer texto.
5. Usar o `[CONTEXTO]` para limitar a interpretação.
6. Respeitar o `[PÚBLICO_ALVO]`.
7. Aplicar o `[ESTILO]`.
8. Seguir a ordem definida em `[ESTRUTURA]`.
9. Respeitar a quantidade de parágrafos quando informada.
10. Usar `descrição>` como base semântica da escrita.
11. Inserir `elementos_obrigatórios>` quando informados.
12. Aplicar `[CONTROLE]` para definir o grau de liberdade.
13. Usar `[RESTRIÇÕES]` como limite prioritário.
14. Seguir `[FORMATO]` para a apresentação textual.
15. Produzir somente o que for pedido em `[SAÍDA]`.
16. Não antecipar etapas futuras.
17. Não criar seções adicionais sem autorização.
18. Não alterar o objetivo original sem solicitação.
19. Quando houver dúvida, evitar extrapolar em excesso.
20. Quando o tipo de uso for `teste`, comparar saída e LMC sem gerar novo documento.
21. Quando o tipo de uso for `devolutiva`, analisar sem executar nova produção completa.
22. Quando o tipo de uso for `consolidação`, unir apenas blocos já aprovados.

---

## 28. Níveis de uso da LMC-DOC

### Nível 1 — Básico

Usa apenas:

```txt
[DOCUMENTO]
[OBJETIVO]
[SAÍDA]
```

Indicado para documentos simples.

---

### Nível 2 — Estruturado

Usa:

```txt
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA]
[RESTRIÇÕES]
[SAÍDA]
```

Indicado para relatórios, planos de aula e artigos simples.

---

### Nível 3 — Controlado

Usa:

```txt
[PROTOCOLO_DE_USO]
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Indicado para documentos que exigem mais fidelidade à intenção do usuário.

---

### Nível 4 — Progressivo

Usa:

```txt
[SEÇÃO]
[PARÁGRAFO]
[DEVOLUTIVA]
[REVISÃO]
[CHECKLIST]
[CONSOLIDAÇÃO]
```

Indicado para construção de textos longos por etapas.

---

## 29. Modelo mínimo

```txt
[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal

[SAÍDA]
    formato esperado
```

---

## 30. Modelo padrão

```txt
[NOTA]
    tipo = LMC
    categoria = gerador_documento
    versao = 2.2
    modo = consulta_orientada_por_campo

[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente ao que foi solicitado

[PROJETO]
    nome_do_projeto

[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal

[CONTEXTO]
    situação ou problema que originou o documento

[PÚBLICO_ALVO]
    leitores ou destinatários

[MODO]
    documento | educacional

[ESTILO]
    formal | didático | claro

[ESTRUTURA]

    seção>
        titulo>
            Introdução

        objetivo>
            apresentar o tema principal

        quantidade_paragrafos>
            1

        descrição>
            ideias que devem compor a seção

        elementos_obrigatórios>
            elemento 1
            elemento 2
            elemento 3

[CONTROLE]
    nivel>
        moderado

    saida>
        texto_limpo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    limites que a IA deve respeitar

[FORMATO]
    forma final desejada

[SAÍDA]
    produto final esperado
```

---

## 31. Exemplo de uso — relatório curto

```txt
[NOTA]
    tipo = LMC
    categoria = gerador_documento
    versao = 2.2
    modo = consulta_orientada_por_campo

[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente com o documento solicitado

[PROJETO]
    teste_lmc_doc_relatorio

[DOCUMENTO]
    relatório curto

[OBJETIVO]
    Criar um relatório simples sobre o uso da tecnologia na educação.

[CONTEXTO]
    A tecnologia está cada vez mais presente nas escolas, mas seu uso precisa estar associado a objetivos pedagógicos claros. O relatório deve apresentar benefícios, cuidados e uma conclusão equilibrada sobre o tema.

[PÚBLICO_ALVO]
    professores e estudantes do Ensino Médio

[MODO]
    documento | educacional

[ESTILO]
    formal | didático | claro

[ESTRUTURA]

    seção>
        titulo>
            Introdução

        objetivo>
            Apresentar o tema do uso da tecnologia na educação.

        quantidade_paragrafos>
            1

        descrição>
            Apresentar o papel e a importância da tecnologia no contexto escolar, explicando como ela está inserida na escola por meio de mídias e recursos digitais. Abordar como professores e alunos interagem com a tecnologia no processo de ensino e aprendizagem.

        elementos_obrigatórios>
            tecnologia no contexto escolar
            mídias e recursos digitais
            interação entre professor e aluno
            ensino e aprendizagem
            aulas mais dinâmicas
            transmissão de informações

    seção>
        titulo>
            Desenvolvimento

        objetivo>
            Explicar dois benefícios e dois cuidados no uso da tecnologia em sala de aula.

        quantidade_paragrafos>
            2

        descrição>
            Explicar que a tecnologia pode contribuir para a diversificação das estratégias de ensino e para maior assimilação dos conteúdos. Também apresentar cuidados como o uso excessivo da tecnologia e a distração dos alunos quando não há orientação adequada.

        benefícios>
            benefício_1>
                diversificação das estratégias de ensino

            benefício_2>
                maior assimilação dos conteúdos

        cuidados>
            cuidado_1>
                uso excessivo da tecnologia

            cuidado_2>
                distração dos alunos

        elementos_obrigatórios>
            diversificação das estratégias de ensino
            assimilação dos conteúdos
            uso excessivo da tecnologia
            distração dos alunos
            planejamento pedagógico
            orientação do professor

    seção>
        titulo>
            Conclusão

        objetivo>
            Apresentar uma posição equilibrada sobre o tema.

        quantidade_paragrafos>
            1

        descrição>
            Concluir que a tecnologia pode ser uma aliada no processo educacional, desde que seja utilizada de forma planejada, equilibrada e com finalidades pedagógicas claras. Reforçar que a tecnologia não substitui o papel do professor.

        elementos_obrigatórios>
            tecnologia como aliada
            uso planejado
            equilíbrio
            finalidade pedagógica
            papel do professor

[CONTROLE]
    nivel>
        moderado

    saida>
        texto_limpo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não usar linguagem excessivamente técnica
    não criar citações ou referências bibliográficas
    não usar tópicos no texto final
    não ultrapassar 500 palavras
    não fugir do tema educação e tecnologia
    não criar novas seções
    não alterar os títulos das seções

[FORMATO]
    texto organizado em três seções
    cada seção deve ter título
    usar parágrafos curtos
    linguagem clara e objetiva

[SAÍDA]
    gerar o relatório completo seguindo a estrutura informada
```

---

## 32. Exemplo de uso — teste de resultado

```txt
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        comparar saída gerada com o LMC original

[OBJETIVO]
    Verificar se o documento gerado respeitou a estrutura, o conteúdo, as restrições e o formato definidos no LMC-DOC.

[BASE_DE_REFERÊNCIA]
    LMC-DOC original usado para gerar o relatório.

[SAÍDA_GERADA]
    Inserir aqui o texto produzido pela IA.

[CRITÉRIOS_DE_AVALIAÇÃO]
    verificar se manteve as seções
    verificar se respeitou a quantidade de parágrafos
    verificar se seguiu o estilo
    verificar se respeitou as restrições
    verificar se houve extrapolação de conteúdo

[SAÍDA]
    apresentar avaliação comparativa com pontos corretos, desvios e sugestões de ajuste
```

---

## 33. Observações sobre diferentes IAs

Testes preliminares indicam que diferentes IAs podem obedecer de forma diferente à mesma estrutura LMC-DOC.

A LMC-DOC tende a controlar melhor:

* estrutura;
* tema;
* quantidade de seções;
* quantidade de parágrafos;
* estilo geral;
* intenção principal.

A LMC-DOC pode ter menor controle sobre:

* uso automático de Markdown;
* frases de apresentação;
* grau de extrapolação;
* enriquecimento textual;
* interpretação fina de benefícios, cuidados ou condições.

Por isso, a LMC-DOC deve ser entendida como ferramenta de redução de ambiguidade, não como garantia absoluta de respostas idênticas.

---

## 34. Definição acadêmica da LMC-DOC

A LMC-DOC pode ser definida como uma especificação da Linguagem de Marcação Conceitual voltada à produção documental assistida por Inteligência Artificial, estruturando objetivos, contexto, seções, parágrafos, restrições, níveis de controle e formatos de saída com o propósito de reduzir ambiguidades da linguagem natural, controlar a progressão textual e preservar a intenção do usuário durante o processo de escrita.

A LMC-DOC não busca eliminar completamente a interpretação da IA, mas reduzir a variação interpretativa e tornar o processo de escrita mais organizado, corrigível e reutilizável.

---

## 35. Síntese da versão 2.2

A LMC-DOC v2.2 introduz três avanços principais:

1. **Protocolo de uso**
   Diferencia especificação, execução, revisão, teste, devolutiva e consolidação.

2. **Controle por níveis**
   Permite definir se a IA terá liberdade livre, moderada ou rígida.

3. **Custo de especificação**
   Reconhece que a LMC deve permanecer simples o suficiente para ser útil ao usuário.

---

## 36. Encerramento

A LMC-DOC é uma linguagem em evolução.

Sua proposta não é substituir a escrita humana, mas organizar a intenção do usuário para que a IA atue como ferramenta de apoio, respeitando estrutura, contexto, limites e objetivos.

A principal contribuição da LMC-DOC é permitir que o usuário conduza o processo de produção textual de forma progressiva, clara e controlada, sem depender apenas de prompts soltos em linguagem natural.

---

**Fim da especificação LMC-DOC v2.2**
