# Operar em papel só serve de controle se seguir o mesmo caminho das ordens reais

_Uma execução em papel deveria mostrar o que uma regra de negociação teria feito com dinheiro real. Só consegue se os sinais, as ordens, o tempo e os custos seguirem o mesmo caminho. O que se quebra quando não seguem._

Uma regra de negociação passou no backtest. Antes de pôr dinheiro, ela roda em papel por algumas semanas. Se os resultados em papel parecem os do backtest, a regra passa a operar com dinheiro real. É o plano de quase todo trader cuidadoso, e é um bom plano. Mas ele se apoia numa suposição fácil de quebrar sem perceber: que a execução em papel faz a mesma coisa que a execução real vai fazer.

Na linguagem dos experimentos, operar em papel é um controle. Um controle só funciona quando difere do real numa única coisa. Aqui, essa única diferença deveria ser que nenhum dinheiro se move. Todo o resto, do momento em que chega um preço até o momento em que uma execução é registrada, deveria ser igual.

## Onde o papel e o real se afastam

Muitas montagens em papel são construídas à parte do sistema real, muitas vezes às pressas, e diferem em detalhes pequenos que se somam.

**O sinal é calculado de outro jeito.** O código do backtest é reaproveitado no papel, mas o sistema real tem a sua própria versão, escrita para ser rápida. Uma arredonda um valor e a outra não. Uma usa o fechamento do candle e a outra o último negócio alguns segundos antes. Na maioria dos dias ninguém percebe. Nos dias que importam, as duas discordam.

**O tempo é outro.** No papel, costuma-se decidir com o candle fechado e executar ao preço desse candle. No real, o sistema vê o candle fechar, calcula, envia a ordem e espera. O preço que consegue é o de alguns segundos ou minutos depois. Uma regra que opera movimentos curtos pode perder quase toda a vantagem nesse intervalo, e o papel nunca vai mostrar isso.

**As execuções são imaginadas.** No papel, costuma-se supor que toda ordem é executada inteira e ao preço pedido. Ordens reais são executadas em parte, com atraso ou nunca, e as que falham costumam ser justamente as que teriam ido melhor.

**Os custos ficam de fora ou são chutados.** Corretagem, spread e o custo de manter uma posição de um dia para o outro ficam de fora com facilidade, ou entram uma vez como número redondo e nunca mais são revistos.

**As falhas nunca acontecem.** No papel não há ordem rejeitada, conexão perdida nem reinício no meio de uma operação. No real, há. Como o sistema se comporta depois de cada uma delas faz parte do que a regra vai de fato fazer com dinheiro, e um papel montado por um caminho à parte nunca testa isso.

Cada uma dessas coisas é pequena sozinha. Juntas, significam que o papel mede uma regra um pouco diferente da que vai entrar em operação. E quando depois os dois discordam, ninguém sabe dizer se mudou a regra ou só o encanamento.

## Como fazer do papel um controle honesto

A solução cabe numa frase: papel e real seguem um só caminho. O mesmo código calcula o sinal. O mesmo código monta a ordem. O mesmo relógio decide quando. O mesmo modelo de custos é aplicado. Só no último passo um envia a ordem para um livro simulado e o outro para a corretora. Esse último passo é a única diferença, e por isso é a única coisa a que se pode atribuir uma distância entre papel e real.

Daí saem algumas verificações.

- Registre o que o papel decidiu, quando e a que preço, na mesma forma em que o real registra. Assim os dois podem ser comparados linha a linha, e não só pelos totais.
- Ponha os custos desde o primeiro dia, no nível que você espera pagar, e reveja-os quando já houver execuções reais.
- Não deixe o papel ser mais gentil que o real. Se o real espera o candle fechar e depois envia a ordem, o papel deve esperar e precificar do mesmo jeito.
- Trate um papel que sai melhor que o backtest como um aviso, não como boa notícia. Quase sempre significa que algo no caminho está fácil demais.

Nada disso diz que a regra é boa. Um papel fiel de uma regra ruim continua sendo uma regra ruim. O que ele dá é uma leitura em que se pode confiar: quando papel e real são o mesmo caminho, uma diferença entre eles é uma diferença do mercado, não do seu software.

É assim que funciona Livros em papel no Ultimate Trading System, o software que construímos: uma regra que passou nos testes roda em papel, no mesmo caminho que o dinheiro real toma. As ordens reais começam só quando você as liga, a partir de um motor de negociação em uma máquina que você escolhe. O teste gratuito não precisa de conta em nenhuma corretora, porque Construir e Livros em papel funcionam com dados públicos. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
