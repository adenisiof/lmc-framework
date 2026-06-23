# LMC-REQ — Especificação para Levantamento e Organização de Requisitos

**Autor:** Adenísio Pereira de Freitas
**Projeto:** LMC-FRAMEWORK
**Categoria:** módulo de requisitos
**Status:** em desenvolvimento
**Arquivo:** `specs/LMC-REQ.md`

---

## 1. Definição

A **LMC-REQ** é o módulo da **LMC — Linguagem de Marcação Conceitual** voltado ao levantamento, organização, análise e validação de requisitos com apoio de Inteligência Artificial.

Sua função é transformar uma ideia inicial, necessidade, problema ou solicitação em uma estrutura clara de requisitos, permitindo que a IA ajude o usuário a organizar o que o sistema, processo ou projeto precisa fazer.

A LMC-REQ pode ser usada antes da criação de código, antes da documentação técnica, antes da organização de backlog ágil ou antes da modelagem de processos.

Fluxo conceitual:

```txt
Ideia ou problema
↓
LMC-REQ
↓
Requisitos estruturados
↓
Validação humana
↓
LMC-CODE, LMC-AGILE, LMC-DOC ou LMC-PROCESS
```

A LMC-REQ não substitui a análise humana. Ela organiza a intenção do usuário para reduzir ambiguidades antes da execução técnica.

---

## 2. Finalidade da LMC-REQ

A LMC-REQ tem como finalidade estruturar requisitos de forma clara, verificável e reutilizável.

Ela pode ser usada para organizar:

```txt
ideias de sistemas
necessidades de usuários
requisitos funcionais
requisitos não funcionais
regras de negócio
critérios de aceitação
escopo de projeto
fluxos de uso
restrições técnicas
dependências
riscos
premissas
itens fora do escopo
pendências de definição
```

A LMC-REQ ajuda o usuário a explicar para a IA não apenas o que deseja criar, mas também por que, para quem, com quais limites e com quais critérios de validação.

---

## 3. Problema que a LMC-REQ busca resolver

Muitos projetos começam com ideias vagas.

O usuário pode dizer:

```txt
quero um sistema de provas
quero um aplicativo para organizar alunos
quero uma página para cadastrar dados
quero um sistema para gerar relatórios
```

Essas frases indicam uma intenção, mas ainda não definem claramente:

```txt
quem usará o sistema
qual problema será resolvido
quais funcionalidades são obrigatórias
quais dados serão usados
quais regras precisam ser respeitadas
quais limitações existem
como saber se o sistema ficou correto
```

Quando esses elementos não são definidos, a IA pode gerar código, documentos ou planos que parecem bons, mas não atendem totalmente à necessidade real.

A LMC-REQ busca reduzir esse problema organizando a fase de requisitos antes da execução.

---

## 4. Relação com a LMC-CORE

A LMC-REQ herda as regras gerais da **LMC-CORE**, especialmente:

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

A LMC-REQ acrescenta tags específicas para requisitos:

```txt
[PROBLEMA]
[SOLUÇÃO_PROPOSTA]
[STAKEHOLDERS]
[USUÁRIOS]
[ESCOPO]
[FORA_DO_ESCOPO]
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
[DADOS]
[FLUXOS_DE_USO]
[CENÁRIOS]
[PREMISSAS]
[DEPENDÊNCIAS]
[RISCOS]
[PRIORIDADES]
[REQUISITOS_ABERTOS]
[VALIDAÇÃO]
```

---

## 5. Princípios da LMC-REQ

### P1. Problema antes da solução

Antes de definir funcionalidades, é necessário compreender o problema que será resolvido.

### P2. Usuário antes da tecnologia

Antes de escolher tecnologia, é necessário entender quem usará o sistema e para qual finalidade.

### P3. Requisito deve ser claro

Um requisito deve indicar uma necessidade ou comportamento de forma objetiva.

### P4. Requisito deve ser verificável

Deve ser possível avaliar se o requisito foi atendido.

### P5. Escopo deve ser delimitado

A LMC-REQ deve indicar o que faz parte do projeto e o que não faz.

### P6. Regras de negócio devem ser separadas

Regras de negócio não devem ser confundidas com interface ou tecnologia.

### P7. Prioridade deve orientar a execução

Nem todo requisito tem a mesma importância. A LMC-REQ deve permitir indicar o que é obrigatório, desejável ou futuro.

### P8. Pendências devem ficar visíveis

Quando algo ainda não estiver definido, deve ser registrado como requisito aberto ou ponto de dúvida.

### P9. A IA não deve inventar regras críticas

Quando informações essenciais não forem fornecidas, a IA deve apontar lacunas em vez de criar decisões como se fossem definitivas.

### P10. Requisitos alimentam outros módulos

A LMC-REQ pode gerar base para LMC-CODE, LMC-AGILE, LMC-DOC e LMC-PROCESS.

---

## 6. Estrutura mínima da LMC-REQ

A estrutura mínima é:

```txt
[PROBLEMA]
    problema ou necessidade identificada

[OBJETIVO]
    o que o projeto precisa alcançar

[SAÍDA]
    produto esperado
```

Exemplo:

```txt
[PROBLEMA]
    O professor precisa aplicar provas e organizar os resultados dos alunos de forma mais prática.

[OBJETIVO]
    Levantar os requisitos iniciais de um sistema simples de provas escolares.

[SAÍDA]
    gerar lista de requisitos funcionais, não funcionais e regras de negócio.
```

---

## 7. Estrutura recomendada da LMC-REQ

```txt
[PROTOCOLO_DE_USO]
[PROJETO]
[PROBLEMA]
[SOLUÇÃO_PROPOSTA]
[OBJETIVO]
[CONTEXTO]
[STAKEHOLDERS]
[USUÁRIOS]
[ESCOPO]
[FORA_DO_ESCOPO]
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
[DADOS]
[FLUXOS_DE_USO]
[CENÁRIOS]
[PREMISSAS]
[DEPENDÊNCIAS]
[RISCOS]
[PRIORIDADES]
[REQUISITOS_ABERTOS]
[CONTROLE]
[RESTRIÇÕES]
[FORMATO]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

Nem todas as tags precisam ser usadas em toda solicitação. Em projetos simples, a estrutura pode ser reduzida.

---

## 8. [PROBLEMA]

A tag `[PROBLEMA]` descreve a necessidade, dor ou situação que motiva o projeto.

Exemplo:

```txt
[PROBLEMA]
    Professores precisam criar, aplicar e corrigir provas de forma mais organizada, reduzindo retrabalho e facilitando a análise dos resultados por turma.
```

O problema deve ser descrito antes da solução.

---

## 9. [SOLUÇÃO_PROPOSTA]

A tag `[SOLUÇÃO_PROPOSTA]` descreve a ideia inicial de solução.

Exemplo:

```txt
[SOLUÇÃO_PROPOSTA]
    Criar um sistema web simples para cadastrar provas, gerar questões, aplicar atividades e registrar respostas dos alunos.
```

A solução proposta ainda pode ser ajustada após a análise dos requisitos.

---

## 10. [STAKEHOLDERS]

A tag `[STAKEHOLDERS]` identifica pessoas, grupos ou setores interessados no projeto.

Modelo:

```txt
[STAKEHOLDERS]

    stakeholder>
        nome>
            professor

        interesse>
            criar e corrigir provas com menos retrabalho

    stakeholder>
        nome>
            coordenação pedagógica

        interesse>
            acompanhar resultados por turma
```

Stakeholders podem ser usuários diretos ou pessoas impactadas pelo sistema.

---

## 11. [USUÁRIOS]

A tag `[USUÁRIOS]` define quem usará diretamente o sistema ou processo.

Modelo:

```txt
[USUÁRIOS]

    usuário>
        tipo>
            professor

        objetivo>
            criar provas e visualizar resultados

    usuário>
        tipo>
            aluno

        objetivo>
            acessar e responder provas
```

A diferença entre stakeholder e usuário é que o usuário interage diretamente com o sistema.

---

## 12. [ESCOPO]

A tag `[ESCOPO]` define o que faz parte do projeto.

Exemplo:

```txt
[ESCOPO]
    cadastro de turmas
    cadastro de provas
    criação de questões objetivas
    aplicação de prova por chave de acesso
    registro de respostas
    relatório por turma
```

O escopo ajuda a impedir que a IA crie funcionalidades além do necessário.

---

## 13. [FORA_DO_ESCOPO]

A tag `[FORA_DO_ESCOPO]` define o que não será tratado nesta versão.

Exemplo:

```txt
[FORA_DO_ESCOPO]
    aplicativo mobile
    integração com diário oficial
    correção automática de questões discursivas
    login com conta institucional
    pagamento ou assinatura
```

Essa tag é importante para controlar a expansão indevida do projeto.

---

## 14. [REQUISITOS_FUNCIONAIS]

A tag `[REQUISITOS_FUNCIONAIS]` define o que o sistema deve fazer.

Modelo:

```txt
[REQUISITOS_FUNCIONAIS]

    requisito>
        id>
            RF01

        nome>
            cadastrar turma

        descrição>
            o sistema deve permitir que o professor cadastre turmas

        prioridade>
            obrigatória

        critério_de_aceitação>
            o professor consegue criar uma turma informando nome, série e identificação
```

Exemplo compacto:

```txt
[REQUISITOS_FUNCIONAIS]
    RF01 - cadastrar turmas
    RF02 - cadastrar provas
    RF03 - cadastrar questões
    RF04 - permitir resposta dos alunos
    RF05 - gerar relatório de resultados
```

---

## 15. [REQUISITOS_NAO_FUNCIONAIS]

A tag `[REQUISITOS_NAO_FUNCIONAIS]` define qualidades, restrições e características do sistema.

Exemplos:

```txt
[REQUISITOS_NAO_FUNCIONAIS]
    o sistema deve ser simples de usar
    o sistema deve funcionar em navegador
    o sistema deve ter interface responsiva
    o sistema deve evitar dependências complexas
    o sistema deve apresentar mensagens claras de erro
```

Tipos comuns:

```txt
usabilidade
desempenho
segurança
acessibilidade
compatibilidade
manutenibilidade
responsividade
confiabilidade
```

---

## 16. [REGRAS_DE_NEGOCIO]

A tag `[REGRAS_DE_NEGOCIO]` define regras que pertencem ao funcionamento do domínio, independentemente da tecnologia.

Exemplo:

```txt
[REGRAS_DE_NEGOCIO]
    cada aluno deve acessar a prova com uma chave única
    uma prova só pode ser respondida dentro do período definido
    questões objetivas devem ter apenas uma alternativa correta
    o professor pode visualizar os resultados por aluno e por turma
```

Regras de negócio não devem ser confundidas com layout ou código.

---

## 17. [DADOS]

A tag `[DADOS]` define quais informações o sistema precisa armazenar ou manipular.

Modelo:

```txt
[DADOS]

    entidade>
        nome>
            aluno

        campos>
            nome
            número da chamada
            turma
            chave de acesso

    entidade>
        nome>
            prova

        campos>
            título
            componente curricular
            data de início
            data de término
            questões
```

Essa tag ajuda o LMC-CODE a criar estruturas de dados mais coerentes.

---

## 18. [FLUXOS_DE_USO]

A tag `[FLUXOS_DE_USO]` descreve a sequência de ações esperada.

Modelo:

```txt
[FLUXOS_DE_USO]

    fluxo>
        nome>
            professor cria prova

        passos>
            professor acessa o sistema
            cadastra uma prova
            adiciona questões
            define período de aplicação
            gera chaves para alunos

    fluxo>
        nome>
            aluno responde prova

        passos>
            aluno informa nome e chave
            acessa a prova
            responde as questões
            envia as respostas
            recebe confirmação
```

Fluxos ajudam a IA a entender o comportamento do sistema de ponta a ponta.

---

## 19. [CENÁRIOS]

A tag `[CENÁRIOS]` descreve situações de uso.

Modelo:

```txt
[CENÁRIOS]

    cenário>
        nome>
            aluno tenta acessar fora do período

        condição>
            a prova está fora da data permitida

        resultado_esperado>
            o sistema deve bloquear o acesso e exibir mensagem informativa
```

Cenários podem ser usados depois como base para testes.

---

## 20. [PREMISSAS]

A tag `[PREMISSAS]` define condições consideradas verdadeiras para o projeto funcionar.

Exemplo:

```txt
[PREMISSAS]
    o professor será responsável por cadastrar as provas
    os alunos não precisam criar conta
    cada aluno usará uma chave única
    o sistema será acessado pelo navegador
```

Premissas ajudam a limitar decisões do projeto.

---

## 21. [DEPENDÊNCIAS]

A tag `[DEPENDÊNCIAS]` define elementos dos quais o projeto depende.

Exemplo:

```txt
[DEPENDÊNCIAS]
    conexão com internet
    navegador atualizado
    banco de dados para salvar respostas
    definição prévia das turmas
```

Dependências podem ser técnicas, humanas, organizacionais ou de dados.

---

## 22. [RISCOS]

A tag `[RISCOS]` registra problemas possíveis.

Modelo:

```txt
[RISCOS]

    risco>
        descrição>
            alunos compartilharem chaves de acesso

        impacto>
            respostas podem ser associadas incorretamente

        mitigação>
            vincular chave ao nome, número e turma
```

A IA pode sugerir mitigação quando o controle permitir.

---

## 23. [PRIORIDADES]

A tag `[PRIORIDADES]` classifica requisitos por importância.

Modelo:

```txt
[PRIORIDADES]
    obrigatórios>
        cadastro de provas
        resposta dos alunos
        registro de resultados

    desejáveis>
        relatório gráfico
        exportação em PDF

    futuros>
        integração com diário escolar
        banco de questões
```

Essa tag ajuda a planejar versões do projeto.

---

## 24. [REQUISITOS_ABERTOS]

A tag `[REQUISITOS_ABERTOS]` registra pontos ainda indefinidos.

Exemplo:

```txt
[REQUISITOS_ABERTOS]
    definir se haverá login do professor
    definir se os dados serão salvos em banco de dados ou arquivo local
    definir se o aluno verá a nota imediatamente
    definir se questões discursivas serão incluídas na primeira versão
```

A IA não deve tratar requisitos abertos como decisões já tomadas.

---

## 25. [VALIDAÇÃO]

A tag `[VALIDAÇÃO]` define como os requisitos serão confirmados.

Exemplo:

```txt
[VALIDAÇÃO]
    revisar requisitos com o professor
    verificar se todas as funcionalidades obrigatórias estão contempladas
    confirmar regras de negócio antes de gerar código
    transformar requisitos aprovados em tarefas ou histórias de usuário
```

---

## 26. Requisito funcional — modelo completo

```txt
requisito>
    id>
        RF01

    nome>
        cadastrar prova

    descrição>
        o sistema deve permitir que o professor cadastre uma prova com título, componente curricular, turma, período de aplicação e questões

    usuário>
        professor

    prioridade>
        obrigatória

    entradas>
        título
        turma
        componente curricular
        questões
        período de aplicação

    saída>
        prova cadastrada no sistema

    critério_de_aceitação>
        ao preencher os dados obrigatórios, o professor consegue salvar a prova e visualizá-la na lista de provas
```

---

## 27. Requisito não funcional — modelo completo

```txt
requisito>
    id>
        RNF01

    categoria>
        usabilidade

    descrição>
        o sistema deve possuir interface simples e clara para professores e alunos

    prioridade>
        obrigatória

    critério_de_aceitação>
        o usuário consegue identificar facilmente onde cadastrar, responder e visualizar resultados
```

---

## 28. Regra de negócio — modelo completo

```txt
regra>
    id>
        RN01

    nome>
        chave única por aluno

    descrição>
        cada aluno deve receber uma chave única para acessar a prova

    impacto>
        impede que alunos acessem provas de outros estudantes

    critério_de_aceitação>
        o sistema deve validar a chave antes de liberar a prova
```

---

## 29. Níveis de uso da LMC-REQ

### Nível 1 — Ideia inicial

Indicado para transformar uma ideia solta em requisitos básicos.

```txt
[PROBLEMA]
[OBJETIVO]
[SAÍDA]
```

---

### Nível 2 — Requisitos básicos

Indicado para pequenos projetos.

```txt
[PROBLEMA]
[SOLUÇÃO_PROPOSTA]
[USUÁRIOS]
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[SAÍDA]
```

---

### Nível 3 — Requisitos estruturados

Indicado para sistemas e processos com várias partes.

```txt
[PROBLEMA]
[SOLUÇÃO_PROPOSTA]
[STAKEHOLDERS]
[USUÁRIOS]
[ESCOPO]
[FORA_DO_ESCOPO]
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
[DADOS]
[SAÍDA]
```

---

### Nível 4 — Requisitos verificáveis

Indicado para gerar base de implementação.

```txt
[REQUISITOS_FUNCIONAIS]
[REQUISITOS_NAO_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
[FLUXOS_DE_USO]
[CENÁRIOS]
[CRITÉRIOS_DE_ACEITAÇÃO]
[VALIDAÇÃO]
```

---

### Nível 5 — Base para desenvolvimento

Indicado para alimentar LMC-CODE ou LMC-AGILE.

```txt
[ESCOPO]
[REQUISITOS_FUNCIONAIS]
[REGRAS_DE_NEGOCIO]
[DADOS]
[FLUXOS_DE_USO]
[PRIORIDADES]
[CRITÉRIOS_DE_ACEITAÇÃO]
[SAÍDA]
```

---

## 30. Modelo mínimo

```txt
[PROBLEMA]
    problema ou necessidade

[OBJETIVO]
    objetivo da análise de requisitos

[SAÍDA]
    produto esperado
```

---

## 31. Modelo padrão

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        levantar e organizar requisitos

    escopo>
        não gerar código nesta etapa

[PROJETO]
    nome_do_projeto

[PROBLEMA]
    problema identificado

[SOLUÇÃO_PROPOSTA]
    ideia inicial de solução

[OBJETIVO]
    objetivo do projeto ou sistema

[CONTEXTO]
    contexto de uso

[STAKEHOLDERS]
    grupos interessados

[USUÁRIOS]
    usuários diretos

[ESCOPO]
    funcionalidades e partes incluídas

[FORA_DO_ESCOPO]
    itens não incluídos nesta versão

[REQUISITOS_FUNCIONAIS]
    requisitos que descrevem o que o sistema deve fazer

[REQUISITOS_NAO_FUNCIONAIS]
    qualidades e restrições do sistema

[REGRAS_DE_NEGOCIO]
    regras do domínio

[DADOS]
    entidades e informações necessárias

[FLUXOS_DE_USO]
    sequências principais de uso

[CENÁRIOS]
    situações esperadas ou exceções

[PREMISSAS]
    condições consideradas verdadeiras

[DEPENDÊNCIAS]
    elementos necessários para o projeto funcionar

[RISCOS]
    possíveis problemas e mitigação

[PRIORIDADES]
    classificação dos requisitos

[REQUISITOS_ABERTOS]
    dúvidas e decisões pendentes

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
    não inventar regras críticas
    não assumir decisões não informadas como definitivas

[FORMATO]
    organizar em seções claras
    separar requisitos funcionais, não funcionais e regras de negócio

[CRITÉRIOS_DE_ACEITAÇÃO]
    requisitos devem estar claros
    requisitos devem ser verificáveis
    escopo deve estar delimitado
    dúvidas devem ser listadas como requisitos abertos

[SAÍDA]
    gerar especificação inicial de requisitos
```

---

## 32. Exemplo — sistema web de provas escolares

```txt
[PROTOCOLO_DE_USO]
    tipo>
        execução

    ação>
        levantar e organizar requisitos

    escopo>
        não gerar código nesta etapa

[PROJETO]
    sistema_web_provas_escolares

[PROBLEMA]
    Professores precisam criar, aplicar, corrigir e acompanhar provas escolares de forma mais organizada, reduzindo retrabalho e facilitando a análise dos resultados por aluno e por turma.

[SOLUÇÃO_PROPOSTA]
    Criar um sistema web simples para cadastro de turmas, criação de provas, aplicação por chave de acesso e geração de relatórios de desempenho.

[OBJETIVO]
    Organizar os requisitos iniciais de um sistema web de provas escolares.

[CONTEXTO]
    O sistema será usado por professores para criar provas e por alunos para responder atividades sem necessidade de cadastro completo.

[STAKEHOLDERS]

    stakeholder>
        nome>
            professor

        interesse>
            criar provas, acompanhar respostas e obter relatórios

    stakeholder>
        nome>
            aluno

        interesse>
            acessar e responder provas de forma simples

    stakeholder>
        nome>
            coordenação pedagógica

        interesse>
            acompanhar dados gerais de desempenho

[USUÁRIOS]

    usuário>
        tipo>
            professor

        objetivo>
            cadastrar turmas, criar provas, corrigir questões e visualizar resultados

    usuário>
        tipo>
            aluno

        objetivo>
            acessar prova por chave, responder questões e enviar respostas

[ESCOPO]
    cadastro de turmas
    cadastro de provas
    criação de questões objetivas
    criação de questões discursivas
    definição de peso da prova
    geração de chave única por aluno
    aplicação de prova por período
    correção automática de questões objetivas
    correção manual de questões discursivas
    relatório por aluno
    relatório por turma

[FORA_DO_ESCOPO]
    aplicativo mobile
    integração com diário oficial
    pagamento online
    ranking público de alunos
    publicação automática de notas sem validação do professor

[REQUISITOS_FUNCIONAIS]

    requisito>
        id>
            RF01

        nome>
            cadastrar turma

        descrição>
            o professor deve poder cadastrar turmas informando nome, série e identificação

        prioridade>
            obrigatória

        critério_de_aceitação>
            o professor consegue criar, visualizar e selecionar uma turma

    requisito>
        id>
            RF02

        nome>
            criar prova

        descrição>
            o professor deve poder criar uma prova informando título, turma, componente curricular, peso e período de aplicação

        prioridade>
            obrigatória

        critério_de_aceitação>
            a prova criada fica disponível para edição e aplicação

    requisito>
        id>
            RF03

        nome>
            cadastrar questões

        descrição>
            o professor deve poder cadastrar questões objetivas e discursivas

        prioridade>
            obrigatória

        critério_de_aceitação>
            a prova pode conter diferentes tipos de questão

    requisito>
        id>
            RF04

        nome>
            gerar chave de acesso

        descrição>
            o sistema deve gerar uma chave única para cada aluno acessar a prova

        prioridade>
            obrigatória

        critério_de_aceitação>
            cada aluno acessa apenas a prova vinculada à sua chave

    requisito>
        id>
            RF05

        nome>
            responder prova

        descrição>
            o aluno deve poder informar nome, número de chamada, série e chave para acessar e responder a prova

        prioridade>
            obrigatória

        critério_de_aceitação>
            o aluno consegue responder e enviar a prova dentro do período permitido

    requisito>
        id>
            RF06

        nome>
            corrigir questões objetivas

        descrição>
            o sistema deve corrigir automaticamente questões de múltipla escolha com base no gabarito

        prioridade>
            obrigatória

        critério_de_aceitação>
            respostas objetivas são comparadas com o gabarito e recebem pontuação

    requisito>
        id>
            RF07

        nome>
            corrigir questões discursivas

        descrição>
            o professor deve poder corrigir manualmente questões discursivas

        prioridade>
            obrigatória

        critério_de_aceitação>
            o professor consegue atribuir nota às respostas discursivas

    requisito>
        id>
            RF08

        nome>
            gerar relatório

        descrição>
            o sistema deve gerar relatório por aluno e por turma

        prioridade>
            desejável

        critério_de_aceitação>
            o professor consegue visualizar desempenho individual e coletivo

[REQUISITOS_NAO_FUNCIONAIS]
    o sistema deve funcionar em navegador
    a interface deve ser simples para professores e alunos
    o aluno não deve precisar criar conta
    o sistema deve apresentar mensagens claras de erro
    o sistema deve ser responsivo
    os dados devem ser organizados de forma segura
    o sistema deve permitir manutenção futura

[REGRAS_DE_NEGOCIO]
    cada aluno deve possuir uma chave única
    a prova só pode ser acessada dentro do período definido
    questões objetivas devem possuir gabarito
    questões discursivas devem ser corrigidas pelo professor
    o resultado final deve considerar o peso definido para a prova
    o professor deve validar os resultados antes de utilizá-los oficialmente

[DADOS]

    entidade>
        nome>
            turma

        campos>
            id
            nome
            série
            identificação

    entidade>
        nome>
            aluno

        campos>
            nome
            número de chamada
            série
            turma
            chave de acesso

    entidade>
        nome>
            prova

        campos>
            id
            título
            componente curricular
            turma
            peso
            data de início
            data de término

    entidade>
        nome>
            questão

        campos>
            enunciado
            tipo
            alternativas
            gabarito
            pontuação

    entidade>
        nome>
            resposta

        campos>
            aluno
            prova
            questão
            resposta enviada
            pontuação

[FLUXOS_DE_USO]

    fluxo>
        nome>
            professor cria prova

        passos>
            cadastrar turma
            criar prova
            adicionar questões
            definir gabarito
            definir período
            gerar chaves de acesso

    fluxo>
        nome>
            aluno responde prova

        passos>
            informar dados de identificação
            informar chave de acesso
            acessar prova
            responder questões
            enviar prova
            receber confirmação

    fluxo>
        nome>
            professor corrige e analisa

        passos>
            acessar respostas
            verificar correção automática
            corrigir discursivas
            visualizar relatório por aluno
            visualizar relatório por turma

[CENÁRIOS]

    cenário>
        nome>
            chave inválida

        condição>
            aluno informa chave inexistente

        resultado_esperado>
            sistema bloqueia acesso e informa que a chave é inválida

    cenário>
        nome>
            prova fora do período

        condição>
            aluno tenta acessar prova antes ou depois do período permitido

        resultado_esperado>
            sistema bloqueia acesso e informa que a prova não está disponível

    cenário>
        nome>
            questão discursiva

        condição>
            aluno responde questão discursiva

        resultado_esperado>
            resposta fica aguardando correção do professor

[PREMISSAS]
    o professor será responsável por cadastrar provas e turmas
    o aluno não precisará criar conta
    cada aluno usará uma chave individual
    o sistema será acessado pelo navegador

[DEPENDÊNCIAS]
    definição das turmas
    definição das provas
    definição dos tipos de questão
    escolha futura de banco de dados
    escolha futura da tecnologia de autenticação do professor

[RISCOS]

    risco>
        descrição>
            aluno compartilhar chave com outro estudante

        impacto>
            respostas podem ser atribuídas incorretamente

        mitigação>
            vincular chave aos dados do aluno e turma

    risco>
        descrição>
            professor esquecer de definir o período da prova

        impacto>
            alunos podem não conseguir acessar a prova

        mitigação>
            tornar período de aplicação obrigatório

[PRIORIDADES]
    obrigatórios>
        cadastro de turmas
        criação de provas
        geração de chave
        resposta dos alunos
        correção objetiva

    desejáveis>
        relatório por turma
        correção discursiva manual
        exportação dos resultados

    futuros>
        banco de questões
        login institucional
        gráficos de desempenho

[REQUISITOS_ABERTOS]
    definir se haverá login para professor
    definir banco de dados
    definir se o aluno verá nota após envio
    definir se será possível editar prova após publicação
    definir se relatórios poderão ser exportados em PDF

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
    não gerar código nesta etapa
    não escolher tecnologia definitiva sem solicitação
    não inventar regras críticas
    não incluir funcionalidades fora do escopo
    não tratar requisitos abertos como decisões finais

[FORMATO]
    organizar em seções
    usar linguagem clara
    separar requisitos funcionais, não funcionais, regras de negócio, dados, fluxos e pendências

[CRITÉRIOS_DE_ACEITAÇÃO]
    requisitos funcionais devem estar identificados
    regras de negócio devem estar separadas
    dados principais devem estar listados
    escopo e fora do escopo devem estar claros
    dúvidas devem aparecer como requisitos abertos

[SAÍDA]
    gerar especificação inicial de requisitos para o sistema web de provas escolares
```

---

## 33. Regras de interpretação específicas da LMC-REQ

Ao receber uma instrução LMC-REQ, a IA deve:

1. Identificar o problema antes de propor solução.
2. Diferenciar problema, solução, objetivo e escopo.
3. Identificar usuários e stakeholders.
4. Separar requisitos funcionais de requisitos não funcionais.
5. Separar regras de negócio de funcionalidades.
6. Não gerar código se o protocolo for apenas de levantamento de requisitos.
7. Não escolher tecnologias definitivas sem solicitação.
8. Não inventar regras críticas quando houver lacuna.
9. Registrar dúvidas em `[REQUISITOS_ABERTOS]`.
10. Delimitar o que está dentro e fora do escopo.
11. Organizar requisitos com prioridade quando possível.
12. Criar critérios de aceitação verificáveis.
13. Usar linguagem clara para usuários não técnicos.
14. Evitar excesso de termos técnicos quando o público for iniciante.
15. Produzir uma saída que possa alimentar LMC-CODE, LMC-AGILE ou LMC-DOC.
16. Preservar a validação humana antes de transformar requisitos em implementação.

---

## 34. Critérios de qualidade de requisitos

Uma saída gerada com LMC-REQ deve ser avaliada pelos seguintes critérios:

```txt
clareza do problema
coerência da solução proposta
delimitação do escopo
separação entre dentro e fora do escopo
identificação dos usuários
identificação dos stakeholders
clareza dos requisitos funcionais
clareza dos requisitos não funcionais
separação das regras de negócio
presença de critérios de aceitação
identificação de dados principais
identificação de fluxos de uso
registro de riscos
registro de requisitos abertos
utilidade para desenvolvimento futuro
```

---

## 35. Relação com outros módulos

A LMC-REQ pode ser combinada com outros módulos da LMC.

Exemplos:

```txt
LMC-REQ + LMC-CODE
    transformar requisitos em código, sistema ou protótipo

LMC-REQ + LMC-AGILE
    transformar requisitos em épicos, histórias de usuário e backlog

LMC-REQ + LMC-DOC
    gerar documento formal de especificação de requisitos

LMC-REQ + LMC-PROCESS
    transformar necessidades organizacionais em processos estruturados

LMC-REQ + LMC-TEST
    avaliar se a saída da IA respeitou os requisitos definidos

LMC-REQ + LMC-EDU
    levantar requisitos de sistemas educacionais ou materiais pedagógicos
```

---

## 36. Limites da LMC-REQ

A LMC-REQ não garante que todos os requisitos estejam completos na primeira versão.

Ela ajuda a organizar o levantamento, mas ainda depende de validação humana, revisão com usuários e refinamento progressivo.

Requisitos podem mudar durante o projeto. Por isso, a LMC-REQ deve ser entendida como uma ferramenta de estruturação inicial e evolução contínua, não como documento definitivo e imutável.

---

## 37. Definição acadêmica da LMC-REQ

A LMC-REQ pode ser definida como uma especificação modular da Linguagem de Marcação Conceitual voltada ao levantamento e organização de requisitos em interações humano–IA, estruturando problema, solução proposta, stakeholders, usuários, escopo, requisitos funcionais, requisitos não funcionais, regras de negócio, dados, fluxos, cenários, riscos e critérios de aceitação, com o objetivo de reduzir ambiguidades entre a intenção do usuário e a especificação necessária para desenvolvimento, documentação ou planejamento de sistemas e processos.

---

## 38. Síntese

A LMC-REQ organiza ideias de projeto em requisitos claros.

Sua função é ajudar o usuário a comunicar para a IA:

```txt
qual problema precisa ser resolvido
qual solução está sendo imaginada
quem será impactado
quem usará o sistema
o que entra no escopo
o que fica fora do escopo
quais funcionalidades são necessárias
quais regras precisam ser respeitadas
quais dados serão usados
quais fluxos precisam existir
quais dúvidas ainda estão abertas
como validar se o requisito foi atendido
```

A LMC-REQ não cria a solução sozinha. Ela estrutura a intenção humana para que a IA auxilie no desenvolvimento com mais clareza, controle e rastreabilidade.

---

**Fim da especificação LMC-REQ**
