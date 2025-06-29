# DIO Invest

## Planilha de Investimentos: Projeção de Crescimento Financeiro
Este é um projeto de planilha que ajuda a visualizar e planejar seus investimentos mensais, projetando o crescimento do seu patrimônio e a renda passiva gerada por dividendos ao longo do tempo. A planilha é baseada em um perfil de investimento moderado e fornece sugestões de alocação em diferentes tipos de Fundos de Investimento Imobiliário (FIIs).

📊 Visão Geral
A planilha é dividida em algumas seções principais:

⚙️ Configurações: Onde você define seus dados básicos de renda e metas. Define o seu aporte mensal e o período de investimento para ver as projeções.
 - Quanto investir por mês?: R$ 200,00 (aporte)

 - Por quantos anos?: 5 (qtd_anos)

 - Taxa de Rendimento mensal?: 1,08% (taxa_mensal)


💰 Investimento Mensall: Calcula as projeções de crescimento do seu patrimônio e dividendos.

Cenários: Demonstra o potencial de crescimento do seu investimento em diferentes períodos.


🎯 Aba - Perfil de Investimento
Este modelo adota um perfil de investimento Moderado e sugere a alocação do seu valor mensal em diferentes tipos de FIIs para diversificar a carteira e reduzir riscos.

Perfil: Sugere a alocação do seu investimento mensal em diferentes categorias de FIIs.





## Fórmula para o Patrimônio Acumulado (na seção Cenários):
=FV($H$20; $F25 * 12; $H$18 * -1)

$H$20: Referência absoluta para a célula que contém a taxa_mensal.

$F25 * 12: A célula F25 contém o número de anos (2, 5, 10, etc.).

$H$18 * -1: Referência absoluta para a célula que contém o valor do aporte.


- Valor a ser investido por mês: R$ 200,00


## Fórmula para Alocação dos Valores:
=VLOOKUP(tipo_perfil & "-" & E35; Perfil!$A:$D; 4; FALSE)

VLOOKUP (PROCV): Procura um valor em uma coluna e retorna um valor correspondente de outra coluna na mesma linha.

tipo_perfil & "-" & E35: Cria um critério de busca concatenando o tipo de perfil (ex: "Moderado") e o tipo de FII (ex: "PAPEL") para encontrar a linha correta na planilha de referência.

Perfil!$A:$D: O intervalo de dados de busca na planilha chamada "Perfil".

4: O número do índice da coluna na qual o valor a ser retornado está localizado (a quarta coluna).

FALSE: Garante que a busca seja exata.

📄 Referências em outras planilhas
Esta planilha faz referência a uma ou mais planilhas de apoio para obter dados e sugestões:

Planilha "Perfil": Contém a tabela com a alocação de percentuais sugerida para cada tipo de FII, de acordo com o perfil de investidor (Moderado, Agressivo, etc.). A fórmula VLOOKUP é usada para buscar os valores nesta planilha.


## Como calcular os valores na tabela de Alocação Sugerida:

Para preencher a coluna "Valores (R$)", você deve multiplicar o "Percentual Sugerido" pelo "Valor a ser investido por mês".

Na primeira linha, a fórmula seria: [célula do percentual] * [célula do valor a ser investido] (ex: B40 * H38).

Importante: Para copiar a fórmula para as outras linhas sem erros, você deve congelar a célula que contém o valor a ser investido (a célula do R$ 200,00). Para fazer isso, use o $ (símbolo de dólar) ou pressione a tecla F4 no teclado.

A fórmula ficará assim: [célula do percentual] * $[célula do valor a ser investido] (ex: B40 * $H$38).

Depois de definir a fórmula na primeira linha, você pode simplesmente arrastar o canto inferior direito da célula para baixo para preencher as células restantes da coluna. A referência ao valor de investimento permanecerá fixa.
