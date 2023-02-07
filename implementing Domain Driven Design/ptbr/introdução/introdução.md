# Introdução

## Big-Picture

O pilar do DDD é a Linguagem ubíqua, não importa a forma que seu software é desenhado, você vai querer que ele reflita uma linguagem ubíqua nos contextos delimitados.

## Modelo estratégico

Um contexto delimitado é onde um modelo de domínio é aplicado e provê um contexto para esta linguagem, falada pelo time

## Contexto de mapeamento

Contexto de mapeamentos mostram as relações entre contextos delimitados

## Arquitetura

Os contextos delimitados geralmente interagem com contextos de mapeamento, mas é importante dizer que não podemos contaminar o domínio com qualquer arquitetura, nosso domínio deve ser o mais puro possível.

Um ótimo modelo de arquitetura para contextos delimitados é a arquitetura exagonal (porta e adaptadores), lembre-se arquitetura é importante, mas o crucial para o negócio é o domínio.

## Modelagem tática

Modelamos nosso modelo tático dentro dos contextos delimitados, um dos padrões mais importantes é o aggregado, esse aggregado é construído por uma simples entidade ou mesmo um agrupamento de entidades e/ou objetos de valores

## Serviços de domínio

Esses serviços de domínio tem a responsabilidade de se envolver com múltiplas entidades executando operações.

## Eventos de domínio

Podemos utilizar e modelar eventos de domínio para ações significativas em nosso domínio.

## A verdade

A verdade é que isso é apenas uma primeira pincelada sobre o DDD e não como cobrir o assunto todo aqui
