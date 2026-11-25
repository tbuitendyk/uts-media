# Uma palavra para testar uma regra de negociação: o padrão plantado

_Antes de confiar numa busca que diz ter encontrado uma regra, verifique se ela encontra uma que você escondeu de propósito. O que é um padrão plantado e como usá-lo._

Cada verificação desta lista pergunta se uma regra é real. Esta pergunta algo anterior: a busca consegue encontrar uma regra real?

## O que significa

Um padrão plantado é uma regra que você coloca de propósito num mercado inventado. Você constrói preços que seguem um padrão conhecido, misturado com ruído, de modo que sabe a resposta certa antes de começar. Depois roda toda a busca sobre esse mercado, exatamente como faria com histórico real, e vê se ela encontra o que você escondeu.

## Por que importa

Uma busca que nunca falha não prova nada. Se a maquinaria tiver um defeito, pode apontar regras que não existem ou deixar passar regras que existem. Com histórico real não dá para saber qual das duas coisas acontece, porque ninguém conhece a resposta certa. Num mercado inventado, dá. Uma busca que não encontra um padrão que você plantou não merece confiança quando diz ter encontrado um que você não plantou.

## Como usar

Plante um padrão, passe-o pela cadeia real, não por um atalho, e verifique se ele aparece. Depois embaralhe esse mesmo mercado inventado para destruir o padrão, rode de novo e verifique se nada aparece. As duas metades contam: encontrar o padrão mostra que a busca enxerga; não encontrar nada nas cópias embaralhadas mostra que ela não enxerga o que não existe. Repita a verificação sempre que o software mudar.

## Onde entra entre as outras verificações

Vem primeiro, antes de qualquer regra ser julgada: testar o instrumento e só então confiar na leitura. Depois vêm quão bom parece o "nada", o histórico que a regra nunca viu e as formas mais simples de negociar o mesmo trecho.

## Onde usamos isso

O Ultimate Trading System, o software que construímos, planta um padrão conhecido num mercado inventado e o passa pela cadeia real, que precisa encontrá-lo enquanto as versões embaralhadas não dão nada. Cada versão mostra se passou. Não há nenhuma IA em nada do que roda, e as mesmas entradas dão sempre a mesma resposta. O teste gratuito não precisa de conta em nenhuma corretora. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Testar o instrumento primeiro, com mais detalhe: https://telegra.ph/Teste-o-instrumento-antes-de-confiar-na-leitura-plantar-um-padrão-conhecido-11-20

A palavra anterior, a forma mais simples: https://telegra.ph/Uma-palavra-para-testar-uma-regra-de-negociação-a-forma-mais-simples-11-24

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
