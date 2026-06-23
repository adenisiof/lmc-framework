# LMC-DOC — Especificação Documental da Linguagem de Marcação Conceitual

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo documental
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-DOC.md`

---

## 1. Definição

A **LMC-DOC** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à criação, revisão e organização de documentos com apoio de Inteligência Artificial.

Sua função é estruturar a produção documental por meio de blocos semânticos, permitindo que o usuário defina objetivo, contexto, estrutura, conteúdo, restrições, formato e saída esperada.

A LMC-DOC herda as regras gerais da **LMC-CORE**, especialmente:

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

A LMC-DOC acrescenta regras específicas para documentos, como:

```txt
[DOCUMENTO]
[ESTRUTURA_DOCUMENTAL]
[SEÇÃO]
[PARÁGRAFO]
[TÓPICO]
[ITEM]
```

---

## 2. Finalidade da LMC-DOC

A LMC-DOC tem como finalidade organizar a produção de documentos de forma clara, progressiva e controlada.

Ela pode ser usada para criar:

```txt
relatórios
artigos
planos de aula
resumos
roteiros
atas
pareceres
declarações
projetos
documentos institucionais
materiais educacionais
```

A LMC-DOC não tem como objetivo fazer a IA escrever tudo de uma vez sem controle. Sua finalidade é permitir que o usuário conduza a escrita por etapas, evitando ambiguidades, extrapolações indevidas e perda da intenção original.

---

## 3. Problema que a LMC-DOC busca resolver

A produção de documentos com IA pode apresentar problemas quando o pedido é feito apenas em linguagem natural aberta.

Problemas comuns:

```txt
objetivo pouco claro
estrutura indefinida
excesso de liberdade da IA
criação de informações não solicitadas
mudança de tom durante o texto
seções fora da ordem esperada
dificuldade de revisar apenas uma parte
dificuldade de testar se a IA seguiu o pedido
```

A LMC-DOC reduz esses problemas separando a instrução em blocos documentais.

---

## 4. Princípios da LMC-DOC

### P1. Um documento deve ter objetivo claro

Todo documento deve possuir uma finalidade principal definida em `[OBJETIVO]`.

### P2. A estrutura vem antes da redação

Antes de gerar o texto final, a organização do documento deve estar definida.

### P3. A escrita pode ser feita por blocos

O documento pode ser construído por seções, tópicos, parágrafos ou itens.

### P4. A IA deve respeitar a estrutura definida

Quando a estrutura estiver fechada, a IA não deve criar novas seções sem autorização.

### P5. A revisão deve ser localizada

Quando possível, a correção deve ocorrer no bloco com problema, sem reescrever todo o documento.

### P6. A progressão deve ser controlada

A IA não deve antecipar etapas futuras, como escrever o texto final quando o usuário pediu apenas a estrutura.

### P7. A inferência deve ser limitada

A IA só pode completar lacunas quando isso não contrariar o objetivo, o contexto, as restrições e o nível de controle definido.

### P8. O modelo deve ser reutilizável

Uma estrutura LMC-DOC deve poder ser reaproveitada em documentos semelhantes.

---

## 5. Estrutura básica da LMC-DOC

A estrutura mínima para gerar um documento é:

```txt
[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal

[SAÍDA]
    produto esperado
```

Exemplo:

```txt
[DOCUMENTO]
    relatório curto

[OBJETIVO]
    Explicar a importância da tecnologia na educação.

[SAÍDA]
    Gerar um relatório curto em linguagem clara.
```

---

## 6. Estrutura recomendada da LMC-DOC

Para documentos mais organizados, recomenda-se usar:

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[PÚBLICO_ALVO]
[ESTILO]
[ESTRUTURA_DOCUMENTAL]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Modelo:

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente com o documento solicitado

[PROJETO]
    nome_do_projeto

[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal do documento

[CONTEXTO]
    situação que orienta a produção do documento

[PÚBLICO_ALVO]
    público que receberá o documento

[ESTILO]
    tom da escrita

[ESTRUTURA_DOCUMENTAL]
    organização das seções, tópicos ou parágrafos

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
    limites específicos

[FORMATO]
    forma final do documento

[SAÍDA]
    produto final esperado
```

---

## 7. Tags específicas da LMC-DOC

As tags abaixo pertencem especificamente ao módulo documental.

```txt
[DOCUMENTO]
[ESTRUTURA_DOCUMENTAL]
[SEÇÃO]
[PARÁGRAFO]
[TÓPICO]
[ITEM]
```

As demais tags gerais devem seguir a LMC-CORE.

---

## 8. [DOCUMENTO]

A tag `[DOCUMENTO]` define o tipo de documento que será produzido.

Exemplos:

```txt
relatório
artigo científico
plano de aula
resumo
roteiro
ata
parecer
declaração
projeto
documento institucional
```

Uso:

```txt
[DOCUMENTO]
    artigo científico
```

---

## 9. [ESTILO]

A tag `[ESTILO]` define o tom do documento.

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

## 10. [ESTRUTURA_DOCUMENTAL]

A tag `[ESTRUTURA_DOCUMENTAL]` define a organização interna do documento.

Pode conter:

```txt
seções
capítulos
tópicos
parágrafos
itens
listas
quadros
```

Modelo:

```txt
[ESTRUTURA_DOCUMENTAL]

    seção>
        titulo>
            Introdução

        objetivo>
            apresentar o tema do documento

        quantidade_paragrafos>
            1

        descrição>
            explicar as ideias que devem aparecer na seção

        elementos_obrigatórios>
            tema principal
            contexto
            justificativa
```

---

## 11. seção>

A subtag `seção>` representa uma parte maior do documento.

Modelo:

```txt
seção>
    titulo>
        nome da seção

    objetivo>
        função da seção no documento

    quantidade_paragrafos>
        número esperado de parágrafos

    descrição>
        ideias que devem orientar a escrita

    elementos_obrigatórios>
        termos, ideias ou argumentos que precisam aparecer

    restrições>
        limites específicos da seção
```

Exemplo:

```txt
seção>
    titulo>
        Introdução

    objetivo>
        apresentar o tema e justificar sua importância

    quantidade_paragrafos>
        1

    descrição>
        explicar o problema central e apresentar o contexto geral

    elementos_obrigatórios>
        tema
        problema
        justificativa
```

---

## 12. parágrafo>

A subtag `parágrafo>` representa um parágrafo específico.

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

Exemplo:

```txt
parágrafo>
    objetivo>
        apresentar o problema da comunicação humano-IA

    descrição>
        explicar que a linguagem natural pode gerar ambiguidades na interpretação da IA

    elementos_obrigatórios>
        linguagem natural
        ambiguidade
        interpretação da IA

    restrições>
        não apresentar conclusão ainda
```

---

## 13. tópico>

A subtag `tópico>` representa um assunto interno de uma seção.

Modelo:

```txt
tópico>
    nome>
        nome do tópico

    objetivo>
        função do tópico

    conteúdo>
        ideia central

    ordem>
        posição no documento
```

Exemplo:

```txt
tópico>
    nome>
        Benefícios da tecnologia

    objetivo>
        apresentar contribuições positivas do uso da tecnologia

    conteúdo>
        diversificação das estratégias de ensino

    ordem>
        1
```

---

## 14. item>

A subtag `item>` representa um elemento simples dentro de listas, checklists ou enumerações.

Modelo:

```txt
item>
    nome>
        nome do item

    descrição>
        explicação do item

    status>
        pendente | em_revisão | aprovado
```

Exemplo:

```txt
item>
    nome>
        Definir objetivo do relatório

    descrição>
        identificar a finalidade principal antes da escrita

    status>
        aprovado
```

---

## 15. Propriedades documentais

A LMC-DOC utiliza propriedades para orientar a produção textual.

Principais propriedades:

```txt
titulo>
objetivo>
descrição>
quantidade_paragrafos>
elementos_obrigatórios>
restrições>
ordem>
status>
```

---

## 16. titulo>

Define o título de uma seção, tópico ou parte do documento.

Exemplo:

```txt
titulo>
    Desenvolvimento
```

---

## 17. objetivo>

Define a função de uma parte do documento.

Exemplo:

```txt
objetivo>
    explicar os benefícios e os cuidados relacionados ao uso da tecnologia na educação
```

---

## 18. descrição>

Define a matéria-prima semântica que a IA deve usar para escrever.

Exemplo:

```txt
descrição>
    Explicar que a tecnologia pode ampliar as estratégias de ensino, mas precisa ser usada com planejamento pedagógico.
```

A IA pode melhorar fluidez, ortografia e organização, desde que preserve a intenção original.

---

## 19. quantidade_paragrafos>

Define a quantidade esperada de parágrafos.

Exemplo:

```txt
quantidade_paragrafos>
    2
```

Quando essa propriedade for informada, a IA deve respeitar a quantidade indicada, salvo se houver conflito com outra restrição.

---

## 20. elementos_obrigatórios>

Define termos, conceitos ou ideias que precisam aparecer no texto.

Exemplo:

```txt
elementos_obrigatórios>
    tecnologia no contexto escolar
    planejamento pedagógico
    papel do professor
```

---

## 21. restrições>

Define limites específicos de uma seção, parágrafo, tópico ou item.

Exemplo:

```txt
restrições>
    não criar citações
    não apresentar dados estatísticos não informados
    não concluir o texto nesta seção
```

---

## 22. Ordem de produção documental

A LMC-DOC recomenda a seguinte ordem:

```txt
1. definir o tipo de documento
2. definir o objetivo
3. definir o contexto
4. definir o público-alvo
5. definir o estilo
6. definir a estrutura documental
7. definir o controle
8. definir restrições
9. definir formato
10. gerar ou revisar a saída
```

---

## 23. Níveis de uso da LMC-DOC

### Nível 1 — Básico

Indicado para documentos simples.

```txt
[DOCUMENTO]
[OBJETIVO]
[SAÍDA]
```

---

### Nível 2 — Estruturado

Indicado para relatórios, planos de aula e documentos médios.

```txt
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA_DOCUMENTAL]
[FORMATO]
[SAÍDA]
```

---

### Nível 3 — Controlado

Indicado para documentos que exigem fidelidade maior à intenção do usuário.

```txt
[PROTOCOLO_DE_USO]
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA_DOCUMENTAL]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

---

### Nível 4 — Progressivo

Indicado para textos longos construídos por partes.

```txt
[SEÇÃO]
[PARÁGRAFO]
[DEVOLUTIVA]
[REVISÃO]
[CONSOLIDAÇÃO]
```

---

## 24. Modelo mínimo

```txt
[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal

[SAÍDA]
    produto esperado
```

---

## 25. Modelo padrão

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente com o documento solicitado

[PROJETO]
    nome_do_projeto

[DOCUMENTO]
    tipo do documento

[OBJETIVO]
    finalidade principal do documento

[CONTEXTO]
    situação que orienta o documento

[PÚBLICO_ALVO]
    leitores ou destinatários

[ESTILO]
    formal | didático | claro

[ESTRUTURA_DOCUMENTAL]

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
    não criar informações não fornecidas
    não alterar os títulos definidos
    não criar novas seções

[FORMATO]
    texto organizado em seções
    parágrafos curtos
    linguagem clara

[SAÍDA]
    gerar o documento completo seguindo a estrutura informada
```

---

## 26. Modelo de seção controlada

```txt
[SEÇÃO]
    titulo>
        nome da seção

    objetivo>
        função da seção

    quantidade_paragrafos>
        quantidade esperada

    descrição>
        ideias que devem aparecer

    elementos_obrigatórios>
        conceito 1
        conceito 2

    restrições>
        limite 1
        limite 2

[SAÍDA]
    gerar apenas esta seção
```

---

## 27. Modelo de parágrafo controlado

```txt
[PARÁGRAFO]
    objetivo>
        função do parágrafo

    descrição>
        ideias que devem aparecer

    elementos_obrigatórios>
        conceito 1
        conceito 2

    restrições>
        não concluir o texto
        não criar novas informações

[SAÍDA]
    gerar apenas um parágrafo
```

---

## 28. Exemplo — relatório curto

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar documento final

    escopo>
        responder somente com o relatório solicitado

[PROJETO]
    exemplo_relatorio_tecnologia_educacao

[DOCUMENTO]
    relatório curto

[OBJETIVO]
    Criar um relatório simples sobre o uso da tecnologia na educação.

[CONTEXTO]
    A tecnologia está cada vez mais presente nas escolas, mas seu uso precisa estar associado a objetivos pedagógicos claros.

[PÚBLICO_ALVO]
    professores e estudantes do Ensino Médio

[ESTILO]
    formal | didático | claro

[ESTRUTURA_DOCUMENTAL]

    seção>
        titulo>
            Introdução

        objetivo>
            apresentar o tema da tecnologia na educação

        quantidade_paragrafos>
            1

        descrição>
            explicar a presença da tecnologia no contexto escolar e sua relação com o ensino e a aprendizagem

        elementos_obrigatórios>
            tecnologia no contexto escolar
            recursos digitais
            ensino e aprendizagem

    seção>
        titulo>
            Desenvolvimento

        objetivo>
            apresentar benefícios e cuidados no uso da tecnologia

        quantidade_paragrafos>
            2

        descrição>
            explicar que a tecnologia pode diversificar as estratégias de ensino, mas exige planejamento e orientação do professor

        elementos_obrigatórios>
            diversificação das estratégias de ensino
            planejamento pedagógico
            orientação do professor
            uso excessivo da tecnologia
            distração dos alunos

    seção>
        titulo>
            Conclusão

        objetivo>
            apresentar uma posição equilibrada sobre o tema

        quantidade_paragrafos>
            1

        descrição>
            concluir que a tecnologia pode ser uma aliada no processo educacional quando usada com planejamento e finalidade pedagógica

        elementos_obrigatórios>
            tecnologia como aliada
            uso planejado
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

## 29. Exemplo — artigo científico

```txt
[PROTOCOLO_DE_USO]
    tipo>
        planejamento

    ação>
        estruturar artigo científico

    escopo>
        não escrever o artigo completo

[PROJETO]
    artigo_lmc

[DOCUMENTO]
    artigo científico

[OBJETIVO]
    Estruturar um artigo sobre a LMC como linguagem de comunicação humano-IA.

[CONTEXTO]
    O artigo discutirá a LMC como uma linguagem de marcação conceitual para reduzir ambiguidades em interações com IA.

[PÚBLICO_ALVO]
    pesquisadores, professores e profissionais de tecnologia

[ESTILO]
    acadêmico | técnico | claro

[ESTRUTURA_DOCUMENTAL]

    seção>
        titulo>
            Introdução

        objetivo>
            apresentar o problema, a justificativa e o objetivo do artigo

    seção>
        titulo>
            Fundamentação teórica

        objetivo>
            relacionar linguagem, comunicação humano-IA e estruturação de instruções

    seção>
        titulo>
            Metodologia

        objetivo>
            explicar como a LMC será analisada e testada

    seção>
        titulo>
            Resultados e discussão

        objetivo>
            apresentar e interpretar os testes realizados

    seção>
        titulo>
            Conclusão

        objetivo>
            apresentar contribuições, limites e trabalhos futuros

[RESTRIÇÕES]
    não escrever o artigo completo nesta etapa
    não criar referências bibliográficas fictícias
    não inventar resultados

[SAÍDA]
    gerar apenas a estrutura comentada do artigo
```

---

## 30. Regras de interpretação específicas da LMC-DOC

Ao receber uma instrução LMC-DOC, a IA deve:

1. Identificar o tipo de documento em `[DOCUMENTO]`.
2. Ler o `[OBJETIVO]` antes de iniciar a escrita.
3. Usar o `[CONTEXTO]` para limitar a interpretação.
4. Adaptar a linguagem ao `[PÚBLICO_ALVO]`.
5. Aplicar o `[ESTILO]` informado.
6. Seguir a ordem definida em `[ESTRUTURA_DOCUMENTAL]`.
7. Respeitar os títulos definidos pelo usuário.
8. Respeitar a quantidade de parágrafos quando informada.
9. Usar `descrição>` como base semântica da escrita.
10. Incluir os `elementos_obrigatórios>` quando informados.
11. Respeitar `restrições>` específicas de cada seção ou parágrafo.
12. Aplicar `[CONTROLE]` conforme definido pela LMC-CORE.
13. Priorizar `[RESTRIÇÕES]` quando houver conflito.
14. Seguir o `[FORMATO]` esperado.
15. Produzir somente o que estiver definido em `[SAÍDA]`.
16. Não criar novas seções se a estrutura estiver fechada.
17. Não alterar a intenção do usuário.
18. Não criar referências, dados ou citações não fornecidas.
19. Quando o pedido for revisão, corrigir sem mudar o sentido original.
20. Quando o pedido for consolidação, unir apenas blocos aprovados.

---

## 31. Critérios de qualidade documental

Um documento gerado com LMC-DOC deve ser avaliado pelos seguintes critérios:

```txt
aderência ao objetivo
respeito à estrutura definida
respeito às restrições
coerência entre seções
clareza textual
adequação ao público-alvo
adequação ao estilo solicitado
controle da extrapolação
fidelidade às informações fornecidas
qualidade da saída final
```

---

## 32. Relação com outros módulos

A LMC-DOC pode ser combinada com outros módulos da LMC.

Exemplos:

```txt
LMC-DOC + LMC-EDU
    criação de planos de aula, relatórios pedagógicos e materiais educacionais

LMC-DOC + LMC-REQ
    documentação de requisitos e regras de negócio

LMC-DOC + LMC-AGILE
    documentação de sprints, histórias de usuário e retrospectivas

LMC-DOC + LMC-CODE
    documentação técnica de sistemas e arquivos de projeto

LMC-DOC + LMC-TEST
    avaliação de documentos gerados por diferentes IAs
```

---

## 33. Limites da LMC-DOC

A LMC-DOC não garante que todas as IAs produzirão respostas idênticas.

Ela busca reduzir a variação interpretativa, mas ainda podem ocorrer diferenças em:

```txt
estilo textual
profundidade da explicação
uso automático de Markdown
grau de síntese ou expansão
interpretação de termos abertos
organização visual da resposta
```

Por isso, a LMC-DOC deve ser entendida como ferramenta de controle e redução de ambiguidade, não como garantia absoluta de uniformidade.

---

## 34. Definição acadêmica da LMC-DOC

A LMC-DOC pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à produção documental assistida por Inteligência Artificial, estruturando tipo de documento, objetivo, contexto, público-alvo, estilo, seções, parágrafos, restrições e formato de saída com o propósito de reduzir ambiguidades da linguagem natural, controlar a progressão textual e preservar a intenção do usuário durante o processo de escrita.

---

## 35. Síntese

A LMC-DOC organiza a produção documental em blocos claros.

Sua função é transformar uma intenção textual aberta em uma instrução estruturada, permitindo que a IA compreenda melhor:

```txt
qual documento produzir
para quem produzir
com qual objetivo
em qual contexto
com qual estrutura
com quais limites
em qual formato
```

A LMC-DOC não substitui a escrita humana. Ela organiza a intenção humana para que a IA atue como ferramenta de apoio na produção, revisão e consolidação de documentos.

---

**Fim da especificação LMC-DOC**
