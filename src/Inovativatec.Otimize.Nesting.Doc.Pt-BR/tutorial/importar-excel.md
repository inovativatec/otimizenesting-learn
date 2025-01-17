# Importação de uma lista de peças do Excel

O Otimize Nesting é, antes de tudo, uma ferramenta de software de produtividade. Ele inclui os recursos de que você precisa para a criação de agrupamentos de peças altamente produtivos.

Se há um recurso comum a todos os aplicativos de produtividade, é a capacidade de ler dados de planilhas do Excel. Essas planilhas geralmente são criadas manualmente, por exemplo, no Microsoft Excel, ou automaticamente por outro programa de software.

Este tópico aborda os conceitos básicos da importação de listas de peças retangulares e o ajuda a economizar tempo.

> \[OBSERVAÇÃO] Sistemas CAD ou ERP especiais podem criar arquivos digitais com listas de peças para melhorar a integração do sistema. Se esses arquivos tiverem a configuração de coluna correta, eles poderão ser importados para o Otimize Nesting.

A importação de sua lista de peças existente para o Otimize Nesting envolve duas etapas principais: preparar o arquivo e importá-lo usando o Otimize Nesting.

## Parte 1: Preparar o arquivo da lista de peças

Prepare uma planilha contendo a lista de peças que deseja produzir. O Otimize Nesting espera uma determinada posição de coluna na planilha para cada informação de peça. A imagem a seguir mostra um exemplo de lista de peças.

![Exemplo de lista de peças](./import-excel/importExcelPartList.png "Exemplo de lista de peças")

As colunas são as seguintes:

**Descrição**: Essa é a primeira coluna do arquivo, que contém a descrição textual da peça que deve ser produzida. Os diagramas de aninhamento sobre a área da peça exibirão esse texto.

**Width (Largura**): Representa a largura da peça a ser produzida. A unidade de comprimento (milímetros, centímetros, polegadas) deve corresponder à que você selecionou na configuração do software.

**Length (Comprimento**): O mesmo se aplica à coluna de largura aqui.

**Quantidade**: Representa o número de peças idênticas que serão produzidas.

**Material**: Representa o nome da matéria-prima a partir da qual essa peça será produzida. Durante a importação, o Otimize Nesting verifica se esse material já existe na lista de materiais. Caso contrário, será adicionado um novo registro de material com um tamanho de placa padrão.

**Rotação/Grão**: Se a coluna contiver **1** (recomendado para a maioria dos cenários), essa peça poderá ser girada em etapas de 90 graus para que o otimizador possa encontrar um layout melhor.

Essa opção deve ser definida como **1**, a menos que as peças que você produz sejam provenientes de um material com grãos ou veios. Nesse caso, recomendamos deixar o valor dessa coluna igual a **0**.

**Edge Band (Faixa de borda**): As últimas quatro colunas indicam qual lado da peça receberá o material de acabamento. No caso de móveis, por exemplo, elas indicam quais lados da peça receberão uma fita de borda. A ordem desses lados da fita de borda é a seguinte:

- Superior
- Direito
- Inferior
- Esquerda

Quando todos os dados forem adicionados à planilha, salve-a em um arquivo no seu computador local.

Você deve salvar esse arquivo no formato CSV (Comma Separated Values, valores separados por vírgula):

1. Vá para a planilha no Microsoft Excel e selecione **File** -> **Save As (** **Arquivo** -> **Salvar como**).
2. Será exibida uma caixa de diálogo. Selecione a pasta desejada, digite o nome do arquivo e selecione **CSV (delimitado por vírgulas) (\*.csv)** para salvar como tipo.

![Salvar lista de peças](./import-excel/importExcelSaveAs.png)

Como alternativa, [faça o download deste exemplo de arquivo .csv](./import-excel/SampleCSVPartList.csv) com a formatação correta das colunas e use-o como modelo para suas listas de peças.

## Parte 2: Importar o arquivo de lista de peças

1. Inicie o Otimize Nesting.
2. Crie um novo projeto ou abra um projeto existente. Vá para a guia **Parts (Peças** ).
3. Selecione **Importar peças** -> **csv**.

![Importar peças](./import-excel/importExcelImportCSV.png)

4. A caixa de diálogo **Abrir** arquivo é exibida. Localize e selecione o arquivo .csv que você salvou anteriormente. Selecione **Abrir**.
5. A página **Importar arquivo** é exibida com a lista de peças.

![Página de importação](./import-excel/importExcelImportPage.png)

6. Selecione **Importar**. As peças serão adicionadas ao projeto, e a guia Peça será exibida novamente.

![Peças importadas](./import-excel/importExcelImportedParts.png)

## Solução de problemas

### Configurações regionais

Idiomas e regiões diferentes podem usar caracteres de separação de colunas diferentes para planilhas. Se houver erros na página **Importar arquivo**:

1. Selecione o separador correto
2. Selecione **Refresh (Atualizar** ) para que os dados sejam atualizados

![Selecione Separador](./import-excel/importExcelIncorrectSeparator.png)

### Cabeçalhos de linha

Normalmente, as planilhas contêm nomes de colunas de cabeçalho na primeira linha. Essa ou qualquer outra linha pode ser ignorada na página **Import File (Importar arquivo)**.

![Ignorar linhas](./import-excel/importExcelIgnoreRows.png)
