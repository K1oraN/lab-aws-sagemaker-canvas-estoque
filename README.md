# 📊 Previsão de Estoque Inteligente na AWS

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas.

## 🚀 Passo a Passo (Desafio de Projeto):

### 1. Selecionando Dataset:

-   O dataset ultilizado para esses projeto para o treinamento da M.L. foi disponibilizado no proprio repositório da DIO em `datasets`.

![image](https://i.imgur.com/mLu0O3c.png)

### 2. Construindo e Treinando:

-  Agora iremos fazer algumas cofigurações definindo o QUANTIDADE_ESTOQUE como `target` e o ID_PRODUTO como `ITEM ID`.
-  Fiz também alterações nos campos `Specify the number of days you want to forecast into the future` onde vamos especificar o numero de dias que veremos no futuro para X, outra alteração foi habilitar o `Use holiday schedule` para usar feriados na predição.
-  Treinei esse modelo no modo `Quick Build`.

![image](https://i.imgur.com/UMm4bVK.png)

### 3. Analisando
-   Fiz ajuste no modelo para alcançar um métrica melhor, e a melhor que consegui foi essa na imagem usando o modo `Quick Build`.
-   Após o treinamento, aqui vemos que o valor ainda foi bem acima porque as metricas `MAPE, WAPE, RMSE` quanto mais perto de `0` melhor e comparando com o outro modelos exemplos teve um valor bem alto.
-   Uma coisa que poderiamos fazer era continuar treinando, mas me sastifez esses valores.

![image](https://i.imgur.com/nFTFk7l.png)

-   Outras coisas que podemos analisar é que o principais impactos foi no `preço` e `Feriados`, respectivamente com valores de `51%` e `12`% aproximadamente.

![image](https://i.imgur.com/vl0C9As.png)

### 4. Prevendo

-   Usa o modelo treinado, podemos ver o resultado final das previsões geradas.
-   Analisando vemos que o item denominado como `Item III` e `Item IV`, considerando isso no `datasets`. Podemos ver que o etoque que tivemos uma alta, então não seria necessário no momento a compra de mais itens.
-   Já no `Item V` vemos uma baixa que seria necessário a compra de mais desse item.

- P10 LINHA ROSA (Reflete um cenário pessimista)
- P50 LINHA VERDE(Reflete um cenário neutro)
- P90 LINHA AMARELO(Reflete um cenário otimista)

![image](https://i.imgur.com/UeuLDtx.png)
![image](https://i.imgur.com/jeVS9Ty.png)
![image](https://i.imgur.com/0NmCcbN.png)
