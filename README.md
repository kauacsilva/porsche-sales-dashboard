# Porsche Sales Dashboard

Dashboard interativo para explorar registros comerciais de veículos Porsche por modelo, ano-modelo, cidade e forma de pagamento, com origem declarada em uma planilha Excel e apresentação em HTML.

A solução reúne indicadores, rankings e comparações por cidade em um arquivo que pode ser aberto diretamente no navegador, sem instalação ou conexão com a internet.

**Arquivo principal:** [dashboard-porsche.html](https://github.com/kauacsilva/porsche-sales-dashboard/blob/main/arquivos/dashboard-porsche.html)

> Projeto independente, sem vínculo oficial com a Porsche. As contagens representam registros comerciais, incluindo pedidos pendentes, e não equivalem a vendas concluídas ou veículos entregues.

## Índice

- [Visão geral](#visão-geral)
- [Objetivos e perguntas de negócio](#objetivos-e-perguntas-de-negócio)
- [Dados e metodologia](#dados-e-metodologia)
- [Ferramentas e tecnologias](#ferramentas-e-tecnologias)
- [Como utilizar](#como-utilizar)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Autor e contato](#autor-e-contato)

## Visão geral

O projeto aborda a necessidade de comparar a distribuição de registros comerciais entre modelos e cidades dos Estados Unidos, identificando os anos-modelo mais frequentes e as diferenças entre mercados locais.

O dashboard transforma os dados incorporados ao arquivo em uma visão navegável, com filtros combináveis e critérios de contagem explícitos. Isso permite explorar possíveis prioridades de investigação comercial sem confundir volume registrado com demanda comprovada.

O valor prático está na consulta interativa, na comparação entre segmentos e na exposição de limitações da base, especialmente datas inválidas, cancelamentos e baixo número de observações por cidade. O documento não apresenta mensuração de ganhos financeiros, produtividade ou impacto comercial após a implementação.

## Objetivos e perguntas de negócio

- Quais modelos apresentam maior número de registros em cada cidade?
- Qual ano-modelo tem maior participação no período selecionado?
- Quais modelos aparecem com menor frequência em cada cidade?
- Como os resultados mudam ao selecionar modelo, ano-modelo, cidade ou pagamento?
- Como a inclusão de cancelamentos e a exclusão de datas inválidas afetam a análise?

## Dados e metodologia

### Fonte e escopo

O HTML declara como fonte o arquivo `Porshue_database.xlsx`. Esta documentação foi elaborada exclusivamente a partir de `dashboard-porsche.html`, incluindo os dados e as regras presentes no código.

| Característica | Base completa incorporada |
| --- | --- |
| Registros | 100 |
| Cidades distintas | 79 |
| Modelos distintos, mantendo versões separadas | 40 |
| Anos-modelo | 2020 a 2026 |
| Intervalo das datas válidas | 14/03/2024 a 01/10/2027 |



O painel utiliza seis campos por registro: data de venda, modelo, ano-modelo, forma de pagamento, cidade e status de entrega. Não incorpora preços nem calcula faturamento, margem ou ticket médio.

### Etapas verificáveis

1. **Uso de dados previamente tratados:** o documento informa o uso de colunas `Sanitized`. As fórmulas e os procedimentos que produziram essas colunas não estão documentados no HTML.
2. **Incorporação dos dados:** os valores estão armazenados em uma estrutura JavaScript dentro do próprio arquivo, sem leitura automática da planilha.
3. **Aplicação das regras:** os filtros globais são combinados, e os registros cancelados são excluídos por padrão.
4. **Agregação:** os registros são agrupados e contados por modelo, ano-modelo e cidade.
5. **Apresentação:** indicadores, barras, comparações locais e textos de interpretação são recalculados conforme a seleção.


## Ferramentas e tecnologias

| Tecnologia ou recurso | Aplicação comprovada |
| --- | --- |
| Planilha Excel (`.xlsx`) | Fonte declarada dos dados, na aba `Sanitized` |
| HTML | Estrutura da página, indicadores, filtros e tabela |
| CSS | Layout responsivo, barras visuais, cores e hierarquia visual |
| JavaScript | Dados incorporados, filtragem, agrupamento, contagem, ordenação e atualização da interface |
| Navegador com JavaScript habilitado | Execução local da solução |

O HTML é autossuficiente: não depende de bibliotecas externas, servidor ou instalação de pacotes. O documento não comprova o uso de fórmulas específicas do Excel, tabelas dinâmicas, Power Query, VBA, Power Pivot ou Power BI.


## Como utilizar

### Abrir e explorar

1. Baixe [dashboard-porsche.html](https://github.com/kauacsilva/porsche-sales-dashboard/blob/main/arquivos/dashboard-porsche.html).
2. Abra o arquivo em um navegador com JavaScript habilitado. A visualização do código no GitHub não executa o painel.
3. Use os filtros de modelo, ano-modelo, cidade e pagamento para definir o recorte geral.
4. Preencha uma ou ambas as datas para analisar um período e observe o aviso sobre exclusão de registros sem data válida.
5. Ative “Incluir registros cancelados” apenas quando quiser incorporá-los à contagem.
6. Em “Preferências por cidade”, use “Explorar cidade” para restringir apenas essa seção.
7. Use “Anterior” e “Próxima” para navegar pelas cidades. “Ver todas” remove somente a seleção local, preservando os filtros globais.
8. Use “Limpar filtros” para voltar ao estado inicial e consulte “Sobre a base e os critérios da análise” para revisar as regras.

Não é necessário abrir a planilha ou ter o Excel instalado para utilizar o dashboard.

## Estrutura do repositório

Organização sugerida para publicação; não representa uma estrutura de repositório já verificada.

| Caminho | Finalidade | 
| --- | --- | 
| `README.md` | Documentação do projeto | Este documento |
| `dashboard-porsche.html` | Dashboard completo, com estilos, código e dados incorporados  
| `Porsche_database.xlsx` | Dados fictícios para a elaboração do dashboard com auxilio de Inteligência Artificial 

A planilha `Porshue_database.xlsx` é citada como fonte pelo HTML, mas sua localização em um repositório e sua disponibilização para terceiros não estão documentadas.


## Autor e contato

- **Autor:** Kauã Castro
- **LinkedIn:** [https://www.linkedin.com/in/kauã-castro]

Projeto de análise independente. A marca Porsche é utilizada como referência temática e não indica afiliação, parceria ou validação oficial.
