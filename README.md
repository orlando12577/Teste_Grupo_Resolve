# Relatório do projeto:

O projeto foi desenvolvido no Google Colab, utilizando Python para realizar o tratamento, limpeza, padronização e consolidação de dados provenientes de duas planilhas de vendas com estruturas diferentes: System Report e Q-Log.

O primeiro passo foi analisar a estrutura de ambas as bases para identificar diferenças nas colunas, tipos de dados e formato dos registros. No Q-Log, foi necessário reconstruir a coluna ID do Pedido, já que os identificadores apareciam em linhas separadas das vendas. Em seguida, as informações foram propagadas para os respectivos itens do pedido utilizando preenchimento sequencial (forward fill).

Após isso, as duas planilhas passaram por um processo de padronização, incluindo a renomeação das colunas para um formato único, conversão dos tipos de dados (datas, quantidades e preços) e normalização das informações para que ambas pudessem ser consolidadas.
Na etapa de limpeza dos dados, foram removidos registros que não faziam parte das vendas válidas, como itens cancelados, impostos de importação, taxas de transporte/frete e registros sem preço. Também foram realizadas validações para garantir que não existissem valores nulos ou registros duplicados na base final.

Com os dados tratados, foi realizada a consolidação das duas fontes em um único conjunto de dados, além da criação de uma coluna de Valor Total, calculada pela multiplicação da quantidade pelo preço unitário.
Por fim, foi desenvolvido um resumo analítico utilizando agregação por cliente e produto, apresentando a quantidade total adquirida e o valor total gasto por cada cliente em cada produto. O resultado foi exportado para um arquivo Excel contendo duas abas: uma com a base consolidada e outra com o resumo das compras.

##Tecnologias Utilizas:

- Google Colab (ambiente de desenvolvimento)
- Python
- Pandas (manipulação e análise de dados)
- OpenPyXL (geração do arquivo Excel)
- Regex (Expressões Regulares) para identificação de registros inválidos
- Excel (.xlsx) como formato de entrada e saída dos dados
