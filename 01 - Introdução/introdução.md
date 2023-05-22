# Introdução Resumida

Muito se tem falado de DDD e venho trabalhando em alguns projetos que ensaiam algo similar, eu venho fazendo minhas anotações e vejo que isso é poderoso, além disso, venho estudando pelo livro do Vernon.

## Minha primeira conclusão sobre o assunto é:

Trabalhe no coração do sotware e para o negócio. Framework x, Data ORMs y são meras ferramentas que te ajudam a salvar dados e fazem outras coisas.

Ferramentas são detalhes que ajudam o negócio a atingir seus resultados e que geralmente se guiam em cima de receitas prontas.

DDD leva programadores e equipe para outro patamar.

## Big-Picture, a Base de tudo

O pilar do DDD é a Linguagem ubíqua, não importa a forma que seu software é desenhado, você vai querer que ele reflita uma linguagem ubíqua nos contextos delimitados.

## Modelo estratégico

Um contexto delimitado é onde um modelo de domínio é aplicado e provê um contexto para esta linguagem, falada pelo time.

## Contexto de mapeamento

Contexto de mapeamentos mostram as relações entre contextos delimitados

## Arquitetura

Os contextos delimitados geralmente interagem com contextos de mapeamento, mas é importante dizer que não podemos contaminar o domínio com qualquer arquitetura, nosso domínio deve ser o mais puro possível, geralmente nesse ponto o melhor é ter o domínio puro com apenas a linguagem de programação.

## Arquitetura recomendada

Um ótimo modelo de arquitetura para contextos delimitados é a arquitetura Exagonal (porta e adaptadores), lembre-se arquitetura é importante, mas o crucial para o negócio é o domínio.

## Modelagem tática

Modelamos nosso modelo tático dentro dos contextos delimitados, um dos padrões mais importantes é o aggregado, esse aggregado é construído por uma simples entidade ou mesmo um agrupamento de entidades e/ou objetos de valores ou mesmo entidades e objetos de valores juntas, geralmente temos mais de uma entidade e/ou mais de um objeto de valor, nesse ponto é bom lembrar que os objetos de valor são imutáveis, não possuem identificador(ID) e dependem de uma entidade, ou seja, eles existem para servir entidades.

## Serviços de domínio - Services

Esses serviços de domínio tem a responsabilidade de se envolver com múltiplas entidades executando operações - em estudo...

## Eventos de domínio

Podemos utilizar e modelar eventos de domínio para ações significativas em nosso domínio - em estudo ...

## O que Temos?

A verdade é que isso é apenas uma primeira pincelada sobre o DDD e apenas um norte sobre o assunto
