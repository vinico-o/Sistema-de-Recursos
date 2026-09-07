## 1. Introdução

### 1.1 Propósito do Documento de Requisitos

Este documento tem como propósito definir e descrever os requisitos funcionais e não funcionais de um Sistema de Recursos.

Além disso, o documento será utilizado como referência no planejamento, implementação, testes e manutenção do sistema, para assim garantir que todas as necessidades referentes ao sistema sejam satisfeitas.

O público-alvo deste documento envolve:

- Gerentes de Software do sistema;
- Analistas e Projetistas;
- Grupo de SQA;
- Desenvolvedores responsáveis pela implementação do sistema;

### 1.2 Escopo do Produto

O sistema tem como objetivo auxiliar na organização e no controle do estoque, de vendas e do desempenho financeiro de um comércio.

O sistema será utilizado para:

- Cadastrar produtos no catálogo do estoque;
- Controlar compra e vendas dos produtos;
- Acompanhar o desempenho financeiro do comércio;

O Sistema de Recursos é destinado principalmente a pequenos e médios estabelecimentos comerciais do setor varejista, oferecendo recursos para o gerenciamento integrado de estoque, compras, vendas e operações financeiras. O sistema busca atender negócios que necessitam de uma ferramenta de gestão simplificada, capaz de centralizar suas operações e fornecer informações para auxiliar no controle e na tomada de decisões.

O sistema não contempla APIs de pagamentos, de emissão de Nota Fiscal ou de autenticação. Todos os dados serão inseridos manualmente pelo usuário.

### 1.3 Definições, acrônimos e abreviações

As principais definições, abreviações e acrônimos utilizados neste documento serão listados a seguir.

| Termo / Definição |  |
| --- | --- |
| **RF** | Requisito Funcional. Descreve uma funcionalidade ou comportamento que o sistema deve oferecer. |
| **RNF** | Requisito Não Funcional. Descreve uma característica de qualidade, restrição ou comportamento esperado do sistema. |
| **RG** | Restrição Geral. Define limitações ou condições que devem ser obrigatoriamente respeitadas pelo sistema. |
| **(E)** | Explícito ao usuário. Requisito cuja execução é visível e perceptível pelo usuário através da interface do sistema. |
| **(O)** | Oculto ao usuário. Requisito processado internamente pelo sistema, sem interação direta com o usuário. |
| **Estoque** | Conjunto de produtos e mercadorias armazenados pela empresa e disponíveis para comercialização ou utilização. |
| **Entrada** | Movimentação responsável por aumentar a quantidade de determinado produto disponível no estoque. |
| **Saída** | Movimentação responsável por diminuir a quantidade de determinado produto disponível no estoque. |
| **Estoque mínimo** | Quantidade mínima de um produto que deve ser mantida em estoque para evitar sua falta. |
| **Produto** | Item comercializado ou armazenado pela empresa, possuindo informações como nome, categoria, preço e quantidade em estoque. |
| **Venda** | Operação comercial na qual um ou mais produtos são vendidos a um cliente. |
| **Receita** | Valor financeiro recebido ou a receber pela empresa, como resultado de vendas ou outras operações. |
| **Despesa** | Valor financeiro pago ou a pagar pela empresa para manutenção de suas atividades. |
| **Saldo** | Diferença entre o total de receitas e o total de despesas registradas no sistema em determinado período. |
| **Fluxo de caixa** | Registro e acompanhamento das entradas e saídas financeiras da empresa ao longo de determinado período. |
| **Movimentação financeira** | Registro de uma operação que altera o fluxo financeiro da empresa, podendo representar uma receita ou despesa. |
| **SQA** | Software Quality Assurance (Garantia de Qualidade de Software). |
| **JVM** | Java Virtual Machine (Máquina Virtual Java). |
| **Login** | Processo pelo qual um usuário se autentica no sistema por meio de suas credenciais. |
| **Logout** | Processo pelo qual um usuário encerra sua sessão no sistema. |

### 1.4 Referências

### 1.5 Visão do restante do Documento

Esse documento está organizado em seções, cada uma responsável por descrever partes específicas do sistema proposto. São elas:

- Seção 2: Apresenta a descrição geral do sistema, indicando os aspectos principais, como perspectivas, funcionalidades, restrições, suposições e dependências do produto. Com isso é possível ter uma visão mais específica do objetivo da aplicação.
- Seção 3: Descreve com maior detalhamento os requisitos do sistema, de como ele se comunicará com o mundo exterior, e lista as funções e recursos específicos. Com isso será possível ter uma visão geral e entender com mais clareza o funcionamento do sistema.
- Seção 4: Acrescenta ao documento informações complementares que auxiliam o entendimento dos requisitos do sistema e do funcionamento geral do sistema.
- Seção 5: Parte do documento que lista todas as seções presentes no documento, além de uma lista alfabética com os termos-chave, conceitos e siglas utilizados seguido da página em que aparecem.

## 2. Descrição Geral

O Sistema de Recursos - Gestão de Estoque, Vendas e Financeiro tem como objetivo auxiliar empresas no gerenciamento de seus produtos, vendas e operações financeiras. O sistema centralizará essas informações, permitindo o controle do estoque, o registro de vendas e o acompanhamento das movimentações financeiras.

### 2.1 Perspectiva do Produto

O Sistema de Recursos será desenvolvido como uma aplicação independente. Ele tem como objetivo auxiliar na organização e gerenciamento do estoque e vendas, como também acompanhar o desempenho financeiro da empresa.

O sistema será composto por módulos que compartilham informações entre si, sendo eles: Estoque, Vendas e Financeiro. Dessa forma, operações em um módulo poderá produzir alterações nos demais módulos.

O usuário interagirá com o sistema por meio de uma interface gráfica, desse modo, ele poderá executar as operações de cada um dos módulos.

### 2.2 Funcionalidade do Produto

O sistema será dividido em três módulos principais: Estoque, Vendas e Financeiro.

#### 2.2.1 Módulo de Estoque

Responsável pelo controle dos produtos armazenados pela empresa.

Principais funcionalidades:

- Cadastrar, alterar, consultar e remover produtos do catálogo;
- Cadastrar categorias de produtos;
- Consultar produtos disponíveis no catálogo;
- Consultar movimentações do estoque.

#### 2.2.2 Módulo de Vendas

Responsável pelo registro e acompanhamento das vendas realizadas.

Principais funcionalidades:

- Registrar uma nova venda;
- Consultar histórico de vendas.

#### 2.2.3 Módulo Financeiro

Responsável pelo controle das movimentações financeiras da empresa.

Principais funcionalidades:

- registrar receitas e despesas;
- Consultar movimentações financeiras;
- Controlar pagamentos;
- Consultar saldo;
- Gerar relatórios financeiros.

### 2.3 Características do Usuário

TODO: verificar se é melhor colocar mais niveis de usuario.

Os usuários deverão possuir conhecimentos básicos de informática e estar familiarizados com as operações relacionadas à estoque, vendas e gestão financeira.

### 2.4 Restrições Gerais

RG01 - O sistema deve ser desenvolvido em linguagem Java.

RG02 - Todos os registros e informações do sistema devem ser armazenados de maneira permanente em um TODO: banco de dados ou arquivo???, a fim de garantir a existência e a integridade dos dados mesmo fora da execução do sistema.

RG03 - O sistema deve ser executável em qualquer sistema operacional compatível com a JVM (Java Virtual Machine), incluindo Windows e Linux.

RG04 - O sistema operará em modo de usuário único por sessão, sem suporte a acesso simultâneo de múltiplos usuários em tempo real.

RG05 - O acesso ao sistema deve restrito a usuários autenticados por meio de login e senha. Nenhuma funcionalidade do sistema pode ser acessada sem autenticação prévia.

### 2.5 Suposições e Dependências

#### 2.5.1 Suposições

- Assume-se que os usuários do sistema possuem conhecimento básico de informática para operar o sistema.
- Assume-se que o computador onde o sistema será executado possui Java instalado e configurado corretamente.
- Assume-se que o sistema seja utilizado para apenas um comércio.

#### 2.5.2 Dependências

- O sistema depende da disponibilidade de um ambiente computacional capaz de executar aplicações desenvolvidas na linguagem Java, sendo necessários sistemas operacionais que suportam Máquina Virtual Java (JVM), como Linux ou Windows.
- O módulo de Vendas depende do módulo de Estoque estar corretamente configurado (produtos cadastrados) antes de registrar qualquer venda.
- O módulo Financeiro depende dos módulos de Vendas e Estoque para gerar automaticamente lançamentos (contas a receber, custos).

## 3. Requisitos Específicos

### 3.1 Requisitos Funcionais

### 3.2 Requisitos Não Funcionais

### 3.3 Requisitos de Interface

## 4. Apêndices

Esta seção reúne materiais complementares ao documento principal, oferecendo informações de apoio que auxiliam na compreensão do sistema, de suas regras de negócio e da organização dos requisitos descritos nas seções anteriores.

### 4.1 Apêndice A - Hierarquia de Perfis de Acesso

O sistema adota um modelo de controle de acesso baseado em perfis hierárquicos. O quadro a seguir sintetiza os módulos acessíveis a cada perfil, servindo como referência consolidada para os requisitos de restrição distribuídos ao longo da seção 3.1.

TODO: tabela de acesso, baseado nos requisitos

Os campos preenchidos com "sim" indicam que o usuário tem acesso àquela funcionalidade, enquanto "não" o usuário não tem acesso.

### **4.2 Apêndice B – Regras de Cálculo**

Este apêndice apresenta as principais fórmulas utilizadas pelo Sistema de Recursos para o cálculo de valores relacionados às operações de estoque, vendas e finanças. As regras apresentadas devem ser consideradas na especificação e implementação dos requisitos funcionais correspondentes.

TODO: colocar as referencias aos requisitos

### 4.2.1 Cálculos de Vendas

#### 4.2.1.1 Subtotal de um item

O subtotal de cada produto refere-se ao valor de um certo produto baseado na quantidade.

> Subtotal_item = Quantidade × Preço Unitário

| Produto | Quantidade | Preço unitário | Subtotal |
| --- | --- | --- | --- |
| Produto A | 3 | R$ 20,00 | R$ 60,00 |
| Produto B | 2 | R$ 15,00 | R$ 30,00 |

#### 4.2.1.2 Valor total da venda

> Total da Venda = ∑ Subtotal_item

Exemplo de valor do produto A e B, seguindo a tabela acima:

> 60,00 R$ + 30,00 R$ = R$90,00

### 4.2.2 Cálculos de Estoque

#### 4.2.2.1 Estoque atual

O estoque atual representa a quantidade disponível em unidades de certo produto no momento atual.

> Estoque_Atual = Estoque_Inicial + Entradas − Saídas

#### 4.2.2.2 Verificação de estoque mínimo

O estoque mínimo é o valor em unidades de certo produto para que ele seja classificado como estoque baixo. Isso ocorre quando o estoque atual é menor ou igual ao estoque mínimo definido.

> Estoque_Atual ≤ Estoque_Mínimo

### 4.2.3 Cálculos Financeiros

#### 4.2.3.1 Saldo Financeiro Atual

O Saldo Financeiro Atual representa o valor real da disponibilidade de caixa. Nesse saldo, são consideradas apenas as despesas que já foram pagas.

> Saldo = Total de Receitas − Total de Despesas Pagas

#### 4.2.3.2 Saldo Financeiro Projetado

O Saldo Financeiro Projetado representa a estimativa da disponibilidade de caixa. Ele é calculado por meio da diferença entre as receitas totais e as receitas pagas e ainda não pagas.

> Saldo = Total de Receitas − (Total de Despesas Pagas + Total de Despesas Não Pagas)sera

## 5. Índice

### 5.1 Sumário

| Seção | Página |
| --- | --- |
| 1\. Introdução |  |
| 1.1 Propósito do Documento de Requisitos |  |
| 1.2 Escopo do Produto |  |
| 1.3 Definições, Acrônimos e Abreviações |  |
| 1.4 Referências |  |
| 1.5 Visão do Restante do Documento |  |
| 2\. Descrição Geral |  |
| 2.1 Perspectiva do Produto |  |
| 2.2 Funcionalidade do Produto |  |
| 2.2.1 Módulo de Estoque |  |
| 2.2.2 Módulo de Vendas |  |
| 2.2.3 Módulo Financeiro |  |
| 2.3 Características do Usuário |  |
| 2.4 Restrições Gerais |  |
| 2.5 Suposições e Dependências |  |
| 2.5.1 Suposições |  |
| 2.5.2 Dependências |  |
| 3\. Requisitos Específicos |  |
| 3.1 Requisitos Funcionais |  |
| 3.2 Requisitos Não Funcionais |  |
| 3.3 Requisitos de Interface |  |
| 4\. Apêndices |  |
| 4.1 Apêndice A – Hierarquia de Perfis de Acesso |  |
| 4.2 Apêndice B – Regras de Cálculo |  |
| 4.2.1 Cálculos de Vendas |  |
| 4.2.2 Cálculos de Estoque |  |
| 4.2.3 Cálculos Financeiros |  |
| 5\. Índice |  |

TODO: completar com o que for adicionado depois desse commit

### 5.2 Índice de Termos

| Termo | Página |
| --- | --- |
| Despesa |  |
| Estoque |  |
| Estoque mínimo |  |
| Fluxo de caixa |  |
| Login |  |
| Logout |  |
| Movimentação financeira |  |
| Produto |  |
| Receita |  |
| Saída |  |
| Saldo |  |
| Venda |  |
