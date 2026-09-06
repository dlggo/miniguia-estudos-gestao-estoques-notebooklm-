# Engenharia de Prompts

Este arquivo registra os prompts utilizados durante a construção do estudo no NotebookLM, seus objetivos, resultados e os aprendizados obtidos durante o processo.

## Prompt 1 — Exploração inicial

### Objetivo

Obter uma primeira visão sobre os conceitos fundamentais de gestão de estoques e almoxarifado a partir das fontes selecionadas.

### Prompt utilizado

> Analise as fontes disponíveis e explique o que é gestão de estoques e qual é a função de um almoxarifado.

### Resultado

O NotebookLM apresentou uma explicação geral sobre gestão de estoques e almoxarifado. Entre os conceitos mencionados estavam estoque mínimo/de segurança, ponto de pedido, estoque máximo, curva ABC e métodos de avaliação como PEPS, UEPS e média ponderada móvel.

### Aprendizado

A resposta foi útil para obter uma visão inicial, mas apresentou muitos conceitos simultaneamente e não diferenciou suficientemente os conceitos nem indicou de forma clara a origem de cada informação.

**Conclusão:** o prompt era adequado para exploração, mas precisava ser mais específico para uma análise aprofundada.

---

## Prompt 2 — Estruturação e comparação

### Objetivo

Aprofundar três parâmetros de ressuprimento e obrigar o NotebookLM a organizar a resposta por critérios definidos.

### Prompt utilizado

> Analise as 5 fontes deste notebook e explique, de forma didática e organizada, a diferença entre estoque mínimo (ou de segurança), ponto de pedido e estoque máximo. Para cada conceito, apresente: 1) definição; 2) finalidade; 3) como ele é utilizado na gestão de estoques; 4) relação com os outros dois conceitos; 5) exemplo prático aplicado a um almoxarifado. Utilize somente informações sustentadas pelas fontes e indique as fontes utilizadas em cada conceito. Ao final, faça uma tabela comparativa.

### Resultado

O NotebookLM apresentou definições, finalidades, relações entre os conceitos, fórmulas e exemplos práticos para estoque mínimo, ponto de pedido e estoque máximo.

Também apresentou fórmulas como:

- Estoque mínimo: `Em = c × f`
- Ponto de pedido: `Pp = (c × T) + Em`
- Estoque máximo: `EM = Em + Q`

### Problema identificado

Apesar da resposta ser mais organizada, surgiu uma questão terminológica: o NotebookLM tratou "estoque morto" como relacionado ao estoque mínimo/de segurança.

Também foi necessário verificar se as fórmulas e exemplos estavam realmente sustentados pelas fontes ou se eram simplificações da resposta.

**Conclusão:** a estrutura melhorou significativamente, mas a resposta precisava passar por uma etapa de verificação crítica.

---

## Prompt 3 — Verificação crítica

### Objetivo

Verificar a confiabilidade da resposta anterior e identificar afirmações que poderiam estar incorretas, simplificadas ou dependentes do contexto de determinada fonte.

### Prompt utilizado

> Faça uma revisão crítica da resposta anterior. Para cada uma das três definições — estoque mínimo/de segurança, ponto de pedido e estoque máximo — identifique quais afirmações estão diretamente sustentadas pelas fontes e quais são interpretações, simplificações ou informações que precisam de confirmação. Verifique especialmente as fórmulas apresentadas, a relação entre os três conceitos e o uso dos termos “estoque mínimo”, “estoque de segurança” e “estoque morto”. Não acrescente informações externas às fontes. Apresente o resultado em uma tabela com as colunas: Afirmação | Está sustentada pelas fontes? | Fonte | Observação/correção necessária.

### Resultado

A revisão confirmou que as principais definições e fórmulas estavam sustentadas pelas fontes.

Entretanto, foi identificada uma divergência importante em relação ao termo **"estoque morto"**. Uma fonte utiliza o termo em uma determinada perspectiva, enquanto outra utiliza "estoque morto" para se referir a material obsoleto, roubado ou deteriorado.

Também foram identificadas diferenças terminológicas entre **Tempo de Reposição (TR)** e **Tempo de Aquisição (T)**.

###  Cicatriz identificada

**Problema:** uma resposta inicialmente apresentada como correta poderia induzir a uma equivalência inadequada entre "estoque morto" e estoque de segurança.

**Diagnóstico:** as próprias fontes utilizavam o termo de maneiras diferentes.

**Correção:** o termo "estoque morto" não deve ser apresentado como sinônimo universal de estoque de segurança. Seu significado precisa ser contextualizado de acordo com a fonte utilizada.

### Aprendizado

A revisão crítica mostrou que uma resposta de IA não deve ser aceita automaticamente. Mesmo quando a resposta parece correta, é necessário confrontá-la com as fontes e investigar divergências terminológicas.

---

## Prompt 4 — Síntese comparativa

### Objetivo

Separar os conceitos que apresentam convergência entre as fontes das diferenças específicas de terminologia, fórmulas e abordagens.

### Prompt utilizado

> Com base exclusivamente nas 5 fontes deste notebook, faça uma síntese comparativa sobre estoque mínimo/de segurança, ponto de pedido e estoque máximo.
>
> Para cada conceito:
>
> 1. apresente a definição que aparece de forma mais consistente entre as fontes;
> 2. indique quais termos diferentes são utilizados pelas fontes para representar o mesmo conceito;
> 3. destaque divergências ou diferenças de abordagem entre os autores/documentos;
> 4. informe quando uma fórmula ou procedimento pertence especificamente à Instrução Normativa nº 205/1988 ou a outra fonte, evitando apresentá-lo como regra universal;
> 5. explique quais conceitos podem ser considerados consenso entre as fontes.
>
> Não utilize informações externas ao notebook.
>
> Ao final, produza uma tabela com:
> Conceito | Definição consensual | Termos alternativos | Divergências entre fontes | Fonte(s) que sustentam.

### Resultado

A síntese apresentou uma definição comparativa dos três parâmetros e identificou:

- convergência entre as fontes sobre a função do estoque mínimo;
- forte concordância sobre o ponto de pedido;
- diferentes formas de apresentar o estoque máximo;
- diferenças terminológicas entre autores e documentos;
- necessidade de contextualizar determinadas fórmulas, especialmente quando provenientes da IN nº 205/1988;
- conflito no uso do termo "estoque morto".

### Aprendizado

O quarto prompt transformou as respostas anteriores em uma síntese mais adequada para estudo. Em vez de buscar somente uma resposta pronta, o processo passou a comparar fontes, identificar divergências e distinguir conceitos gerais de procedimentos específicos de determinada referência.

---

## Evolução dos prompts

O processo apresentou uma evolução progressiva:

**Explorar → Estruturar → Verificar → Sintetizar**

Essa sequência foi utilizada para transformar uma resposta inicial genérica em um material de estudo mais crítico e fundamentado nas fontes selecionadas.

### Principal aprendizado

O uso do NotebookLM foi mais produtivo quando os prompts:

- definiram claramente o objetivo;
- limitaram a resposta às fontes disponíveis;
- solicitaram comparação entre documentos;
- exigiram identificação das fontes;
- pediram revisão crítica;
- distinguiram consenso de divergência;
- evitaram tratar uma fórmula específica como regra universal.

O processo também mostrou que **engenharia de prompts não significa apenas escrever perguntas mais longas**, mas criar uma sequência de instruções que permita explorar, testar, verificar e aprimorar o conhecimento produzido.
