──────────────────────────────────────────────────

1. DEFINIÇÃO
   ──────────────────────────────────────────────────

A LMC-DOC é uma especificação da LMC voltada para a geração de documentos por meio de Inteligência Artificial.

Seu objetivo é permitir que o usuário organize a criação de textos, relatórios, artigos, planos de aula, roteiros, atas, resumos e documentos institucionais de forma progressiva, clara e controlada.

A LMC-DOC não tem como finalidade escrever tudo de uma vez. Sua função é organizar o processo de escrita para que a IA siga uma sequência lógica, evitando atropelar etapas, inventar informações ou fugir do objetivo definido pelo usuário.

──────────────────────────────────────────────────
2. OBJETIVO DA LMC-DOC
──────────────────────────────────────────────────

A LMC-DOC tem como objetivo:

* estruturar a criação de documentos;
* reduzir ambiguidades nas instruções dadas à IA;
* separar objetivo, contexto, estrutura, conteúdo e revisão;
* permitir correções por blocos;
* manter o controle do processo nas mãos do usuário;
* facilitar a reutilização de modelos documentais;
* impedir que a IA antecipe etapas não solicitadas.

──────────────────────────────────────────────────
3. PRINCÍPIOS DA LMC-DOC
──────────────────────────────────────────────────

P1. Um objetivo por documento
Cada documento deve ter um objetivo principal claramente definido.

P2. Estrutura antes da redação
Antes de escrever o texto final, a estrutura do documento deve estar definida.

P3. Escrita em blocos
O documento deve ser construído por partes: seção, tópico, parágrafo ou item.

P4. Controle do usuário
A IA deve seguir a estrutura fornecida pelo usuário e não substituir o planejamento humano.

P5. Correção localizada
Erros devem ser corrigidos no bloco em que aparecem, sem reescrever todo o documento desnecessariamente.

P6. Progressão sequencial
A IA deve avançar etapa por etapa, respeitando a ordem definida na LMC.

P7. Inferência limitada
A IA só deve completar lacunas quando isso não contrariar o objetivo, as restrições e o contexto.

P8. Reutilização
Toda estrutura LMC-DOC deve poder ser reaproveitada em outros documentos semelhantes.

──────────────────────────────────────────────────
4. SINTAXE GERAL
──────────────────────────────────────────────────

A LMC-DOC utiliza três níveis de escrita:

1. Tags principais
   São escritas entre colchetes e indicam os blocos maiores do documento.

Exemplo:
[OBJETIVO]
[DOCUMENTO]
[ESTRUTURA]

2. Subtags conceituais
   Organizam partes internas de um bloco.

Exemplo:
seção>
parágrafo>
tópico>
item>

3. Propriedades
   Definem características específicas de uma tag ou subtag.

Exemplo:
titulo>Introdução
tom>científico
tamanho>3 parágrafos

──────────────────────────────────────────────────
5. REGRAS DE ESCRITA
──────────────────────────────────────────────────

R1. Tags principais devem ser escritas em letras maiúsculas.

Exemplo:
[OBJETIVO]

R2. Subtags devem terminar com o símbolo ">".

Exemplo:
seção>
parágrafo>

R3. Propriedades devem seguir o formato:

propriedade>valor

Exemplo:
titulo>Introdução
estilo>científico

R4. A hierarquia deve ser marcada por ordem e indentação.

Exemplo:

seção>
titulo>Introdução
objetivo>apresentar o problema
quantidade_paragrafos>2

R5. Cada bloco deve ter uma função clara dentro do documento.

R6. A IA deve respeitar a ordem dos blocos informados.

R7. A IA não deve criar novas seções quando a estrutura estiver fechada.

R8. A IA pode sugerir melhoria estrutural apenas quando o bloco [DEVOLUTIVA] for solicitado.

──────────────────────────────────────────────────
6. TAGS OBRIGATÓRIAS
──────────────────────────────────────────────────

[DOCUMENTO]

Define o tipo de documento que será produzido.

Exemplos:
artigo científico
plano de aula
relatório
resumo
roteiro
ata
projeto
declaração
parecer

Uso:

[DOCUMENTO]
artigo científico

──────────────────────────────────────────────────

[OBJETIVO]

Define a finalidade principal do documento.

Deve responder:
O que este documento precisa alcançar?

Exemplo:

[OBJETIVO]
Apresentar a LMC como uma linguagem estruturada para melhorar a comunicação entre humanos e Inteligência Artificial.

──────────────────────────────────────────────────

[ESTRUTURA]

Define a organização do documento.

Pode conter seções, tópicos, capítulos, parágrafos ou itens.

Exemplo:

[ESTRUTURA]

seção>
titulo>Introdução
objetivo>apresentar o problema central

seção>
titulo>Desenvolvimento
objetivo>explicar a proposta

seção>
titulo>Conclusão
objetivo>retomar a contribuição do trabalho

──────────────────────────────────────────────────

[SAÍDA]

Define o formato final esperado.

Exemplo:

[SAÍDA]
texto completo
linguagem formal
organizado em parágrafos

──────────────────────────────────────────────────
7. TAGS RECOMENDADAS
──────────────────────────────────────────────────

[BRANCH]

Define o projeto ou linha de trabalho.

Exemplo:

[BRANCH]
artigo_lmc_documentos

──────────────────────────────────────────────────

[MODO]

Define como a IA deve atuar.

Valores sugeridos:

estudo
desenvolvimento
revisão
documento
científico
didático
institucional
acadêmico

Exemplo:

[MODO]
documento | científico

──────────────────────────────────────────────────

[ESTILO]

Define o tom da escrita.

Valores sugeridos:

técnico
científico
didático
formal
conversacional
institucional
argumentativo
descritivo

Exemplo:

[ESTILO]
científico

──────────────────────────────────────────────────

[CONTEXTO]

Apresenta a situação que motivou o documento.

Exemplo:

[CONTEXTO]
O documento será usado como base para um artigo sobre a LMC e sua aplicação na comunicação humano-IA.

──────────────────────────────────────────────────

[PÚBLICO_ALVO]

Define para quem o documento será escrito.

Exemplo:

[PÚBLICO_ALVO]
professores, pesquisadores e estudantes de tecnologia

──────────────────────────────────────────────────

[DESCRIÇÃO]

Detalha o que deve ser abordado.

Exemplo:

[DESCRIÇÃO]
Explicar que a linguagem natural pode gerar ambiguidades e que a LMC organiza as instruções em blocos semânticos.

──────────────────────────────────────────────────

[RESTRIÇÕES]

Define limites que a IA deve respeitar.

Exemplo:

[RESTRIÇÕES]
não criar conceitos ainda não definidos
não avançar para programação
não escrever o artigo final nesta etapa
não usar linguagem excessivamente informal

──────────────────────────────────────────────────

[FORMATO]

Define forma, tamanho, organização e apresentação.

Exemplo:

[FORMATO]
parágrafos curtos
linguagem acadêmica
sem tópicos numerados
entre 1200 e 1500 caracteres

──────────────────────────────────────────────────

[BASE_DE_REFERÊNCIA]

Define materiais, textos, arquivos ou ideias que devem orientar a produção.

Exemplo:

[BASE_DE_REFERÊNCIA]
usar a definição de LMC já construída neste projeto
usar o modelo de parágrafos do TCC como referência estrutural

──────────────────────────────────────────────────
8. TAGS DE BLOCO TEXTUAL
──────────────────────────────────────────────────

[SEÇÃO]

Define uma parte maior do documento.

Modelo:

[SEÇÃO]

titulo>
objetivo>
descrição>
restrições>
saída_esperada>

Exemplo:

[SEÇÃO]

titulo>Introdução
objetivo>apresentar o problema da comunicação humano-IA
descrição>explicar que a linguagem humana possui ambiguidades, lacunas e redundâncias
saída_esperada>parágrafo introdutório científico

──────────────────────────────────────────────────

[PARÁGRAFO]

Define um parágrafo específico.

Modelo:

[PARÁGRAFO]

objetivo>
descrição>
elementos_obrigatórios>
restrições>
parágrafo_ajustado>

Exemplo:

[PARÁGRAFO]

objetivo>apresentar o problema
descrição>mostrar que a comunicação humana pode gerar ruídos na interação com sistemas de IA
elementos_obrigatórios>ambiguidade, redundância, inferência da IA
restrições>não concluir ainda
parágrafo_ajustado>texto final do parágrafo

──────────────────────────────────────────────────

[TÓPICO]

Define um item dentro de uma seção.

Modelo:

[TÓPICO]

nome>
objetivo>
conteúdo>
ordem>

Exemplo:

[TÓPICO]

nome>Ambiguidade
objetivo>explicar o problema da interpretação aberta
conteúdo>mostrar que uma mesma instrução pode gerar respostas diferentes
ordem>1

──────────────────────────────────────────────────

[ITEM]

Define elemento simples em lista, checklist ou enumeração.

Modelo:

[ITEM]

nome>
descrição>
status>

Exemplo:

[ITEM]

nome>Definir objetivo do documento
descrição>identificar a finalidade principal antes da escrita
status>concluído

──────────────────────────────────────────────────
9. TAGS DE CONTROLE
──────────────────────────────────────────────────

[ETAPA]

Define em qual fase do processo o documento está.

Valores sugeridos:

planejamento
estruturação
redação
revisão
consolidação
finalização

Exemplo:

[ETAPA]
estruturação

──────────────────────────────────────────────────

[CHECKLIST]

Controla o que já foi feito e o que falta.

Exemplo:

[CHECKLIST]

feito>definição do objetivo
feito>definição da estrutura
falta>redação da introdução
falta>revisão final

──────────────────────────────────────────────────

[DEVOLUTIVA]

Solicita análise da IA sobre o bloco produzido.

A IA deve analisar sem avançar para a próxima etapa.

Exemplo:

[DEVOLUTIVA]
avaliar clareza, coerência e aderência ao objetivo

──────────────────────────────────────────────────

[REVISÃO]

Define o tipo de revisão esperada.

Valores sugeridos:

ortográfica
gramatical
científica
estrutural
argumentativa
coerência
clareza
adequação ao público

Exemplo:

[REVISÃO]
corrigir clareza e coerência sem alterar o sentido original

──────────────────────────────────────────────────

[CONSOLIDAÇÃO]

Solicita união dos blocos já aprovados.

Exemplo:

[CONSOLIDAÇÃO]
unir os parágrafos aprovados em uma seção única

──────────────────────────────────────────────────
10. ORDEM PADRÃO PARA CRIAÇÃO DE DOCUMENTOS
──────────────────────────────────────────────────

A ordem recomendada da LMC-DOC é:

1. [BRANCH]
2. [DOCUMENTO]
3. [OBJETIVO]
4. [CONTEXTO]
5. [PÚBLICO_ALVO]
6. [MODO]
7. [ESTILO]
8. [ESTRUTURA]
9. [SEÇÃO] ou [PARÁGRAFO]
10. [RESTRIÇÕES]
11. [FORMATO]
12. [SAÍDA]
13. [DEVOLUTIVA]
14. [REVISÃO]
15. [CONSOLIDAÇÃO]

Nem todas as tags precisam aparecer em todo documento. Porém, [DOCUMENTO], [OBJETIVO], [ESTRUTURA] e [SAÍDA] são recomendadas como base mínima.

──────────────────────────────────────────────────
11. MODELO MÍNIMO
──────────────────────────────────────────────────

[DOCUMENTO]
tipo do documento

[OBJETIVO]
finalidade principal

[ESTRUTURA]
partes do documento

[SAÍDA]
formato esperado

──────────────────────────────────────────────────
12. MODELO PADRÃO
──────────────────────────────────────────────────

[BRANCH]
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
forma de atuação da IA

[ESTILO]
tom da escrita

[ESTRUTURA]

seção>
titulo>
objetivo>
descrição>

seção>
titulo>
objetivo>
descrição>

[RESTRIÇÕES]
limites que a IA deve respeitar

[FORMATO]
forma final desejada

[SAÍDA]
produto final esperado

──────────────────────────────────────────────────
13. MODELO DE PARÁGRAFO CONTROLADO
──────────────────────────────────────────────────

[PARÁGRAFO]

[OBJETIVO]
Definir a função do parágrafo.

[DESCRIÇÃO]
Indicar as ideias que devem aparecer no parágrafo.

[ELEMENTOS_OBRIGATÓRIOS]
Listar conceitos, termos ou argumentos que precisam aparecer.

[RESTRIÇÕES]
Indicar o que o parágrafo não deve fazer.

[PARÁGRAFO_AJUSTADO]
Espaço para a versão final do parágrafo.

──────────────────────────────────────────────────
14. EXEMPLO DE USO — PLANO DE AULA
──────────────────────────────────────────────────

[BRANCH]
plano_de_aula_matematica

[DOCUMENTO]
plano de aula

[OBJETIVO]
Criar plano de aula sobre logaritmos para estudantes do Ensino Médio.

[CONTEXTO]
Os alunos apresentam dificuldades em potenciação, interpretação de problemas e compreensão do uso dos logaritmos.

[PÚBLICO_ALVO]
estudantes da 2ª série do Ensino Médio

[MODO]
documento | educacional

[ESTILO]
didático | formal

[ESTRUTURA]

seção>
titulo>Aprendizagem essencial
objetivo>indicar o que o aluno deve aprender

seção>
titulo>Objetivos da aula
objetivo>definir as metas de aprendizagem

seção>
titulo>Desenvolvimento
objetivo>descrever a sequência didática

seção>
titulo>Avaliação
objetivo>indicar como verificar a aprendizagem

[RESTRIÇÕES]
não criar habilidades não informadas
não usar linguagem excessivamente técnica
não fugir do conteúdo de logaritmos

[SAÍDA]
plano de aula completo e organizado

──────────────────────────────────────────────────
15. EXEMPLO DE USO — ARTIGO CIENTÍFICO
──────────────────────────────────────────────────

[BRANCH]
artigo_lmc

[DOCUMENTO]
artigo científico

[OBJETIVO]
Apresentar a LMC como uma ferramenta de estruturação da comunicação entre humanos e sistemas de IA.

[CONTEXTO]
A linguagem natural possui ambiguidades, redundâncias e lacunas que podem gerar respostas diferentes entre sistemas de IA.

[PÚBLICO_ALVO]
pesquisadores, professores e profissionais de tecnologia

[MODO]
documento | científico

[ESTILO]
técnico | acadêmico

[ESTRUTURA]

seção>
titulo>Introdução
objetivo>apresentar o problema e justificar a pesquisa

seção>
titulo>Fundamentação teórica
objetivo>relacionar LMC com linguagem, IA e estruturação de instruções

seção>
titulo>Metodologia
objetivo>explicar como a LMC será analisada ou aplicada

seção>
titulo>Discussão
objetivo>interpretar os resultados ou possibilidades da LMC

seção>
titulo>Conclusão
objetivo>apresentar contribuições, limites e trabalhos futuros

[RESTRIÇÕES]
não escrever o artigo completo nesta etapa
não avançar para experimentos
não criar referências bibliográficas fictícias

[SAÍDA]
estrutura do artigo organizada em LMC

──────────────────────────────────────────────────
16. REGRAS DE INTERPRETAÇÃO PARA A IA
──────────────────────────────────────────────────

A IA deve:

1. Identificar o tipo de documento em [DOCUMENTO].
2. Ler o [OBJETIVO] antes de qualquer geração textual.
3. Usar o [CONTEXTO] para limitar a interpretação.
4. Respeitar a ordem definida em [ESTRUTURA].
5. Produzir apenas o que foi solicitado em [SAÍDA].
6. Não antecipar etapas futuras.
7. Não criar seções adicionais sem autorização.
8. Não alterar o objetivo original sem solicitação.
9. Usar [RESTRIÇÕES] como prioridade máxima.
10. Quando houver dúvida, declarar a inferência feita.
11. Quando houver [DEVOLUTIVA], analisar sem reescrever.
12. Quando houver [REVISÃO], corrigir sem mudar a intenção do usuário.
13. Quando houver [CONSOLIDAÇÃO], unir apenas blocos já aprovados.
14. Manter a progressão sequencial do trabalho.

──────────────────────────────────────────────────
17. NÍVEIS DE USO DA LMC-DOC
──────────────────────────────────────────────────

Nível 1 — Básico

Usa apenas:
[DOCUMENTO]
[OBJETIVO]
[SAÍDA]

Indicado para documentos simples.

──────────────────────────────────────────────────

Nível 2 — Estruturado

Usa:
[DOCUMENTO]
[OBJETIVO]
[CONTEXTO]
[ESTRUTURA]
[RESTRIÇÕES]
[SAÍDA]

Indicado para planos de aula, relatórios e artigos.

──────────────────────────────────────────────────

Nível 3 — Controlado

Usa:
[PARÁGRAFO]
[OBJETIVO]
[DESCRIÇÃO]
[ELEMENTOS_OBRIGATÓRIOS]
[RESTRIÇÕES]
[PARÁGRAFO_AJUSTADO]

Indicado para construção progressiva de textos longos.

──────────────────────────────────────────────────

Nível 4 — Revisão e Consolidação

Usa:
[DEVOLUTIVA]
[REVISÃO]
[CHECKLIST]
[CONSOLIDAÇÃO]

Indicado para finalizar documentos com maior controle.

──────────────────────────────────────────────────
18. DEFINIÇÃO ACADÊMICA DA LMC-DOC
──────────────────────────────────────────────────

A LMC-DOC pode ser definida como uma especificação da Linguagem de Marcação Conceitual voltada à produção documental assistida por Inteligência Artificial, estruturando objetivos, contexto, seções, parágrafos, restrições e formatos de saída com o propósito de reduzir ambiguidades, controlar a progressão textual e preservar a intenção do usuário durante o processo de escrita.
