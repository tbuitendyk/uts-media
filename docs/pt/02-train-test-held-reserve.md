# Treino, teste, retido, reserva: por que razão um só trecho separado não basta depois de olharmos para ele

_Um trecho separado só julga bem uma regra até agirmos com base no que ele mostra. Por que razão convém dividir o histórico em quatro partes._

Quem testa uma regra de negociação sobre preços passados aprende depressa a primeira lição. Uma regra ajustada num trecho do histórico fica bem nesse trecho, porque foi moldada para caber nele. Por isso separa-se uma parte do histórico, ajusta-se a regra com o resto e verifica-se o resultado na parte que ela nunca viu. A essa parte costuma dar-se o nome de dados fora da amostra.

A ideia é sólida. Também se desgasta mais depressa do que quase todos esperam, e o desgaste vem de um hábito perfeitamente razoável: olhar para o resultado e depois fazer alguma coisa a respeito.

## Como um trecho separado se gasta

Um exemplo inventado. Procuramos num trecho do histórico e saímos com vinte regras candidatas. Passamos as vinte pelo trecho separado. A maioria vai mal. Três vão bem. Ficamos com as três e anotamos os resultados delas no trecho separado como evidência.

Esses resultados já não estão limpos. O trecho separado devia julgar as regras. Em vez disso, escolheu-as. Ficamos com essas três porque ali se saem bem; é claro que ali se saem bem.

Com moedas, isso fica claro. Entregue uma moeda a vinte pessoas e peça dez lançamentos a cada uma. Fique com as três que tiraram mais caras. As folhas delas impressionam, e impressionariam da mesma maneira se todas as moedas fossem normais, porque a seleção foi feita exatamente por aquilo que agora se admira. Peça às mesmas três que lancem outra vez, e elas voltam a ser comuns.

O mesmo desgaste acontece também de forma mais discreta. O resultado no trecho separado é fraco, por isso voltamos atrás, mudamos um ajuste e verificamos de novo. Um pouco melhor. Mudamos outro. Cada ida e volta é uma pequena escolha feita com a ajuda do trecho separado. Depois de um número suficiente delas, a regra está ajustada ao trecho separado tanto quanto estava ao primeiro. Só demorou mais, e em nenhum passo houve desonestidade.

Daqui sai um princípio fácil de dizer e difícil de cumprir: o histórico que julga uma regra nunca deve ser o histórico que a escolheu. No momento em que um trecho influencia uma escolha, muda de lado. Passa a fazer parte da escolha.

## Quatro partes em vez de duas

Se olhar e escolher gastam histórico, a resposta é decidir de antemão que histórico pode ser gasto e guardar algum que não seja usado para nada. Uma disposição possível divide o histórico em quatro: treino, teste, retido e reserva.

**Treino** e **teste** são as partes de trabalho. É ali que as regras são encontradas, comparadas, retocadas e descartadas. Podem ser vistas quantas vezes for preciso. Espera-se que se gastem, e um bom resultado ali não deve impressionar ninguém.

**Retido** é histórico sobre o qual nenhuma escolha jamais foi feita. É ali que as sobreviventes das duas primeiras partes são julgadas. Como nada foi escolhido nem retocado com ele, um resultado em retido significa algo que um resultado nas partes de trabalho não pode significar.

**Reserva** vem por fim. Existe por causa do problema acima. Depois de ver o resultado em retido, já somos alguém que olhou. Pode surgir a tentação de retocar alguma coisa, ou simplesmente de seguir com as sobreviventes que se saíram melhor em retido, o que é de novo o erro das vinte moedas. Reserva é a leitura feita depois de tudo isso, sobre histórico ainda intacto.

## Manter honesta a última parte

Dividir em quatro só ajuda se a divisão for respeitada. Três hábitos fazem quase todo o trabalho.

Decidir a divisão antes de começar e deixá-la por escrito. Mover os limites depois de ver resultados também é escolher.

Decidir de antemão o que conta como passar. Se uma regra fica aquém em reserva, o resultado honesto é que ficou aquém. A tentação será procurar uma explicação.

Olhar para reserva uma só vez. Olhar, retocar e olhar de novo faz dela mais uma parte de trabalho. E então não sobra nada com que julgar.

Mesmo bem respeitada, a divisão tem um limite. Uma regra que passa em todas as partes passou no passado. Nenhuma disposição de preços antigos substitui os preços que ainda não aconteceram. O que a divisão consegue é mais modesto e ainda assim valioso: impede que uma regra seja avaliada pelo mesmo histórico que a escolheu.

O Ultimate Trading System, o software que construímos, divide o histórico nestas quatro partes, treino, teste, retido e reserva, de modo que o histórico que julga uma regra nunca é o histórico que a escolheu. Os passos Retido e Reserva julgam as sobreviventes em histórico sobre o qual nenhuma escolha jamais foi feita: primeiro retido e, por fim, reserva. O teste gratuito não precisa de conta em nenhuma corretora, porque Construir e Livros em papel funcionam com dados públicos. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
