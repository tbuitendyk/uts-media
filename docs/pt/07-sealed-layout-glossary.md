# Uma palavra para testar uma regra de negociação: a disposição selada (treino, teste, retido, reserva)

_Quatro partes do histórico, cada uma com uma só tarefa, para que o histórico que julga uma regra nunca seja o que a escolheu._

Quando alguém pergunta se uma regra de negociação é real, a pergunta seguinte é sempre: real em qual histórico? Uma disposição selada responde dividindo o histórico em quatro partes antes de testar qualquer coisa, cada uma com uma só tarefa.

## Treino

O histórico com que a busca aprende. As regras são ajustadas aqui, então aqui uma regra sempre parece boa. Nada do que acontece no treino conta como evidência.

## Teste

O histórico usado para escolher entre as regras que a busca produziu. Não é o histórico em que foram ajustadas, mas ainda é histórico em que se tomou uma decisão. Depois de escolher a melhor entre muitas regras no teste, o teste começa a favorecer a vencedora.

## Retido

Histórico separado enquanto todas as decisões eram tomadas. As regras que sobrevivem são julgadas aqui, contra formas mais simples de negociar o mesmo trecho. O retido é a primeira leitura honesta, mas só uma vez: se você muda algo pelo que ele mostrou, o retido também começou a escolher.

## Reserva

Um último trecho, aberto por último, depois de todas as outras decisões. É a parte que continua sem ser vista quando não resta nada para ajustar. Uma regra que se sustenta aqui foi julgada em histórico sobre o qual nenhuma decisão foi tomada.

## Por que "selada"

Porque as partes são fixadas antes de o trabalho começar, e as últimas não são olhadas antes da hora. Divida o histórico em apenas duas partes e olhe a segunda mais de uma vez, e você volta a escolher no histórico que deveria julgar.

## Onde usamos isso

O Ultimate Trading System, o software que construímos, divide o histórico assim na sua disposição selada: treino, teste, retido e reserva. O histórico que julga uma regra nunca é o que a escolheu, e a reserva é vista por último. Cada execução também é repetida com votos que não carregam informação, para mostrar primeiro quão bom parece o "nada". O teste gratuito não precisa de conta em nenhuma corretora. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Por que separar um único trecho não basta, com mais detalhe: https://telegra.ph/Treino-teste-retido-reserva-por-que-razão-um-só-trecho-separado-não-basta-depois-de-olharmos-para-ele-11-20

A palavra anterior, determinístico: https://telegra.ph/Uma-palavra-para-testar-uma-regra-de-negociação-determinístico-11-22

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
