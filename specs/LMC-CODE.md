# LMC-CODE — Especificação para Geração de Código com Inteligência Artificial

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo de desenvolvimento de software
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-CODE.md`

---

## 1. Definição

A **LMC-CODE** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado à criação, organização, revisão e geração de código com apoio de Inteligência Artificial.

Sua função é permitir que o usuário descreva um sistema, página, aplicação, componente ou funcionalidade em linguagem estruturada, sem precisar escrever diretamente em uma linguagem de programação.

A LMC-CODE atua como uma camada intermediária entre a ideia humana e a implementação técnica gerada pela IA.

Fluxo conceitual:

```txt
Ideia humana
↓
LMC-CODE
↓
IA
↓
Código gerado
↓
Teste humano
↓
Correção ou evolução
```

A LMC-CODE não substitui o conhecimento técnico em programação, mas permite que usuários com pouca ou nenhuma experiência em código consigam organizar requisitos, funcionalidades e comportamentos esperados de forma mais clara para a IA.

---

## 2. Finalidade da LMC-CODE

A LMC-CODE tem como finalidade estruturar pedidos de geração de código de forma clara, progressiva e verificável.

Ela pode ser usada para criar:

```txt
páginas HTML
interfaces web
calculadoras
formulários
sistemas simples
componentes de tela
scripts JavaScript
aplicações educacionais
protótipos
painéis
ferramentas automatizadas
documentação técnica de código
```

O usuário informa o que deseja construir.
A IA interpreta a estrutura LMC-CODE e gera o código conforme as regras, tecnologias, funcionalidades e restrições definidas.

---

## 3. Problema que a LMC-CODE busca resolver

A geração de código com IA pode falhar quando o pedido é feito apenas em linguagem natural aberta.

Problemas comuns:

```txt
o usuário não sabe explicar tecnicamente o que quer
a IA escolhe tecnologias não solicitadas
a IA mistura interface, lógica e dados sem organização
o código gerado não atende ao objetivo
faltam validações
faltam instruções de uso
o sistema funciona parcialmente
a IA cria funcionalidades não pedidas
a IA divide arquivos quando o usuário queria tudo junto
a IA entrega explicações demais quando o usuário queria apenas código
```

A LMC-CODE reduz esses problemas ao separar a solicitação em blocos como sistema, objetivo, tecnologias, funcionalidades, interface, entradas, processamento, saídas, validações, arquivos e testes.

---

## 4. Relação com a LMC-CORE

A LMC-CODE herda as regras gerais da **LMC-CORE**, especialmente:

```txt
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

A LMC-CODE acrescenta tags específicas para desenvolvimento de software:

```txt
[SISTEMA]
[TIPO_DE_SISTEMA]
[TECNOLOGIAS]
[FUNCIONALIDADES]
[INTERFACE]
[ENTRADAS]
[PROCESSAMENTO]
[REGRAS_DE_NEGOCIO]
[SAÍDAS]
[VALIDAÇÕES]
[ARQUIVOS]
[TESTES]
[EXECUÇÃO]
```

---

## 5. Princípios da LMC-CODE

### P1. Ideia antes do código

Antes de gerar código, a IA deve compreender o objetivo do sistema.

### P2. Usuário não precisa programar

A LMC-CODE deve permitir que o usuário descreva o sistema em linguagem clara, mesmo sem conhecer programação.

### P3. Código deve obedecer ao objetivo

A IA não deve criar funcionalidades principais que não foram solicitadas.

### P4. Funcionalidades devem ser explícitas

Cada funcionalidade esperada deve ser declarada de forma clara.

### P5. Interface e comportamento devem ser separados quando possível

Mesmo em sistemas simples, a LMC-CODE deve diferenciar aparência, entrada de dados, processamento e saída.

### P6. Validações devem ser informadas

Quando houver entrada de dados, a IA deve considerar validações para evitar erros de uso.

### P7. Código deve ser testável

A saída deve permitir que o usuário execute, teste e identifique se o sistema funciona.

### P8. Simplicidade na versão inicial

A LMC-CODE deve começar simples. A separação em camadas mais avançadas pode ser feita em versões futuras.

---

## 6. Estrutura mínima da LMC-CODE

A estrutura mínima para gerar código é:

```txt
[SISTEMA]
    tipo ou nome do sistema

[OBJETIVO]
    o que o sistema deve fazer

[SAÍDA]
    qual código deve ser gerado
```

Exemplo:

```txt
[SISTEMA]
    calculadora web simples

[OBJETIVO]
    Criar uma calculadora que some, subtraia, multiplique e divida dois números.

[SAÍDA]
    gerar um arquivo HTML completo com CSS e JavaScript no mesmo arquivo
```

---

## 7. Estrutura recomendada da LMC-CODE

Para gerar código com mais controle, recomenda-se usar:

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[SISTEMA]
[TIPO_DE_SISTEMA]
[OBJETIVO]
[CONTEXTO]
[PÚBLICO_ALVO]
[TECNOLOGIAS]
[FUNCIONALIDADES]
[INTERFACE]
[ENTRADAS]
[PROCESSAMENTO]
[REGRAS_DE_NEGOCIO]
[SAÍDAS]
[VALIDAÇÕES]
[ARQUIVOS]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[TESTES]
[SAÍDA]
```

Nem todas as tags precisam ser usadas em todo projeto. Quanto mais simples for o sistema, menor pode ser a estrutura.

---

## 8. [SISTEMA]

A tag `[SISTEMA]` define o nome ou descrição geral do sistema a ser criado.

Exemplo:

```txt
[SISTEMA]
    calculadora web
```

Outro exemplo:

```txt
[SISTEMA]
    organizador de tarefas para estudantes
```

---

## 9. [TIPO_DE_SISTEMA]

A tag `[TIPO_DE_SISTEMA]` define a categoria do sistema.

Valores possíveis:

```txt
página web
aplicação web
formulário
calculadora
jogo simples
painel
script
componente
protótipo
sistema educacional
sistema administrativo
```

Exemplo:

```txt
[TIPO_DE_SISTEMA]
    aplicação web simples
```

---

## 10. [TECNOLOGIAS]

A tag `[TECNOLOGIAS]` define quais tecnologias devem ser usadas.

Exemplo:

```txt
[TECNOLOGIAS]
    HTML
    CSS
    JavaScript
```

Outro exemplo:

```txt
[TECNOLOGIAS]
    Python
    SQLite
```

Quando o usuário não souber escolher tecnologias, pode usar:

```txt
[TECNOLOGIAS]
    escolher tecnologia simples e adequada para o objetivo
```

Nesse caso, a IA deve justificar brevemente a escolha antes de gerar o código, se o protocolo permitir explicação.

---

## 11. [FUNCIONALIDADES]

A tag `[FUNCIONALIDADES]` descreve o que o sistema deve fazer.

Modelo:

```txt
[FUNCIONALIDADES]

    funcionalidade>
        nome>
            nome da funcionalidade

        descrição>
            o que essa funcionalidade deve fazer

        prioridade>
            obrigatória | desejável | futura
```

Exemplo:

```txt
[FUNCIONALIDADES]

    funcionalidade>
        nome>
            calcular operações básicas

        descrição>
            permitir soma, subtração, multiplicação e divisão entre dois números

        prioridade>
            obrigatória
```

---

## 12. [INTERFACE]

A tag `[INTERFACE]` define como o usuário deve interagir visualmente com o sistema.

Pode incluir:

```txt
campos
botões
menus
títulos
cores
posicionamento
mensagens
layout
responsividade
```

Modelo:

```txt
[INTERFACE]
    titulo>
        título visível da página

    campos>
        campo 1
        campo 2

    botoes>
        botão 1
        botão 2

    layout>
        descrição visual da tela
```

Exemplo:

```txt
[INTERFACE]
    titulo>
        Calculadora Simples

    campos>
        número 1
        número 2

    botoes>
        somar
        subtrair
        multiplicar
        dividir
        limpar

    layout>
        centralizado na tela, simples, claro e responsivo
```

---

## 13. [ENTRADAS]

A tag `[ENTRADAS]` define quais dados o usuário fornecerá ao sistema.

Modelo:

```txt
[ENTRADAS]

    entrada>
        nome>
            nome do dado

        tipo>
            texto | número | data | seleção | arquivo | booleano

        obrigatório>
            sim | não
```

Exemplo:

```txt
[ENTRADAS]

    entrada>
        nome>
            número 1

        tipo>
            número

        obrigatório>
            sim

    entrada>
        nome>
            número 2

        tipo>
            número

        obrigatório>
            sim
```

---

## 14. [PROCESSAMENTO]

A tag `[PROCESSAMENTO]` define o que o sistema deve fazer internamente com as entradas.

Exemplo:

```txt
[PROCESSAMENTO]
    receber dois números
    identificar a operação escolhida
    calcular o resultado
    exibir o resultado na tela
```

Essa tag ajuda a IA a separar a lógica do sistema da aparência visual.

---

## 15. [REGRAS_DE_NEGOCIO]

A tag `[REGRAS_DE_NEGOCIO]` define regras que o sistema deve obedecer.

Exemplo:

```txt
[REGRAS_DE_NEGOCIO]
    não permitir divisão por zero
    exibir mensagem de erro quando os campos estiverem vazios
    permitir apenas valores numéricos
```

Em sistemas mais complexos, as regras de negócio devem ser separadas das funcionalidades.

---

## 16. [SAÍDAS]

A tag `[SAÍDAS]` define o que o sistema deve apresentar ao usuário após o processamento.

Exemplo:

```txt
[SAÍDAS]
    resultado da operação
    mensagem de erro quando houver entrada inválida
    mensagem de orientação quando faltar algum campo
```

---

## 17. [VALIDAÇÕES]

A tag `[VALIDAÇÕES]` define verificações obrigatórias antes de executar uma ação.

Exemplo:

```txt
[VALIDAÇÕES]
    verificar se os campos foram preenchidos
    verificar se os valores são números
    impedir divisão por zero
    limpar mensagens antigas antes de novo cálculo
```

As validações ajudam a evitar que o código funcione apenas no caso ideal.

---

## 18. [ARQUIVOS]

A tag `[ARQUIVOS]` define como o código deve ser entregue.

Exemplo para arquivo único:

```txt
[ARQUIVOS]
    arquivo>
        nome>
            index.html

        conteúdo>
            HTML, CSS e JavaScript no mesmo arquivo
```

Exemplo para arquivos separados:

```txt
[ARQUIVOS]

    arquivo>
        nome>
            index.html

        função>
            estrutura da página

    arquivo>
        nome>
            style.css

        função>
            aparência visual

    arquivo>
        nome>
            script.js

        função>
            lógica da aplicação
```

Na versão inicial da LMC-CODE, recomenda-se permitir o modelo de arquivo único para facilitar testes por usuários iniciantes.

---

## 19. [EXECUÇÃO]

A tag `[EXECUÇÃO]` explica como o usuário deve rodar ou testar o sistema.

Exemplo:

```txt
[EXECUÇÃO]
    salvar o arquivo como index.html
    abrir o arquivo no navegador
    preencher os campos
    clicar em uma operação
    verificar o resultado exibido
```

Essa tag é importante para usuários que não conhecem ambiente de desenvolvimento.

---

## 20. [TESTES]

A tag `[TESTES]` define testes simples para verificar se o sistema funciona.

Modelo:

```txt
[TESTES]

    teste>
        nome>
            nome do teste

        entrada>
            dados usados no teste

        resultado_esperado>
            resultado esperado
```

Exemplo:

```txt
[TESTES]

    teste>
        nome>
            soma simples

        entrada>
            número 1 = 10
            número 2 = 5
            operação = soma

        resultado_esperado>
            15

    teste>
        nome>
            divisão por zero

        entrada>
            número 1 = 10
            número 2 = 0
            operação = divisão

        resultado_esperado>
            exibir mensagem de erro
```

---

## 21. [FORMATO_CODIGO]

A tag `[FORMATO_CODIGO]` define preferências de organização do código.

Exemplo:

```txt
[FORMATO_CODIGO]
    código comentado
    nomes de variáveis claros
    evitar complexidade desnecessária
    usar funções separadas para cada operação
```

Essa tag pode ser usada quando o usuário deseja código mais legível.

---

## 22. [CRITÉRIOS_DE_ACEITAÇÃO]

A tag `[CRITÉRIOS_DE_ACEITAÇÃO]` define quando o código pode ser considerado correto.

Exemplo:

```txt
[CRITÉRIOS_DE_ACEITAÇÃO]
    deve abrir no navegador sem erro
    deve permitir somar dois números
    deve permitir subtrair dois números
    deve permitir multiplicar dois números
    deve impedir divisão por zero
    deve exibir mensagens claras
    deve estar em um único arquivo HTML
```

Essa tag é essencial para avaliar se a IA cumpriu a solicitação.

---

## 23. Controle de complexidade

A LMC-CODE deve permitir três níveis de complexidade.

### Nível simples

Indicado para usuários iniciantes.

Características:

```txt
arquivo único
HTML, CSS e JavaScript juntos
sem banco de dados
sem instalação
execução direta no navegador
```

### Nível intermediário

Indicado para pequenos projetos organizados.

Características:

```txt
arquivos separados
estrutura de pastas simples
funções reutilizáveis
separação entre interface e lógica
```

### Nível avançado

Indicado para sistemas maiores.

Características:

```txt
arquitetura em camadas
persistência de dados
autenticação
regras de negócio separadas
testes automatizados
integração com APIs
```

Na versão inicial, a LMC-CODE prioriza o nível simples e intermediário.

---

## 24. Camadas futuras da LMC-CODE

Em versões futuras, a LMC-CODE poderá ser dividida em camadas específicas.

Modelo futuro previsto:

```txt
[CAMADA_INTERFACE]
    tela
    layout
    componentes
    eventos do usuário

[CAMADA_NEGOCIO]
    regras
    cálculos
    decisões
    validações

[CAMADA_DADOS]
    entidades
    campos
    estruturas internas

[CAMADA_PERSISTENCIA]
    banco de dados
    arquivos
    localStorage
    APIs

[CAMADA_TESTES]
    casos de teste
    resultados esperados
    validação
```

Nesta versão inicial, essas camadas podem aparecer de forma simplificada dentro de:

```txt
[INTERFACE]
[PROCESSAMENTO]
[REGRAS_DE_NEGOCIO]
[VALIDAÇÕES]
[TESTES]
```

---

## 25. Modelo mínimo

```txt
[SISTEMA]
    nome ou tipo do sistema

[OBJETIVO]
    o que o sistema deve fazer

[SAÍDA]
    código esperado
```

---

## 26. Modelo padrão

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar código

    escopo>
        responder somente com o código solicitado e instruções mínimas de execução

[PROJETO]
    nome_do_projeto

[SISTEMA]
    nome do sistema

[TIPO_DE_SISTEMA]
    tipo do sistema

[OBJETIVO]
    objetivo principal do sistema

[CONTEXTO]
    situação ou necessidade que motivou o sistema

[PÚBLICO_ALVO]
    usuários finais do sistema

[TECNOLOGIAS]
    tecnologias que devem ser usadas

[FUNCIONALIDADES]

    funcionalidade>
        nome>
            nome da funcionalidade

        descrição>
            descrição do que deve fazer

        prioridade>
            obrigatória

[INTERFACE]
    descrição dos elementos visuais

[ENTRADAS]
    dados fornecidos pelo usuário

[PROCESSAMENTO]
    lógica que o sistema deve executar

[REGRAS_DE_NEGOCIO]
    regras que devem ser respeitadas

[SAÍDAS]
    resultados exibidos ao usuário

[VALIDAÇÕES]
    verificações necessárias

[ARQUIVOS]
    forma de entrega do código

[CONTROLE]
    nivel>
        moderado

    saida>
        codigo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    limites que a IA deve respeitar

[FORMATO_CODIGO]
    preferências de organização do código

[CRITÉRIOS_DE_ACEITAÇÃO]
    condições para considerar o código correto

[TESTES]
    testes manuais esperados

[SAÍDA]
    produto final esperado
```

---

## 27. Exemplo — calculadora web simples

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        gerar código

    escopo>
        responder com um único arquivo HTML completo

[PROJETO]
    calculadora_web_lmc

[SISTEMA]
    calculadora web simples

[TIPO_DE_SISTEMA]
    aplicação web simples

[OBJETIVO]
    Criar uma calculadora que realize soma, subtração, multiplicação e divisão entre dois números.

[CONTEXTO]
    O sistema será usado como exemplo inicial do módulo LMC-CODE para testar se diferentes IAs conseguem gerar código funcional a partir de uma especificação estruturada.

[PÚBLICO_ALVO]
    usuários iniciantes que desejam executar o sistema diretamente no navegador

[TECNOLOGIAS]
    HTML
    CSS
    JavaScript

[FUNCIONALIDADES]

    funcionalidade>
        nome>
            somar números

        descrição>
            somar dois números informados pelo usuário

        prioridade>
            obrigatória

    funcionalidade>
        nome>
            subtrair números

        descrição>
            subtrair o segundo número do primeiro número

        prioridade>
            obrigatória

    funcionalidade>
        nome>
            multiplicar números

        descrição>
            multiplicar dois números informados pelo usuário

        prioridade>
            obrigatória

    funcionalidade>
        nome>
            dividir números

        descrição>
            dividir o primeiro número pelo segundo número

        prioridade>
            obrigatória

    funcionalidade>
        nome>
            limpar campos

        descrição>
            limpar os campos de entrada e o resultado exibido

        prioridade>
            obrigatória

[INTERFACE]
    titulo>
        Calculadora Simples

    campos>
        número 1
        número 2

    botoes>
        somar
        subtrair
        multiplicar
        dividir
        limpar

    layout>
        centralizado na tela
        visual simples
        campos e botões bem identificados
        responsivo para celular

[ENTRADAS]

    entrada>
        nome>
            número 1

        tipo>
            número

        obrigatório>
            sim

    entrada>
        nome>
            número 2

        tipo>
            número

        obrigatório>
            sim

[PROCESSAMENTO]
    ler os dois números informados
    identificar o botão clicado
    executar a operação correspondente
    exibir o resultado na tela

[REGRAS_DE_NEGOCIO]
    a soma deve adicionar os dois números
    a subtração deve subtrair o segundo número do primeiro
    a multiplicação deve multiplicar os dois números
    a divisão deve dividir o primeiro número pelo segundo
    a divisão por zero não deve ser permitida

[SAÍDAS]
    resultado numérico da operação
    mensagem de erro quando houver entrada inválida
    mensagem de erro quando houver tentativa de divisão por zero

[VALIDAÇÕES]
    verificar se os dois campos foram preenchidos
    verificar se os valores informados são números
    impedir divisão por zero
    limpar mensagens anteriores antes de novo cálculo

[ARQUIVOS]
    arquivo>
        nome>
            index.html

        conteúdo>
            HTML, CSS e JavaScript no mesmo arquivo

[CONTROLE]
    nivel>
        moderado

    saida>
        codigo

    conteudo>
        baseado_no_lmc

    extrapolacao>
        baixa

[RESTRIÇÕES]
    não usar bibliotecas externas
    não separar em múltiplos arquivos
    não criar funcionalidades além das solicitadas
    não usar banco de dados
    não exigir instalação
    não usar framework

[FORMATO_CODIGO]
    código completo
    código comentado de forma simples
    nomes de variáveis claros
    CSS dentro da tag style
    JavaScript dentro da tag script

[CRITÉRIOS_DE_ACEITAÇÃO]
    deve funcionar ao abrir o arquivo no navegador
    deve somar corretamente
    deve subtrair corretamente
    deve multiplicar corretamente
    deve dividir corretamente
    deve impedir divisão por zero
    deve limpar os campos
    deve exibir mensagens claras
    deve estar em um único arquivo HTML

[TESTES]

    teste>
        nome>
            soma

        entrada>
            número 1 = 10
            número 2 = 5
            operação = somar

        resultado_esperado>
            15

    teste>
        nome>
            subtração

        entrada>
            número 1 = 10
            número 2 = 5
            operação = subtrair

        resultado_esperado>
            5

    teste>
        nome>
            multiplicação

        entrada>
            número 1 = 10
            número 2 = 5
            operação = multiplicar

        resultado_esperado>
            50

    teste>
        nome>
            divisão

        entrada>
            número 1 = 10
            número 2 = 5
            operação = dividir

        resultado_esperado>
            2

    teste>
        nome>
            divisão por zero

        entrada>
            número 1 = 10
            número 2 = 0
            operação = dividir

        resultado_esperado>
            exibir mensagem de erro

[EXECUÇÃO]
    copiar o código gerado
    salvar como index.html
    abrir o arquivo no navegador
    testar as operações

[SAÍDA]
    gerar um arquivo HTML completo contendo HTML, CSS e JavaScript no mesmo código
```

---

## 28. Regras de interpretação específicas da LMC-CODE

Ao receber uma instrução LMC-CODE, a IA deve:

1. Identificar o objetivo do sistema antes de gerar código.
2. Ler as tecnologias solicitadas.
3. Respeitar o tipo de sistema.
4. Implementar somente as funcionalidades solicitadas.
5. Considerar a interface descrita pelo usuário.
6. Usar as entradas informadas.
7. Aplicar o processamento definido.
8. Respeitar as regras de negócio.
9. Implementar as validações solicitadas.
10. Gerar as saídas esperadas.
11. Respeitar a estrutura de arquivos definida.
12. Não criar bibliotecas, frameworks ou dependências não solicitadas.
13. Não separar arquivos se o usuário pediu arquivo único.
14. Não criar funcionalidades extras sem autorização.
15. Não omitir instruções básicas de execução quando o público for iniciante.
16. Usar nomes claros para variáveis, funções e arquivos.
17. Gerar código completo, testável e coerente com a solicitação.
18. Informar limitações quando alguma parte não puder ser implementada.
19. Evitar complexidade desnecessária.
20. Priorizar código simples e funcional na versão inicial.

---

## 29. Critérios de qualidade do código gerado

Um código gerado com LMC-CODE deve ser avaliado pelos seguintes critérios:

```txt
aderência ao objetivo
funcionamento básico
respeito às funcionalidades
respeito às tecnologias solicitadas
respeito às restrições
clareza da interface
clareza dos nomes no código
presença de validações
facilidade de execução
ausência de dependências não solicitadas
organização do código
compatibilidade com o público-alvo
```

---

## 30. Relação com outros módulos

A LMC-CODE pode ser combinada com outros módulos da LMC.

Exemplos:

```txt
LMC-CODE + LMC-REQ
    transformar requisitos em sistema

LMC-CODE + LMC-DOC
    gerar documentação técnica do código

LMC-CODE + LMC-TEST
    avaliar se o código gerado respeitou a especificação

LMC-CODE + LMC-AGILE
    transformar histórias de usuário em funcionalidades

LMC-CODE + LMC-PROCESS
    automatizar processos operacionais
```

---

## 31. Limites da LMC-CODE

A LMC-CODE não garante que todo código gerado funcionará perfeitamente na primeira tentativa.

Podem ocorrer problemas como:

```txt
erro de sintaxe
funcionalidade incompleta
diferença entre navegadores
interpretação incorreta da regra
ausência de tratamento de algum caso
uso de solução mais complexa que o necessário
```

Por isso, o código gerado deve ser testado, revisado e ajustado.

A LMC-CODE reduz ambiguidades, mas não elimina a necessidade de validação humana.

---

## 32. Definição acadêmica da LMC-CODE

A LMC-CODE pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada à geração assistida de código por Inteligência Artificial, estruturando sistemas, funcionalidades, interfaces, entradas, regras de negócio, processamento, saídas, validações, arquivos e testes, com o objetivo de reduzir ambiguidades entre a intenção do usuário e a implementação técnica produzida pela IA.

---

## 33. Síntese

A LMC-CODE organiza a criação de código em blocos claros.

Sua função é transformar uma ideia de sistema em uma instrução estruturada para IA, permitindo que o usuário descreva:

```txt
o que quer construir
para quem será usado
quais tecnologias deseja
quais funcionalidades precisa
como a interface deve se comportar
quais dados serão inseridos
quais regras devem ser respeitadas
quais validações são necessárias
como o código deve ser entregue
como testar se funcionou
```

A LMC-CODE não transforma o usuário em programador, mas permite que ele conduza a IA com maior clareza na criação de sistemas, protótipos, páginas e automações.

---

**Fim da especificação LMC-CODE**
