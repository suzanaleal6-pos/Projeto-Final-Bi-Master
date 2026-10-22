<!-- antes  de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Validação dos Créditos de PIS/COFINS a Recuperar na Empresa InfraPower Energia S.A.

#### Aluno: [Suzana Maria Leal de Jesus](https://github.com/suzanaleal6-pos)
#### Orientador: [Anderson Nascimeto](https://github.com/insightds).
#### Co-orientador(/a/es/as): [Nome Sobrenome](https://github.com/link_do_github). 

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/link_do_repositorio). <!-- caso não aplicável, remover esta linha -->

- [Link para a monografia](https://link_da_monografia.com). <!-- caso não aplicável, remover esta linha -->

- Trabalhos relacionados: <!-- caso não aplicável, remover estas linhas -->
    - [Nome do Trabalho 1](https://link_do_trabalho.com).
    - [Nome do Trabalho 2](https://link_do_trabalho.com).

---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->
O objetivo do projeto é a revisão e validação dos créditos de PIS/COFINS apropriados no Ativo Imobilizado da empresa. Com o advento da Reforma Tributária, o PIS e a COFINS serão extintos em 31/12/2026, porém o saldo remanescente dos créditos de Pis e Cofins do Ativo Imobilizado, continuará válido e será convertido em créditos presumidos CBS (Contribuição Sbre Bens e Serviços). Para garantir a migração, o saldo deve estar escriturado corretamente na EFD-Contribuições, ainda no sistema do PIS e Cofins, por isso a importãncia dessa revisão e validação.

### Abstract <!-- Opcional! Caso não aplicável, remover esta seção -->
The project aims to review and validate PIS and COFINS credits associated with the company's fixed assets. With the advent of the Tax Reform, PIS and COFINS will be abolished on December 31, 2026; however, the remaining balance of fixed-asset PIS and COFINS credits will remain valid and be converted into CBS (Contribution on Goods and Services) presumed credits. To ensure this migration, the balance must be correctly recorded in the EFD-Contribuições filing—while still under the PIS and COFINS system—which underscores the importance of this review and validation process.

<!-- trocar o texto abaixo pelo resumo do trabalho, em inglês -->

### 1. Introdução

A legislação do PIS e da COFINS (Leis nº 10.637/2002 e nº 10.833/2003) estabelece que a base de cálculo dessas contribuições sociais é o faturamento mensal, permitindo o desconto de créditos apurados com base em custos, despesas e encargos da pessoa jurídica nas alíquotas de 1,65% e 7,6%, respectivamente. 
Na empresa InfraPower Energia S.A os valores das contribuições são lançados nas contas patrimoniais de longo prazo, a partir do registro do faturamento aos fornecedores, nas contas 1214000004 – PIS/PASEP Diferido LP e 1214000005 – COFINS Diferido LP.
Esses valores são replicados em três tabelas, formando um repositório de dados dos documentos contábeis e fiscais associados aos seus respectivos objetos de custo, que identificarão os bens patrimoniais:

•	MERIN – Créditos de materiais e serviços do mercado interno
•	MERC – Créditos de materiais importados
•	SERV – Créditos sobre serviços prestados no mercado externo

Como a apropriação do crédito de PIS e COFINS está vinculada ao início da depreciação do bem, foram criadas áreas de avaliação 90 – PIS e 91 – COFINS no módulo AA do SAP, para cada imobilizado identificado com direito a crédito.

### 2. Modelagem

Para desenvolver esse trabalho de revisão e validação dos créditos do PIS e da COFINS, apropriados no Ativo Imobilizado, escolhemos o período de 10/2025, e utilizaremos as seguintes ferramentas:
Datasphere - É a plataforma cloud da SAP para integração, é onde está a base de dados com as tabelas e views brutas. Serão usadas as tabelas MERIN (compras no mercado interno), ANEP e ANEK, que são tabelas do Ativo Imobilizado. A MERIN contém todos os dados contábeis e fiscais, e são apropriados os créditos do PIS e COFINS brutos, no momento do registro da fatura, com a execução de JOBs diários, os valores devidos irão para os respectivos imobilizados
DBeaver - é o banco de dados que faz conexão com o Datasphere onde serão consumidas as tabelas e feito os SQLs;
KNIME - é uma plataforma para análise de dados e automação de processos de dados (ETL/ELT). O Knime consumirá os dados provenientes do SQL executado no Dbeaver, os dados serão tratados e preparados, até termos o resultado, que será a exportação para um arquivo em Excel.


### 3. Resultados

Dos R$ 577 mil em créditos de PIS e COFINS gerados na competência de 10/2025, que deveriam estar contabilizados no Ativo Imobilizado da empresa, verificou-se que R$ 545 mil (94%) foram apropriados corretamente, enquanto R$ 32 mil (6%) apresentaram divergência entre o crédito gerado e o valor apropriado no Ativo Imobilizado — condição necessária para o posterior aproveitamento do crédito.

### 4. Conclusões

A conclusão indica que parte dos créditos a que a InfraPower Energia S.A. tem direito não está refletida no Ativo Imobilizado e, portanto, não poderá ser aproveitada enquanto não for regularizada, quando os bens entrarem em operação e iniciarem sua depreciação. A validação permitiu identificar os valores corretos e fornecer subsídios para os ajustes necessários, de modo que, até dezembro de 2026, o saldo de PIS/COFINS esteja regularizado e apto à migração prevista na Reforma Tributária.
---

Matrícula: 241.100.083

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
