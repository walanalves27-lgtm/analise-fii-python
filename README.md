# analise-fii-python
O sistema gera automaticamente um ranking dos FIIs com base em critérios objetivos e apresenta explicações detalhadas para cada indicador, além de exportar os resultados para Excel.

# Caderno Temático: Análise de Fundos Imobiliários (FIIs) com IA

---

## Contexto e Objetivos

Este projeto foi desenvolvido com o objetivo de estudar e compreender a análise de Fundos Imobiliários (FIIs) utilizando Inteligência Artificial como ferramenta de apoio.

A ideia principal foi criar um material estruturado que permita:

- Entender os principais indicadores dos FIIs
- Simplificar a leitura de relatórios gerenciais
- Apoiar a tomada de decisão de investimento
- Desenvolver pensamento crítico com auxílio de IA

## Curadoria de Fontes

As seguintes fontes foram utilizadas como base de estudo:

1. https://www.fundamentus.com.br/fii_resultado.php  
2. Relatórios gerenciais de FIIs (ex: MXRF11)  
3. https://www.b3.com.br  
4. https://statusinvest.com.br/fundos-imobiliarios  
5. Conteúdos educacionais sobre FIIs (artigos e PDFs)

## Engenharia de Prompts e "Cicatrizes"

Durante o desenvolvimento, utilizei diversos prompts para extrair informações e melhorar o entendimento.

### Exemplos de Prompts

- "Resuma este relatório gerencial de FII de forma simples para iniciantes"
- "Explique o que é P/VP em FIIs como se fosse para um iniciante"
- "Quais são os principais indicadores para analisar um fundo imobiliário?"

### Dificuldades Encontradas

- Dificuldade em extrair dados de PDFs (formatação inconsistente)
- Problemas com leitura de texto (maiúsculas/minúsculas)
- Erros em regex ao buscar valores específicos
- Estrutura HTML inconsistente no scraping

---

### Soluções Aplicadas

- Uso de `.lower()` e `re.IGNORECASE`
- Validação de dados antes de acessar listas
- Uso de `try/except` para evitar falhas
- Identificação dinâmica de tabelas no HTML

---

## Miniguia de Estudo

### O que são FIIs?

Fundos Imobiliários (FIIs) são investimentos que permitem aplicar em imóveis sem precisar comprar um imóvel diretamente.

### Principais Indicadores

#### P/VP
- Compara o preço da cota com o valor patrimonial
- < 1 → pode estar barato
- > 1 → pode estar caro

#### Liquidez
- Volume de negociação do fundo
- Alta liquidez = mais facilidade para comprar/vender

#### Vacância
- Percentual de imóveis desocupados
- Quanto menor, melhor

### Estratégia Básica de Análise

- Buscar fundos com P/VP próximo ou abaixo de 1
- Priorizar alta liquidez
- Evitar fundos com alta vacância

## Glossário

- **FII**: Fundo de Investimento Imobiliário  
- **P/VP**: Preço sobre Valor Patrimonial  
- **Liquidez**: Volume de negociação  
- **Vacância**: Percentual de imóveis vazios  
- **Yield**: Retorno percentual  

## Prompts Reutilizáveis

- "Explique este indicador financeiro de forma simples"
- "Resuma este relatório destacando pontos importantes"
- "Quais riscos devo considerar neste investimento?"
- "Transforme esse conteúdo técnico em linguagem simples"

## Conclusão

Este projeto permitiu desenvolver habilidades práticas em:

- Análise de dados financeiros
- Uso de IA como ferramenta de estudo
- Organização de conhecimento
- Pensamento crítico

Além disso, mostrou como a tecnologia pode facilitar a vida de investidores iniciantes.

## Autor

Projeto desenvolvido para fins educacionais como parte da formação em tecnologia.
