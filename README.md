# AzureCognitiveSearch

# Utilizando AI Search para indexação e consulta de Dados

## Problema:

O desafio propoe que seja criada uma pesquisa que funcione juntamente com um serviço de inteligência artificial para identificar palavras chave, sentimentos, utilizando também o serviço de armazenamento do azure.

## Instruções Detalhadas:
Para um guia passo a passo detalhado deste módulo, consulte a documentação oficial da Microsoft disponível aqui: [Documentação](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

## Reflexões e Potencial da Ferramenta

Acredito que esta ferramenta possui um grande potencial, especialmente para figuras públicas como políticos, que poderiam utilizar a análise de aprovação do público e dados de pesquisas para obter insights confiáveis. Isso facilitaria o acesso a informações valiosas, como o sentimento geral da população e as regiões com maior suporte.

## Interpretação e consulta ao índice:

```
search=*&$count=true    (  verifica se a indexação esta funcionando e mostra os documentos )
```
![image](https://github.com/kobajk/AzureCognitiveSearch/assets/50890222/2bb8c0a0-6be5-4977-b281-de9d5fe61d4e)


```
search=locations:'Chicago' ( Consulta as ocorrencias acontecidas em Chicado )
```
![image](https://github.com/kobajk/AzureCognitiveSearch/assets/50890222/64823e28-59b5-4cf6-8a15-f9caba03aa36)

Nesse caso, consultou todos os feedbacks dados por pessoas em Chicago, como conseguimos observar em ("content"), que no total foram 3:
```
"content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n"

"content": "\n\nReview: The coffee tastings every Wednesday afternoon are so fun. Each month there is a new drink theme. You do need to book a spot in advance to attend. It is very worth it! I also love their local music. Fourth Coffee brings in rising artists every weekend. I like to head over there mid-afternoon on weekdays when it’s not too busy and get a slice of pie or their seasonal baked goods.  \nDate: August 13, 2018\nLocation: Chicago, Illinois  \n\nimage1.png\n\n\n\nimage2.png\n\n\n\n",

"content": "\nReview: I often make Fourth Coffee my meeting spot for my client meetings weekday mornings. I own a small business and the folks who work at Fourth Coffee are always very friendly. It leaves a good impression on my clients. There are also plenty of drink selections, good wi-fi, and seating. Some of my favorite coffees are the lavender honey latte and, in the winter, the apple-chai latte. There are delicious baked goods offered as well. \nDate: October 21, 2018\nLocation: Chicago, Illinois \n\nimage1.png\n\n\n\n",
```

Agora iremos pesquisar todas as reviews com sentimentos negativos:
```
search=sentiment:'negative' ( Consulta as ocorrencias com sentimento negativo )
```

![image](https://github.com/kobajk/AzureCognitiveSearch/assets/50890222/05d20421-e7fd-4f1a-86f1-22337087899f)
