# Quão bom parece o "nada"? Por que razão um backtest precisa de uma referência sem informação

_O resultado de um backtest diz pouco até se saber o que obtém, no mesmo histórico, uma regra que não sabe nada. Como construir essa referência._

Um backtest, o teste de uma regra de negociação sobre preços passados, termina num número. A regra percorreu vários anos de histórico e saiu à frente. A reação natural é ficar satisfeito. A reação útil é fazer uma pergunta pouco emocionante: à frente de quê?

Quase todos comparam com zero. Se a regra terminou acima do ponto de partida, é considerada boa. Mas zero é a marca errada, e algumas moedas bastam para mostrar isso.

## Cem pessoas e cem moedas

Imagine cem pessoas numa sala. Cada uma lança uma moeda dez vezes e anota o resultado. Ninguém na sala tem qualquer habilidade para lançar moedas. Mesmo assim, quando as folhas são recolhidas, é quase certo que um punhado delas mostra oito caras ou mais. Ordene as folhas da melhor para a pior, e a primeira parece talento.

Não é talento. É o que o melhor de cem parece quando nada acontece.

Procurar uma regra de negociação funciona da mesma maneira. Nunca se testa uma só regra. Testa-se uma janela de observação mais longa e outra mais curta, um limiar mais apertado e outro mais largo, esta saída e aquela. Cada combinação é mais uma pessoa na sala. Com alguns milhares de tentativas, a melhor delas mostra um resultado vistoso no histórico em que se procurou, saiba ou não saiba alguma coisa sobre preços.

Por isso o número no topo da lista responde à pergunta errada. Diz quanto obteve a melhor de muitas tentativas. Não diz quanto desse resultado a busca teria produzido de qualquer maneira, sem nada por trás.

## Fabricar o "nada" de propósito

A solução é medir isso diretamente. Antes de julgar uma regra, constrói-se uma versão dela que não pode saber nada, e essa versão passa exatamente pelo mesmo processo.

Há algumas maneiras comuns. Uma é trocar os sinais da regra por lançamentos de moeda: o mesmo número de entradas, colocadas ao acaso. Outra é manter os sinais da própria regra, mas embaralhá-los no tempo, de modo que cada um ainda existe, mas já não está ao lado dos preços a que respondia. A terceira é embaralhar os rótulos com que a regra foi ajustada, para que tudo o que ela aprender venha do ruído. A ideia geral tem um nome comum: teste de permutação.

O que têm em comum é que a ligação entre sinal e preço é cortada de propósito, e todo o resto fica igual. O mesmo histórico. Os mesmos custos. A mesma pontuação. E, acima de tudo, a mesma busca: se a execução real testou alguns milhares de ajustes e ficou com o melhor, a execução sem informação testa alguns milhares de ajustes e também fica com o melhor.

Depois, olha-se para o que o "nada" obteve.

## O que a referência diz e o que não diz

Primeiro, o "nada" raramente vale zero. Imagine um mercado inventado que subiu aos poucos durante todo o trecho. Ali, comprar ao acaso termina à frente. Imagine outro que andou de lado, com um custo em cada operação. Quase tudo termina atrás. A referência muda com o histórico, e é por isso mesmo que uma marca fixa como zero engana.

Segundo, embaralhar uma vez não basta. Uma única execução sem informação pode sair alta ou baixa por sorte, como uma única pessoa com a sua moeda. Repetida muitas vezes, dá uma faixa: onde o "nada" costuma cair e até onde às vezes chega. Essa faixa é a verdadeira marca.

Terceiro, muda o que conta como resultado. Uma regra que fica dentro da faixa não mostrou nada, por melhor que o seu número pareça sozinho. Uma regra que fica claramente fora dela mereceu um segundo olhar, e só isso. Passou num teste, num trecho do histórico. O passo seguinte é histórico que ela nunca viu.

Uma referência não diz o que uma regra fará a seguir. Elimina uma maneira de nos enganarmos: confundir a melhor de muitas tentativas com uma descoberta. Vale a pena eliminá-la primeiro, porque é fácil cair nela e barato verificar. Também mantém o esforço honesto: quando se procura com mais afinco, o resultado real sobe, mas o do "nada" sobe também. Ver os dois subir juntos é uma lição de humildade, e é útil.

É uma das coisas que o Ultimate Trading System, o software que construímos, faz por conta própria. Cada execução é repetida com votos que não carregam informação alguma, e assim o quadro mostra quão bom o "nada" parece antes de qualquer coisa ser julgada contra ele. Uma sobrevivente enfrenta depois histórico que nunca viu, medida contra quatro maneiras mais simples de operar o mesmo trecho. O teste gratuito não precisa de conta em nenhuma corretora, porque Construir e Livros em papel funcionam com dados públicos. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
