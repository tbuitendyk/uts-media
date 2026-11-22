# Teste o instrumento antes de confiar na leitura: plantar um padrão conhecido

_Antes de acreditar no que um backtest diz sobre preços reais, verifique-o num mercado inventado cuja resposta já se conhece. Como fazer, e para quê._

Um backtest é um instrumento de medida. Entram uma regra e um histórico de preços, e sai uma leitura. Quase toda a preocupação, ao testar, vai para a regra: se está sobreajustada, se o histórico era longo o bastante. Muito menos atenção vai para uma pergunta mais simples. O próprio instrumento funciona?

A pergunta é justa, porque um processo de testes é software, e software tem falhas. O difícil é que o histórico real não consegue responder. Se o processo diz que uma regra é boa, não há outra maneira de saber se a regra é boa ou se o processo está errado. Não conhecemos a resposta certa. É por isso que testamos.

Portanto, antes de confiar nele com preços reais, convém dar-lhe um caso em que a resposta é conhecida.

## Uma balança e um peso conhecido

Ninguém confia numa balança de cozinha só porque ela mostra um número. Põe-se em cima algo de peso conhecido e vê-se se ela concorda. Depois tira-se o peso e verifica-se se marca zero. As duas verificações revelam falhas diferentes. Uma balança presa no zero passa na segunda e falha na primeira. Uma balança que marca peso sem nada em cima falha na segunda.

Um processo de testes pode falhar dessas mesmas duas maneiras. Pode ser cego: há algo real nos dados, e ele não relata nada. Ou pode ver coisas: não há nada nos dados, e ele relata um achado. Na negociação, a segunda falha é a perigosa, porque um achado é o que se esperava, e boas notícias raramente são verificadas duas vezes.

## Plantar um padrão e depois embaralhá-lo

O peso conhecido, para um backtest, é um mercado inventado com um padrão escondido de propósito.

Comece com preços feitos de lançamentos de moeda: a cada hora, sobe ou desce, sem nenhuma ligação entre uma hora e a seguinte. Nenhuma regra consegue encontrar nada ali, porque não há nada para encontrar. Depois plante alguma coisa. Por exemplo: após três subidas seguidas, faça a hora seguinte subir mais vezes do que desce. O padrão foi escolhido por quem montou o teste, que sabe onde ele está e com que força foi posto.

Agora passe esse mercado inventado pelo processo. Não por uma cópia simplificada, nem por um modo especial de teste. Pelo processo real, do princípio ao fim, o mesmo código que mais tarde vai ler o histórico real. Ele deve encontrar o que foi plantado.

Se não encontrar, algo está errado, e este é o lugar barato para descobrir. As causas habituais são pouco interessantes: sinais alinhados com a hora errada, um passo que descarta linhas sem avisar, uma pontuação calculada sobre a coluna errada. Qualquer uma delas pode apagar um padrão real. Com histórico real, a conclusão teria sido simplesmente que ali não havia nada.

Isso é metade do teste. Para a outra metade, tome o mesmo mercado inventado e embaralhe-o, de modo que todas as subidas e descidas continuem lá, mas noutra ordem. O padrão desapareceu. Passe-o pelo mesmo processo. Desta vez, ele deve sair vazio.

Se ainda assim relatar um achado, o processo vê coisas. Uma causa clássica é informação que escapa do futuro: em algum ponto, o cálculo de uma hora pôde olhar para uma hora posterior. Uma fuga assim faz quase qualquer coisa parecer boa, incluindo o ruído. Em termos de laboratório, o mercado com o padrão é o teste que deve dar positivo, e o embaralhado é o teste que deve dar negativo. Só se acredita num resultado quando os dois se comportam como devem.

## O que vale passar

Convém ter claro o que isto prova. Prova que o instrumento consegue ver um padrão do tipo e da força que foi plantado, e que fica calado quando não há nenhum. Não diz nada sobre qualquer regra concreta encontrada em histórico real, nem sobre o que uma regra assim fará a seguir.

Dois detalhes decidem se a verificação significa alguma coisa.

Plantar algo fraco. Um padrão tão ruidoso como uma sirene pode ser encontrado até por um processo meio estragado. Deve ser mais ou menos tão fraco quanto aquilo que se esperaria encontrar em dados reais.

Prender a aprovação ao código que a obteve. Se o processo mudar, a verificação deve ser repetida. Caso contrário, confia-se numa balança que foi desmontada e montada de novo desde a última vez que foi verificada.

No Ultimate Trading System, o software que construímos, o instrumento é testado primeiro. Um padrão conhecido é plantado num mercado inventado e passado pelo processo real, que deve encontrá-lo enquanto versões embaralhadas dele saem vazias. Cada versão mostra se passou. O teste gratuito não precisa de conta em nenhuma corretora, porque Construir e Livros em papel funcionam com dados públicos. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
