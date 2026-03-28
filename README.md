# Sistema de Análise de FIIs com IA

O sistema realiza a coleta automática de dados de Fundos Imobiliários (FIIs), aplica critérios objetivos de análise e gera um ranking com explicações detalhadas para cada indicador, além de permitir a exportação dos resultados para Excel.

# Caderno Temático: Análise de FIIs com IA

## Contexto e Objetivos

Este projeto foi desenvolvido com o objetivo de estudar e compreender a análise de Fundos Imobiliários (FIIs) utilizando Inteligência Artificial como ferramenta de apoio.

A proposta foi criar um material estruturado que permitisse:

- Entender os principais indicadores dos FIIs  
- Simplificar a leitura de relatórios gerenciais  
- Apoiar a tomada de decisão de investimento  
- Desenvolver pensamento crítico com auxílio de IA  

## Curadoria de Fontes (NotebookLM)

As seguintes fontes foram utilizadas e inseridas no NotebookLM:

### Fundamentus – Lista de FIIs
- Link: https://www.fundamentus.com.br/fii_resultado.php  
- Tipo: Página Web  
- Conteúdo: Indicadores como P/VP, liquidez e vacância  

### Status Invest – Fundos Imobiliários
- Link: https://statusinvest.com.br/fundos-imobiliarios  
- Tipo: Página Web  
- Conteúdo: Dados complementares e comparativos  

### B3 – Bolsa de Valores
- Link: https://www.b3.com.br  
- Tipo: Página Web  
- Conteúdo: Funcionamento do mercado de FIIs
  
### Artigos Educacionais
- Tipo: Texto/PDF  
- Conteúdo: Conceitos e estratégias de investimento  

## Engenharia de Prompts e "Cicatrizes"

### Exemplos de Prompts

- "Resuma este relatório gerencial de FII de forma simples para iniciantes"  
- "Explique o que é P/VP de forma simples"  
- "Quais são os principais indicadores de FIIs?"  

### Dificuldades Encontradas

- Extração de dados de PDFs  
- Problemas com maiúsculas/minúsculas  
- Erros com regex  
- Estrutura HTML inconsistente no scraping
  
### Soluções Aplicadas

- Uso de `.lower()` e `re.IGNORECASE`  
- Validação de listas antes de acessar índices  
- Uso de `try/except`  
- Identificação dinâmica de tabelas no HTML
  
## Miniguia de Estudo

### O que são FIIs?

Fundos Imobiliários (FIIs) são investimentos que permitem aplicar em imóveis sem precisar comprá-los diretamente.

### Principais Indicadores

#### P/VP
- Compara o preço com o valor patrimonial  
- < 1 → pode estar barato  
- > 1 → pode estar caro  

#### Liquidez
- Volume de negociação  
- Quanto maior, melhor  

#### Vacância
- Percentual de imóveis vazios  
- Quanto menor, melhor
  
## Estratégia Básica

- Buscar FIIs com P/VP próximo ou abaixo de 1  
- Priorizar alta liquidez  
- Evitar alta vacância
  
## Glossário

- **FII**: Fundo Imobiliário  
- **P/VP**: Preço sobre valor patrimonial  
- **Liquidez**: Volume negociado  
- **Vacância**: Imóveis desocupados  
- **Rendimento**: Retorno do investimento  

## Prompts Reutilizáveis

- "Explique de forma simples"  
- "Resuma este relatório"  
- "Quais riscos existem?"  
- "Transforme em linguagem simples"
  
## Conclusão

Este projeto permitiu desenvolver habilidades em:

- Análise de dados  
- Uso de IA  
- Web scraping  
- Organização de informação  

Além disso, demonstrou como a tecnologia pode ajudar investidores iniciantes.

## Autor

Projeto desenvolvido como parte da formação em tecnologia.
