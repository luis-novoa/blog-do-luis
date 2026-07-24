+++
title = 'Adoção de IA nas empresas: por que a maioria trava no piloto'
date = 2026-07-24T15:44:10-04:00
draft = false
description = 'A maioria das empresas roda um piloto de IA, aprova todo mundo, e nunca sai dali. Por que isso acontece e o que separa quem sai do piloto de quem fica preso nele.'
tags = ['ia', 'engenharia', 'produtividade']
+++

A maioria das empresas que eu converso já rodou pelo menos um piloto de IA. Poucas
conseguiram tirar valor real disso de forma consistente. O padrão se repete tanto que
dá pra descrever sem saber o setor: alguém compra acesso a um modelo, um time monta uma
prova de conceito em duas semanas, todo mundo aplaude na demo — e seis meses depois
ninguém mais usa aquilo, ou usa de um jeito tão manual que o ganho desapareceu.

Isso não é falta de tecnologia. Os modelos atuais são bons o suficiente pra boa parte
dos casos de uso que as empresas tentam resolver. O que trava é outra coisa.

## O piloto testa a coisa errada

Um piloto normalmente responde uma pergunta: "o modelo consegue fazer isso?". É a
pergunta errada. A pergunta que decide se a adoção emplaca é: "esse fluxo, com IA no
meio, funciona melhor do que o fluxo atual, de ponta a ponta, com gente de verdade
usando ele todo dia?".

São perguntas diferentes porque a segunda inclui coisas que o piloto costuma deixar de
fora: quem revisa a saída do modelo, o que acontece quando ele erra, como isso se
integra no sistema que já existe, e se a pessoa que vai usar aquilo no dia a dia
confia o suficiente pra não voltar a fazer tudo na mão "só por garantia".

## Três padrões de falha que se repetem

**1. Não existe dono do fluxo.** O time de dados entrega um modelo, o time de produto
entrega uma interface, e ninguém é responsável pelo resultado fim a fim. Quando algo
sai errado, é "problema do modelo" — e ninguém tem mandato pra mudar o processo ao
redor dele.

**2. A revisão humana vira gargalo maior que o problema original.** Um caso clássico:
IA gera um rascunho, mas cada rascunho ainda precisa de 90% da revisão que o trabalho
manual exigia, só que agora com uma etapa extra no meio. O ganho de tempo existe no
papel, mas some na prática porque a confiança na saída é baixa e ninguém quer ser
responsabilizado por deixar passar um erro.

**3. O caso de uso foi escolhido pela visibilidade, não pelo encaixe.** Times escolhem
o projeto de IA mais fácil de mostrar num slide, não o que tem o melhor encaixe entre
"o modelo é bom nisso" e "isso dói de verdade no dia a dia de alguém". Dá uma demo
ótima e uma adoção péssima.

## O que separa quem sai do piloto

As empresas que conseguem tirar valor real têm três coisas em comum, nessa ordem de
importância:

- **Escopo estreito e verificável.** Elas escolhem um problema onde dá pra checar se a
  saída do modelo está certa de forma barata — automaticamente, ou com uma revisão
  humana rápida de verdade, não uma reescrita disfarçada de revisão.
- **Alguém dono do resultado, não da ferramenta.** Existe uma pessoa cujo trabalho
  melhora ou piora dependendo de o fluxo funcionar, e essa pessoa tem autoridade pra
  ajustar o processo, não só o prompt.
- **Medição do que importa, não do que é fácil de medir.** "Quantos tickets a IA
  respondeu" é fácil de medir e quase sempre engana. "Quantos tickets foram resolvidos
  sem precisar de retrabalho humano depois" é mais difícil de medir e é a métrica que
  importa.

## Um jeito prático de começar

Se eu tivesse que resumir em um conselho: não pergunte "onde podemos usar IA". Pergunte
"qual tarefa específica, feita hoje por uma pessoa, tem um resultado fácil de checar e
está doendo o suficiente pra alguém querer ser dono dela". Comece por aí, meça o que
realmente importa, e só depois pense em escalar pra outros times.

Esse é o primeiro post do blog. A ideia aqui é escrever sobre o que estou construindo e
aprendendo — vai ter mais post técnico, mas também vai ter espaço pra qualquer outra
coisa que valha a pena registrar.
