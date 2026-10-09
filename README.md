# Reorganização pedagógica e monitoria acadêmica no ensino introdutório de programação: um estudo de caso longitudinal

Material suplementar do artigo submetido à Revista Brasileira de Informática na Educação (RBIE).

> **Versão anonimizada para avaliação por pares.** Informações que identificam a instituição e as pessoas autoras foram omitidas e serão restauradas na versão final.

## Descrição

Este repositório reúne os dados agregados e o código utilizados nas análises do artigo, que investiga a associação entre fases de organização pedagógica e o desempenho dos estudantes na disciplina Algoritmos e Programação I, do curso de Bacharelado Interdisciplinar em Ciência e Tecnologia (BICT) de uma universidade pública federal da região Nordeste do Brasil, no período de 2019 a 2025.

O período foi organizado em três fases:

| Fase | Período | Caracterização |
|---|---|---|
| 1 | 2019–2022 | Sem registros sistematizados de monitoria formal |
| 2 | 2023 | Reorganização pedagógica da disciplina |
| 3 | 2024–2025 | Monitoria acadêmica estruturada |

## Conteúdo

| Arquivo | Descrição |
|---|---|
| `Planilha_resultado_turmas.xlsx` | Dados agregados por turma (2019–2026), sem identificação de estudantes ou docentes |
| `Analise_estatistica_turmas.ipynb` | Notebook com o pré-processamento, as análises estatísticas e a geração das figuras |
| `README.md` | Este arquivo |

## Dicionário de dados

Cada linha da planilha corresponde a uma turma da disciplina em um semestre letivo. A primeira linha do arquivo é um título e é ignorada na leitura (`skiprows=1`).

| Coluna | Descrição |
|---|---|
| `Disciplina` | Nome do componente curricular |
| `Ano/Período` | Semestre letivo (data no formato AAAA-MM-DD, em que o mês indica o período: 01, 02 ou 03) |
| `Código` | Identificação da turma no semestre (Turma 01, 02 etc.) |
| `CH Total do Componente` | Carga horária total da disciplina, em horas |
| `Tipo` | Tipo de semestre (regular ou suplementar) |
| `Situação` | Situação da turma no sistema acadêmico (consolidada ou aberta) |
| `Horário` | Código de horário; a letra N indica turno noturno, e as letras M e T, turno integral |
| `Matrículas` | Número de estudantes matriculados na turma |
| `Capacidade` | Número de vagas ofertadas |
| `Data Início` / `Data Fim` | Datas de início e término do semestre letivo |
| `APR` | Número de estudantes aprovados |
| `REP` | Número de estudantes reprovados por desempenho |
| `REPMF` | Número de estudantes reprovados por média e faltas |
| `Total` | Soma de APR, REP e REPMF |

As turmas de 2026, ainda não consolidadas, constam na planilha, mas são excluídas das análises.

## Análises realizadas

**Análise geral por fase**
- Taxas de aprovação e reprovação por desempenho entre estudantes ativos (APR + REP)
- Teste qui-quadrado de independência e V de Cramér
- Teste de tendência de Cochran-Armitage

**Análises complementares**
- Análise de sensibilidade com a fase de referência restrita aos anos de oferta presencial (2019 e 2022)
- Estratificação por turno: teste de Cochran-Mantel-Haenszel generalizado e teste exato de Fisher

Adotou-se nível de significância de 5% em todos os testes.

## Correspondência com o artigo

| Elemento do artigo | Seção do notebook |
|---|---|
| Tabela 4 e Figura 2 | Análise descritiva anual |
| Figura 3 e testes da análise geral | Análise por fase temporal |
| Análise de sensibilidade | Análise de sensibilidade (sem 2020 e 2021) |
| Tabela 5 e Figura 4 | Análise complementar por turno |

##