# Uma palavra para testar uma regra de negociação: determinístico

_O que significa uma pesquisa de negociação dar a mesma resposta para as mesmas entradas, por que isso importa e como verificar as suas próprias ferramentas._

Há mais uma palavra que aparece sempre que alguém pergunta se uma regra de negociação é real: determinístico. Aqui está ela em linguagem simples.

## O que significa

Um teste é determinístico quando as mesmas entradas dão a mesma resposta, sempre. Os mesmos preços, as mesmas configurações e a mesma versão da ferramenta produzem as mesmas operações, as mesmas pontuações e o mesmo veredito, seja rodando hoje ou daqui a seis meses, na sua máquina ou na de outra pessoa.

## Por que importa

Um resultado que não pode ser reproduzido é um resultado que não pode ser verificado. Se duas execuções do mesmo teste discordam, você já não sabe se uma regra melhorou por causa de uma mudança que fez ou porque a ferramenta simplesmente respondeu diferente desta vez. Toda comparação ao testar uma regra, contra uma execução sem informação, contra uma forma mais simples de negociar, contra histórico que a regra nunca viu, parte do princípio de que a única coisa que mudou foi o que você mudou.

Também importa quando outra pessoa olha. Um colega, um revisor ou você mesmo mais adiante deveriam poder pegar as mesmas entradas e chegar ao mesmo número. Se não conseguem, o número é uma história, não uma evidência.

## O que quebra isso

Qualquer coisa que responda diferente de uma chamada para outra: um serviço externo consultado enquanto o teste roda, uma configuração que não é guardada junto com o resultado, um histórico corrigido sem aviso, uma etapa cuja ordem não é fixa. Nenhuma delas precisa ser grande para que duas execuções discordem.

## Como verificar as suas próprias ferramentas

Rode o mesmo teste duas vezes, sem mudar nada, e compare os resultados linha a linha. Depois pergunte se cada resultado diz exatamente quais preços, quais configurações e qual versão o produziram. Se não diz, você não conseguirá repeti-lo mais tarde, mesmo que a ferramenta em si seja determinística.

## Onde usamos isso

O Ultimate Trading System, o software que construímos, é feito assim. Não há nenhuma IA em nada do que roda: treino, pontuação, simulação e execução são aritmética simples sobre dados de mercado, e as mesmas entradas dão a mesma resposta todas as vezes. Cada conjunto de registros indica de qual veio, então um resultado pode ser rastreado até os preços e as configurações que o produziram, e calculado de novo. O teste gratuito não precisa de conta em nenhuma corretora. O trabalho roda em uma máquina sua; nada fica hospedado: https://ultimate-trading-system.com

As outras quatro palavras, execução sem informação, retido, reserva e padrão plantado, estão explicadas aqui: https://telegra.ph/Quatro-palavras-para-testar-uma-regra-de-negociação-execução-sem-informação-retido-reserva-padrão-plantado-11-20

Isto é software, não é aconselhamento financeiro. Negociar envolve um risco de perda considerável, e passar nestes testes não garante resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-pt): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
