# LMC-TEST — Especificação para Teste e Avaliação de Saídas Geradas por IA

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo de teste e validação
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-TEST.md`

---

## 1. Definição

A **LMC-TEST** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à avaliação, comparação e validação de respostas geradas por Inteligência Artificial a partir de uma instrução LMC.

Sua função é verificar se a saída produzida pela IA respeitou o objetivo, o contexto, a estrutura, as restrições, o formato, os critérios de aceitação e a saída esperada.

A LMC-TEST permite transformar uma avaliação subjetiva em uma análise mais organizada, verificável e comparável.

Fluxo conceitual:

```txt id="efv9gw"
LMC original
↓
IA executa
↓
Saída gerada
↓
LMC-TEST
↓
Avaliação de aderência
↓
Correção da saída ou ajuste da especificação
```

A LMC-TEST pode ser usada para avaliar uma única resposta ou comparar respostas de diferentes IAs, como ChatGPT, Copilot, Gemini, Claude ou outras ferramentas.

---

## 2. Finalidade da LMC-TEST

A LMC-TEST tem como finalidade verificar se uma IA cumpriu corretamente uma instrução estruturada.

Ela pode ser usada para avaliar:

```txt id="8bpwtl"
documentos gerados
relatórios
planos de aula
códigos
requisitos
backlogs
processos
atividades educacionais
respostas comparativas
revisões feitas por IA
consolidações de texto
saídas de diferentes IAs
```

A LMC-TEST não serve apenas para dizer se a resposta está “boa” ou “ruim”. Ela deve identificar:

```txt id="3vp4ty"
o que foi seguido corretamente
o que foi ignorado
o que foi inventado
o que ficou incompleto
o que precisa ser corrigido
se o problema está na saída da IA ou na especificação original
```

---

## 3. Problema que a LMC-TEST busca resolver

Ao usar IA, muitas respostas parecem corretas à primeira vista, mas podem apresentar desvios.

Problemas comuns:

```txt id="k7gkyg"
a IA não segue a estrutura solicitada
a IA cria informações não fornecidas
a IA ignora restrições
a IA muda o tom ou o formato
a IA antecipa etapas não pedidas
a IA entrega algo parcialmente correto
a IA gera código que parece bom, mas não funciona
a IA cria seções extras
a IA esquece elementos obrigatórios
a IA responde com explicações quando o usuário pediu apenas a saída final
```

A LMC-TEST busca reduzir esses problemas avaliando a saída de forma estruturada.

---

## 4. Relação com a LMC-CORE

A LMC-TEST herda as regras gerais da **LMC-CORE**, especialmente:

```txt id="llpdtu"
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[CONTEXTO]
[PAPEL_DA_IA]
[ENTRADA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

A LMC-TEST acrescenta tags específicas para avaliação:

```txt id="wg8dfg"
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[IA_AVALIADA]
[CRITÉRIOS_DE_TESTE]
[MÉTRICAS]
[ADERÊNCIA]
[DESVIOS]
[OMISSÕES]
[EXTRAPOLAÇÕES]
[ERROS]
[PONTUAÇÃO]
[RESULTADO_DO_TESTE]
[RECOMENDAÇÕES]
[AJUSTES_NA_ESPECIFICAÇÃO]
[AJUSTES_NA_SAÍDA]
[COMPARAÇÃO_ENTRE_IAS]
```

---

## 5. Princípios da LMC-TEST

### P1. A avaliação deve partir da instrução original

A saída deve ser comparada com o LMC original, não apenas com a opinião do avaliador.

### P2. Critérios antes da nota

Antes de atribuir pontuação, devem ser definidos os critérios avaliados.

### P3. Aderência não é perfeição

Uma saída pode estar parcialmente aderente, mesmo que tenha desvios.

### P4. Separar erro da IA e falha da especificação

Quando a saída falhar, a LMC-TEST deve indicar se o problema está na resposta da IA, na instrução mal definida ou em ambos.

### P5. Identificar omissões

A avaliação deve apontar elementos solicitados que não apareceram na saída.

### P6. Identificar extrapolações

A avaliação deve apontar informações, seções ou decisões criadas sem autorização.

### P7. Avaliação verificável

Sempre que possível, a avaliação deve se apoiar em evidências da saída gerada.

### P8. Comparação justa

Ao comparar IAs diferentes, todas devem receber a mesma base de referência e os mesmos critérios.

### P9. Teste como melhoria

O objetivo do teste não é apenas apontar erro, mas melhorar a instrução, a saída e o próprio módulo LMC.

### P10. Validação humana

A pontuação da LMC-TEST orienta a decisão, mas a validação final permanece humana.

---

## 6. Estrutura mínima da LMC-TEST

A estrutura mínima é:

```txt id="z2e95h"
[BASE_DE_REFERÊNCIA]
    instrução LMC original

[SAÍDA_GERADA]
    resposta produzida pela IA

[SAÍDA]
    avaliação esperada
```

Exemplo:

```txt id="f8cp4u"
[BASE_DE_REFERÊNCIA]
    LMC original usado para gerar um relatório curto.

[SAÍDA_GERADA]
    Texto produzido pela IA.

[SAÍDA]
    avaliar se o texto respeitou objetivo, estrutura, restrições e formato.
```

---

## 7. Estrutura recomendada da LMC-TEST

```txt id="50owpw"
[PROTOCOLO_DE_USO]
[PROJETO]
[OBJETIVO]
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[IA_AVALIADA]
[CRITÉRIOS_DE_TESTE]
[MÉTRICAS]
[ADERÊNCIA]
[DESVIOS]
[OMISSÕES]
[EXTRAPOLAÇÕES]
[ERROS]
[PONTUAÇÃO]
[RESULTADO_DO_TESTE]
[RECOMENDAÇÕES]
[AJUSTES_NA_ESPECIFICAÇÃO]
[AJUSTES_NA_SAÍDA]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[SAÍDA]
```

Para comparação entre várias IAs, incluir:

```txt id="03aeia"
[COMPARAÇÃO_ENTRE_IAS]
[MATRIZ_COMPARATIVA]
[CONCLUSÃO_COMPARATIVA]
```

---

## 8. [BASE_DE_REFERÊNCIA]

A tag `[BASE_DE_REFERÊNCIA]` contém a instrução original que será usada como referência do teste.

Pode conter:

```txt id="7e8zuv"
LMC original
requisitos originais
critérios de aceitação
estrutura esperada
restrições
formato solicitado
objetivo inicial
```

Exemplo:

```txt id="ktetjy"
[BASE_DE_REFERÊNCIA]
    Inserir aqui o LMC original usado para gerar a resposta.
```

A avaliação deve sempre retornar a essa base antes de julgar a saída.

---

## 9. [SAÍDA_GERADA]

A tag `[SAÍDA_GERADA]` contém a resposta produzida pela IA.

Exemplo:

```txt id="htwcth"
[SAÍDA_GERADA]
    Inserir aqui o texto, código, documento, requisito, processo ou resposta produzida pela IA.
```

A LMC-TEST deve avaliar essa saída em relação à base de referência.

---

## 10. [IA_AVALIADA]

A tag `[IA_AVALIADA]` identifica qual IA produziu a saída.

Exemplo:

```txt id="emzyj9"
[IA_AVALIADA]
    ChatGPT
```

Outro exemplo:

```txt id="oejssm"
[IA_AVALIADA]
    Copilot
```

Quando a avaliação for comparativa, essa tag pode aparecer dentro de cada bloco de saída.

---

## 11. [CRITÉRIOS_DE_TESTE]

A tag `[CRITÉRIOS_DE_TESTE]` define o que será avaliado.

Critérios gerais recomendados:

```txt id="juuc6g"
aderência ao objetivo
respeito ao contexto
respeito à estrutura
respeito às restrições
respeito ao formato
completude da saída
ausência de informações inventadas
controle de extrapolação
clareza da resposta
utilidade da saída
```

Modelo:

```txt id="p1fmhc"
[CRITÉRIOS_DE_TESTE]

    critério>
        nome>
            aderência ao objetivo

        descrição>
            verificar se a saída responde ao objetivo definido no LMC original

        peso>
            2
```

---

## 12. [MÉTRICAS]

A tag `[MÉTRICAS]` define a forma de pontuação.

Modelo simples:

```txt id="vc0ala"
[MÉTRICAS]
    escala>
        0 a 10

    interpretação>
        0 = não atendeu
        5 = atendeu parcialmente
        10 = atendeu completamente
```

Modelo por nível:

```txt id="gi8u8k"
[MÉTRICAS]
    0>
        não atendeu

    1>
        atendeu muito pouco

    2>
        atendeu parcialmente

    3>
        atendeu bem

    4>
        atendeu muito bem

    5>
        atendeu completamente
```

Para a versão inicial, recomenda-se usar escala de 0 a 10.

---

## 13. [ADERÊNCIA]

A tag `[ADERÊNCIA]` registra os pontos em que a saída seguiu corretamente a instrução.

Modelo:

```txt id="wts8ab"
[ADERÊNCIA]
    manteve a estrutura solicitada
    respeitou o tema
    usou o formato esperado
    incluiu os elementos obrigatórios
```

A aderência deve ser descrita com base em evidências da saída.

---

## 14. [DESVIOS]

A tag `[DESVIOS]` registra diferenças entre a saída gerada e a instrução original.

Exemplo:

```txt id="4kym23"
[DESVIOS]
    criou uma seção não solicitada
    usou tópicos quando o formato pedia parágrafos
    mudou o título definido pelo usuário
```

Desvio não significa necessariamente erro grave, mas indica afastamento da especificação.

---

## 15. [OMISSÕES]

A tag `[OMISSÕES]` registra elementos solicitados que não apareceram na saída.

Exemplo:

```txt id="6211wd"
[OMISSÕES]
    não incluiu conclusão
    não mencionou um elemento obrigatório
    não apresentou instruções de execução
    não incluiu teste esperado
```

Omissões devem ser comparadas diretamente com a base de referência.

---

## 16. [EXTRAPOLAÇÕES]

A tag `[EXTRAPOLAÇÕES]` registra informações, seções ou decisões criadas sem autorização.

Exemplo:

```txt id="u6c6a8"
[EXTRAPOLAÇÕES]
    criou referências bibliográficas não fornecidas
    acrescentou funcionalidade fora do escopo
    assumiu tecnologia não solicitada
    criou dados não informados pelo usuário
```

Extrapolação é especialmente importante quando o controle é `rigido` ou a extrapolação esperada é `baixa`.

---

## 17. [ERROS]

A tag `[ERROS]` registra falhas objetivas da saída.

Exemplos:

```txt id="6hsmhy"
erro conceitual
erro de cálculo
erro de código
erro de estrutura
erro de interpretação
erro de formato
erro de coerência
```

Modelo:

```txt id="rogo1c"
[ERROS]

    erro>
        tipo>
            erro de formato

        descrição>
            a IA usou Markdown, mas a instrução pedia texto limpo

        gravidade>
            baixa | média | alta
```

---

## 18. [PONTUAÇÃO]

A tag `[PONTUAÇÃO]` registra notas por critério.

Modelo:

```txt id="5tpdv5"
[PONTUAÇÃO]

    critério>
        nome>
            aderência ao objetivo

        nota>
            9

        justificativa>
            a saída respondeu ao objetivo principal, com pequena expansão não solicitada
```

Também pode ser usada em formato de tabela:

```txt id="vhu996"
| Critério | Nota | Justificativa |
|---|---:|---|
| Aderência ao objetivo | 9 | Atendeu ao objetivo principal |
| Estrutura | 8 | Manteve quase toda a estrutura |
| Restrições | 7 | Ignorou uma restrição |
```

---

## 19. [RESULTADO_DO_TESTE]

A tag `[RESULTADO_DO_TESTE]` apresenta a conclusão do teste.

Valores sugeridos:

```txt id="h2xwyv"
aprovado
aprovado com ajustes
parcialmente aderente
reprovado
inconclusivo
```

Modelo:

```txt id="2h6o6q"
[RESULTADO_DO_TESTE]
    status>
        aprovado com ajustes

    síntese>
        a saída seguiu o objetivo e a estrutura, mas descumpriu uma restrição de formato
```

---

## 20. [RECOMENDAÇÕES]

A tag `[RECOMENDAÇÕES]` apresenta orientações para melhorar a próxima resposta.

Exemplo:

```txt id="h66dg1"
[RECOMENDAÇÕES]
    reforçar a restrição sobre não criar novas seções
    especificar melhor o formato de saída
    incluir critérios de aceitação mais objetivos
```

As recomendações podem ser voltadas para a IA, para o usuário ou para a especificação.

---

## 21. [AJUSTES_NA_ESPECIFICAÇÃO]

A tag `[AJUSTES_NA_ESPECIFICAÇÃO]` sugere melhorias no LMC original.

Exemplo:

```txt id="gd4jnh"
[AJUSTES_NA_ESPECIFICAÇÃO]
    adicionar [CRITÉRIOS_DE_ACEITAÇÃO]
    deixar explícito que a saída deve ter apenas três seções
    informar se a IA pode ou não usar Markdown
```

Essa tag é usada quando o problema está na instrução original ou quando ela pode ser melhorada.

---

## 22. [AJUSTES_NA_SAÍDA]

A tag `[AJUSTES_NA_SAÍDA]` sugere correções na resposta gerada.

Exemplo:

```txt id="txz9ei"
[AJUSTES_NA_SAÍDA]
    remover seção criada sem solicitação
    reescrever conclusão respeitando o objetivo original
    ajustar código para impedir divisão por zero
```

Essa tag é usada quando a saída precisa ser corrigida sem alterar a especificação.

---

## 23. [COMPARAÇÃO_ENTRE_IAS]

A tag `[COMPARAÇÃO_ENTRE_IAS]` é usada para comparar respostas geradas por diferentes IAs a partir da mesma base de referência.

Modelo:

```txt id="0wo2rq"
[COMPARAÇÃO_ENTRE_IAS]

    ia>
        nome>
            ChatGPT

        saída>
            inserir saída gerada

    ia>
        nome>
            Copilot

        saída>
            inserir saída gerada

    ia>
        nome>
            Gemini

        saída>
            inserir saída gerada
```

A comparação só deve ser feita de forma justa quando todas as IAs receberem a mesma instrução original.

---

## 24. [MATRIZ_COMPARATIVA]

A tag `[MATRIZ_COMPARATIVA]` organiza a comparação entre IAs.

Modelo:

```txt id="lhyjtg"
[MATRIZ_COMPARATIVA]

| Critério | ChatGPT | Copilot | Gemini | Observação |
|---|---:|---:|---:|---|
| Aderência ao objetivo | 9 | 8 | 7 | ChatGPT manteve melhor o foco |
| Respeito à estrutura | 10 | 8 | 7 | Copilot alterou uma seção |
| Restrições | 8 | 7 | 6 | Gemini extrapolou mais |
```

A matriz permite comparar resultados de forma visual e objetiva.

---

## 25. [CONCLUSÃO_COMPARATIVA]

A tag `[CONCLUSÃO_COMPARATIVA]` apresenta a leitura final da comparação.

Exemplo:

```txt id="pqqvrl"
[CONCLUSÃO_COMPARATIVA]
    A saída do ChatGPT apresentou maior aderência estrutural. O Copilot apresentou boa clareza, mas alterou parte da estrutura. O Gemini produziu resposta mais livre, com maior extrapolação em relação ao LMC original.
```

A conclusão deve ser baseada nos critérios e não apenas em preferência pessoal.

---

## 26. Índice de Aderência à LMC

A LMC-TEST pode usar um índice simples para medir aderência.

Nome sugerido:

```txt id="m48o6c"
IALMC — Índice de Aderência à LMC
```

Modelo inicial:

```txt id="0pe3tk"
IALMC = média dos critérios avaliados
```

Critérios sugeridos:

```txt id="8gma9y"
aderência ao objetivo
respeito ao contexto
respeito à estrutura
respeito às restrições
respeito ao formato
completude
controle de extrapolação
clareza
utilidade
```

Exemplo:

```txt id="zfk6be"
IALMC = (9 + 8 + 10 + 7 + 8 + 9 + 7 + 9 + 8) / 9
IALMC = 8,3
```

Classificação sugerida:

```txt id="kr1jrf"
0,0 a 3,9  → baixa aderência
4,0 a 5,9  → aderência limitada
6,0 a 7,4  → aderência parcial
7,5 a 8,9  → boa aderência
9,0 a 10   → alta aderência
```

---

## 27. Tipos de teste

### Teste estrutural

Verifica se a saída respeitou a estrutura solicitada.

Exemplo:

```txt id="8pwy5y"
a saída manteve as seções?
a saída manteve a ordem?
a saída criou seções extras?
```

### Teste de conteúdo

Verifica se a saída usou os elementos obrigatórios e evitou informações não autorizadas.

Exemplo:

```txt id="p7u6g4"
incluiu os conceitos obrigatórios?
omitiu alguma informação importante?
criou informações não fornecidas?
```

### Teste de formato

Verifica se a saída respeitou a forma final esperada.

Exemplo:

```txt id="kfi7jm"
entregou em Markdown?
entregou texto limpo?
usou tabela quando solicitado?
evitou comentários extras?
```

### Teste de restrição

Verifica se a IA obedeceu às proibições e limites.

Exemplo:

```txt id="jvculc"
não criou referências?
não alterou títulos?
não usou bibliotecas externas?
não gerou código quando o pedido era apenas planejamento?
```

### Teste funcional

Usado principalmente no LMC-CODE para verificar se o código funciona.

Exemplo:

```txt id="08uf1s"
o código executa?
a calculadora soma corretamente?
a validação impede divisão por zero?
o arquivo abre no navegador?
```

### Teste pedagógico

Usado no LMC-EDU para verificar adequação educacional.

Exemplo:

```txt id="df5jyp"
a atividade está adequada ao ano/série?
a intervenção corresponde à dificuldade?
a linguagem do relatório é pedagógica?
```

### Teste de processo

Usado no LMC-PROCESS para verificar coerência do fluxo.

Exemplo:

```txt id="zq1kxq"
entradas e saídas estão claras?
as etapas seguem ordem lógica?
as melhorias estão ligadas aos gargalos?
```

---

## 28. Níveis de uso da LMC-TEST

### Nível 1 — Avaliação simples

Indicado para análise rápida de uma saída.

```txt id="21uhcr"
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[SAÍDA]
```

---

### Nível 2 — Avaliação por critérios

Indicado para avaliar aderência com mais clareza.

```txt id="e1usku"
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[CRITÉRIOS_DE_TESTE]
[PONTUAÇÃO]
[RESULTADO_DO_TESTE]
```

---

### Nível 3 — Avaliação completa

Indicado para testes formais.

```txt id="xtmrzv"
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[ADERÊNCIA]
[DESVIOS]
[OMISSÕES]
[EXTRAPOLAÇÕES]
[ERROS]
[PONTUAÇÃO]
[RECOMENDAÇÕES]
[RESULTADO_DO_TESTE]
```

---

### Nível 4 — Comparação entre IAs

Indicado para comparar respostas de diferentes sistemas.

```txt id="hgs26v"
[BASE_DE_REFERÊNCIA]
[COMPARAÇÃO_ENTRE_IAS]
[MATRIZ_COMPARATIVA]
[CONCLUSÃO_COMPARATIVA]
```

---

### Nível 5 — Teste com melhoria da especificação

Indicado para evoluir a própria LMC.

```txt id="f6zyxg"
[BASE_DE_REFERÊNCIA]
[SAÍDA_GERADA]
[RESULTADO_DO_TESTE]
[AJUSTES_NA_ESPECIFICAÇÃO]
[AJUSTES_NA_SAÍDA]
[RECOMENDAÇÕES]
```

---

## 29. Modelo mínimo

```txt id="ywjyx6"
[BASE_DE_REFERÊNCIA]
    inserir LMC original

[SAÍDA_GERADA]
    inserir resposta gerada pela IA

[SAÍDA]
    avaliar aderência da saída ao LMC original
```

---

## 30. Modelo padrão

```txt id="9olglq"
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        avaliar saída gerada por IA

    escopo>
        comparar a saída com a base de referência

[PROJETO]
    nome_do_projeto

[OBJETIVO]
    Verificar se a saída gerada respeitou o LMC original.

[BASE_DE_REFERÊNCIA]
    inserir LMC original

[SAÍDA_GERADA]
    inserir saída produzida pela IA

[IA_AVALIADA]
    nome da IA avaliada

[CRITÉRIOS_DE_TESTE]
    aderência ao objetivo
    respeito ao contexto
    respeito à estrutura
    respeito às restrições
    respeito ao formato
    completude
    controle de extrapolação
    clareza
    utilidade

[MÉTRICAS]
    escala>
        0 a 10

    interpretação>
        0 = não atendeu
        5 = atendeu parcialmente
        10 = atendeu completamente

[CONTROLE]
    nivel>
        rigido

    saida>
        markdown

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não gerar nova versão da saída, a menos que seja solicitado
    não avaliar por preferência pessoal
    não ignorar critérios da base de referência
    não inventar informações sobre a execução

[FORMATO]
    apresentar avaliação em seções
    incluir pontuação por critério
    incluir resultado final
    incluir recomendações

[SAÍDA]
    gerar avaliação completa da saída em relação ao LMC original
```

---

## 31. Exemplo — teste de relatório LMC-DOC

```txt id="qa81xu"
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        avaliar saída documental

    escopo>
        comparar relatório gerado com o LMC-DOC original

[PROJETO]
    teste_relatorio_tecnologia_educacao

[OBJETIVO]
    Verificar se o relatório produzido respeitou objetivo, estrutura, restrições e formato.

[BASE_DE_REFERÊNCIA]
    [DOCUMENTO]
        relatório curto

    [OBJETIVO]
        Criar um relatório simples sobre o uso da tecnologia na educação.

    [ESTRUTURA_DOCUMENTAL]
        seção>
            titulo>
                Introdução

            quantidade_paragrafos>
                1

        seção>
            titulo>
                Desenvolvimento

            quantidade_paragrafos>
                2

        seção>
            titulo>
                Conclusão

            quantidade_paragrafos>
                1

    [RESTRIÇÕES]
        não usar tópicos no texto final
        não ultrapassar 500 palavras
        não criar novas seções
        não alterar os títulos das seções

    [SAÍDA]
        gerar relatório completo seguindo a estrutura informada

[SAÍDA_GERADA]
    Inserir aqui o relatório produzido pela IA.

[IA_AVALIADA]
    ChatGPT

[CRITÉRIOS_DE_TESTE]
    manteve as três seções
    respeitou a quantidade de parágrafos
    não criou tópicos
    não ultrapassou 500 palavras
    não criou novas seções
    manteve linguagem clara
    respeitou o tema

[MÉTRICAS]
    escala>
        0 a 10

[FORMATO]
    apresentar avaliação com aderências, desvios, omissões, extrapolações, pontuação e resultado final

[SAÍDA]
    gerar avaliação do relatório
```

---

## 32. Exemplo — teste de código LMC-CODE

```txt id="0bb17x"
[PROTOCOLO_DE_USO]
    tipo>
        teste

    ação>
        avaliar código gerado por IA

    escopo>
        verificar se o código respeitou a especificação LMC-CODE

[PROJETO]
    teste_calculadora_web

[OBJETIVO]
    Verificar se o código gerado atende à especificação da calculadora web simples.

[BASE_DE_REFERÊNCIA]
    [SISTEMA]
        calculadora web simples

    [TECNOLOGIAS]
        HTML
        CSS
        JavaScript

    [FUNCIONALIDADES]
        somar
        subtrair
        multiplicar
        dividir
        limpar campos

    [VALIDAÇÕES]
        verificar campos preenchidos
        verificar valores numéricos
        impedir divisão por zero

    [ARQUIVOS]
        arquivo>
            nome>
                index.html

            conteúdo>
                HTML, CSS e JavaScript no mesmo arquivo

    [RESTRIÇÕES]
        não usar bibliotecas externas
        não separar em múltiplos arquivos
        não exigir instalação
        não criar funcionalidades extras

    [CRITÉRIOS_DE_ACEITAÇÃO]
        deve funcionar ao abrir no navegador
        deve executar as quatro operações
        deve impedir divisão por zero
        deve limpar campos
        deve exibir mensagens claras

[SAÍDA_GERADA]
    Inserir aqui o código HTML produzido pela IA.

[IA_AVALIADA]
    Copilot

[CRITÉRIOS_DE_TESTE]
    código completo
    uso correto de HTML, CSS e JavaScript
    arquivo único
    funcionamento das operações
    validação de campos
    bloqueio de divisão por zero
    botão limpar funcional
    ausência de bibliotecas externas
    clareza da interface
    facilidade de execução

[MÉTRICAS]
    escala>
        0 a 10

[FORMATO]
    apresentar avaliação técnica com tabela de critérios, erros encontrados e recomendações

[SAÍDA]
    gerar avaliação do código gerado
```

---

## 33. Exemplo — comparação entre ChatGPT e Copilot

```txt id="6usgu8"
[PROTOCOLO_DE_USO]
    tipo>
        comparação

    ação>
        comparar saídas de diferentes IAs

    escopo>
        usar os mesmos critérios para todas as saídas

[PROJETO]
    comparacao_calculadora_web

[OBJETIVO]
    Comparar os códigos gerados por ChatGPT e Copilot a partir da mesma especificação LMC-CODE.

[BASE_DE_REFERÊNCIA]
    Inserir aqui o LMC-CODE original usado nas duas IAs.

[COMPARAÇÃO_ENTRE_IAS]

    ia>
        nome>
            ChatGPT

        saída>
            inserir código gerado pelo ChatGPT

    ia>
        nome>
            Copilot

        saída>
            inserir código gerado pelo Copilot

[CRITÉRIOS_DE_TESTE]
    aderência ao objetivo
    respeito às tecnologias
    funcionalidades implementadas
    validações implementadas
    respeito às restrições
    organização do código
    facilidade de execução
    clareza da interface

[MÉTRICAS]
    escala>
        0 a 10

[MATRIZ_COMPARATIVA]
    gerar tabela comparativa com notas por critério

[CONCLUSÃO_COMPARATIVA]
    indicar qual saída apresentou maior aderência ao LMC original e justificar

[SAÍDA]
    gerar comparação entre as saídas das IAs
```

---

## 34. Regras de interpretação específicas da LMC-TEST

Ao receber uma instrução LMC-TEST, a IA deve:

1. Identificar a base de referência antes de avaliar a saída.
2. Comparar a saída gerada com a instrução original.
3. Avaliar por critérios, não apenas por opinião geral.
4. Apontar aderências.
5. Apontar desvios.
6. Apontar omissões.
7. Apontar extrapolações.
8. Apontar erros objetivos quando houver.
9. Atribuir pontuação apenas quando houver métrica definida.
10. Justificar as notas atribuídas.
11. Diferenciar erro da saída e falha da especificação original.
12. Não gerar nova saída corrigida se o usuário pediu apenas avaliação.
13. Sugerir ajustes na especificação quando o LMC original estiver ambíguo.
14. Sugerir ajustes na saída quando a resposta gerada estiver incompleta ou incorreta.
15. Em comparação entre IAs, aplicar os mesmos critérios para todas.
16. Não favorecer uma IA por preferência pessoal.
17. Preservar a validação humana como etapa final.

---

## 35. Critérios de qualidade de teste

Uma saída gerada com LMC-TEST deve ser avaliada pelos seguintes critérios:

```txt id="e5oh6z"
clareza da avaliação
comparação direta com a base de referência
identificação de aderências
identificação de desvios
identificação de omissões
identificação de extrapolações
identificação de erros
justificativa das notas
uso coerente das métricas
recomendações úteis
separação entre problema da IA e problema da especificação
utilidade para melhorar testes futuros
```

---

## 36. Relação com outros módulos

A LMC-TEST pode ser combinada com todos os módulos da LMC.

Exemplos:

```txt id="86yqkw"
LMC-TEST + LMC-DOC
    avaliar documentos, relatórios, artigos, planos e textos gerados

LMC-TEST + LMC-CODE
    avaliar código, funcionalidades, validações e critérios técnicos

LMC-TEST + LMC-EDU
    avaliar planos de aula, atividades, relatórios e intervenções pedagógicas

LMC-TEST + LMC-REQ
    avaliar se requisitos foram bem estruturados e se estão verificáveis

LMC-TEST + LMC-AGILE
    avaliar backlog, histórias, critérios de aceitação e sprints

LMC-TEST + LMC-PROCESS
    avaliar fluxos, etapas, indicadores, gargalos e melhorias
```

---

## 37. Limites da LMC-TEST

A LMC-TEST não garante uma avaliação absoluta ou totalmente objetiva.

Ela reduz a subjetividade ao usar critérios, mas ainda depende de:

```txt id="4omh6m"
qualidade da base de referência
clareza dos critérios
interpretação do avaliador
complexidade da tarefa
tipo de saída avaliada
validação humana
```

Em código, a LMC-TEST pode analisar estrutura e lógica, mas testes reais de execução ainda podem ser necessários.

Em documentos, a LMC-TEST pode avaliar aderência e coerência, mas a qualidade final pode depender do contexto humano.

---

## 38. Definição acadêmica da LMC-TEST

A LMC-TEST pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à avaliação de saídas geradas por Inteligência Artificial, estruturando base de referência, saída gerada, critérios de teste, métricas, aderências, desvios, omissões, extrapolações, erros, pontuação e recomendações, com o objetivo de verificar a aderência da resposta da IA à intenção original do usuário e apoiar a melhoria contínua das especificações LMC.

---

## 39. Síntese

A LMC-TEST organiza a avaliação de respostas da IA em blocos claros.

Sua função é ajudar o usuário a verificar:

```txt id="b3sqoz"
se a IA entendeu o objetivo
se respeitou o contexto
se seguiu a estrutura
se obedeceu às restrições
se entregou no formato solicitado
se omitiu algo importante
se inventou informações
se extrapolou o pedido
se cometeu erros
se a especificação original precisa melhorar
```

A LMC-TEST fecha o ciclo da LMC, permitindo que cada resposta gerada seja analisada, comparada, corrigida e usada para melhorar as próximas instruções.

---

**Fim da especificação LMC-TEST**
