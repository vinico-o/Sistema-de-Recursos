## 1\. Introdução

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
| :---- | :---- |
| **RF** | Requisito Funcional. Descreve uma funcionalidade ou comportamento que o sistema deve oferecer. |
| **RNF** | Requisito Não Funcional. Descreve uma característica de qualidade, restrição ou comportamento esperado do sistema. |
| **RG** | Restrição Geral. Define limitações ou condições que devem ser obrigatoriamente respeitadas pelo sistema. |
| **(E)** | Explícito ao usuário. Requisito cuja execução é visível e perceptível pelo usuário através da interface do sistema. |
| **(O)** | Oculto ao usuário. Requisito processado internamente pelo sistema, sem interação direta com o usuário. |
| **Estoque** | Conjunto de produtos e mercadorias armazenados pela empresa e disponíveis para comercialização ou utilização. |
| **Estoque mínimo** | Quantidade mínima de um produto que deve ser mantida em estoque para evitar sua falta. |
| **Produto** | Item comercializado ou armazenado pela empresa, possuindo informações como nome, categoria, preço e quantidade em estoque. |
| **Venda** | Operação comercial na qual um ou mais produtos são vendidos a um cliente. |
| **Receita** | Valor financeiro recebido ou a receber pela empresa, como resultado de vendas ou outras operações. |
| **Despesa** | Valor financeiro pago ou a pagar pela empresa para manutenção de suas atividades. |
| **Saldo** | Diferença entre o total de receitas e o total de despesas registradas no sistema em determinado período. |
| **Movimentação financeira** | Registro de uma operação que altera o fluxo financeiro da empresa, podendo representar uma receita ou despesa. |
| **SQA** | Software Quality Assurance (Garantia de Qualidade de Software). |
| **JVM** | Java Virtual Machine (Máquina Virtual Java). |
| **Login** | Processo pelo qual um usuário se autentica no sistema por meio de suas credenciais. |
| **Logout** | Processo pelo qual um usuário encerra sua sessão no sistema. |
| **ADM** | Administrador.Usuário com acesso total ao sistema. |
| **EST** | Estoquista. Usuário com acesso às funcinalidades de estoque. |
| **VEND** | Vendedor. Usuário com acesso às funcionalidades de vendas e financeiras. |
| **CRUD** | Operações com dados. C \- create (criar); R \- read (leitura); U \- update (atualizar); D \- delete (deletar). |

### 1.4 Referências

Não usamos referências.

### 1.5 Visão do restante do Documento

Esse documento está organizado em seções, cada uma responsável por descrever partes específicas do sistema proposto. São elas:

- Seção 2: Apresenta a descrição geral do sistema, indicando os aspectos principais, como perspectivas, funcionalidades, restrições, suposições e dependências do produto. Com isso é possível ter uma visão mais específica do objetivo da aplicação.  
- Seção 3: Descreve com maior detalhamento os requisitos do sistema, de como ele se comunicará com o mundo exterior, e lista as funções e recursos específicos. Com isso será possível ter uma visão geral e entender com mais clareza o funcionamento do sistema.  
- Seção 4: Acrescenta ao documento informações complementares que auxiliam o entendimento dos requisitos do sistema e do funcionamento geral do sistema.  
- Seção 5: Parte do documento que lista todas as seções presentes no documento, além de uma lista alfabética com os termos-chave, conceitos e siglas utilizados seguido da página em que aparecem.

## 2\. Descrição Geral

O Sistema de Recursos \- Gestão de Estoque, Vendas e Financeiro tem como objetivo auxiliar empresas no gerenciamento de seus produtos, vendas e operações financeiras. O sistema centraliza essas informações, permitindo o controle do estoque, o registro de vendas e o acompanhamento das movimentações financeiras.

### 2.1 Perspectiva do Produto

O Sistema de Recursos será desenvolvido como uma aplicação independente. Ele tem como objetivo auxiliar na organização e gerenciamento do estoque e vendas, como também acompanhar o desempenho financeiro da empresa.

O sistema será composto por módulos que compartilham informações entre si, sendo eles: Estoque, Vendas e Financeiro. Dessa forma, operações em um módulo poderá produzir alterações nos demais módulos.

O usuário interage com o sistema por meio de uma interface gráfica, desse modo, ele poderá executar as operações de cada um dos módulos.

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

- Registrar receitas e despesas;  
- Consultar movimentações financeiras;  
- Controlar pagamentos;  
- Consultar saldo;  
- Gerar relatórios financeiros.

### 2.3 Características do Usuário

O sistema possui três níveis diferentes de usuários, cada um deles com acessos à diferentes funcionalidades. São eles:

Administrador

- Acesso à todas as funcionalidades do sistema.  
- Gestão de usuários: Cadastro e exclusão.

Estoquista

- Gestão de Estoque: CRUD  
- Visualizar Saldo

Vendedor

- Compra de Produtos  
- Visualizar Relatório Financeiro  
- Venda de Produtos  
- Visualizar Saldo

Os usuários deverão possuir conhecimentos básicos de informática e estar familiarizados com as operações relacionadas à estoque, vendas e gestão financeira.

### 2.4 Restrições Gerais

RG01 \- O sistema deve ser desenvolvido em linguagem Java.

RG02 \- Todos os registros e informações do sistema devem ser armazenados de maneira permanente em um banco de dados relacional, a fim de garantir a existência e a integridade dos dados mesmo fora da execução do sistema.

RG03 \- O sistema deve ser executável em qualquer sistema operacional compatível com a JVM (Java Virtual Machine), incluindo Windows e Linux.

RG04 \- O sistema operará em modo de usuário único por sessão, sem suporte a acesso simultâneo de múltiplos usuários em uma única sessão.

RG05 \- O acesso ao sistema deve ser restrito a usuários autenticados por meio de login e senha. Nenhuma funcionalidade do sistema pode ser acessada sem autenticação prévia.

### 2.5 Suposições e Dependências

#### 2.5.1 Suposições

- Assume-se que os usuários do sistema possuem conhecimento básico de informática para operar o sistema.  
- Assume-se que o computador onde o sistema será executado possui Java instalado e configurado corretamente.  
- Assume-se que o sistema seja utilizado para apenas um comércio.

#### 2.5.2 Dependências

- O sistema depende da disponibilidade de um ambiente computacional capaz de executar aplicações desenvolvidas na linguagem Java, sendo necessários sistemas operacionais que suportam Máquina Virtual Java (JVM), como Linux ou Windows.  
- O módulo de Vendas depende do módulo de Estoque estar corretamente configurado (produtos cadastrados) antes de registrar qualquer venda.  
- O módulo Financeiro depende dos módulos de Vendas e Estoque para gerar automaticamente lançamentos (contas a receber, custos).

## 3 Requisitos Específicos

### 3.1 Requisitos Funcionais

#### 3.1.1 Autenticação

**RF01 – Primeiro usuário:** o sistema deve cadastrar automaticamente um Administrador com nome de usuário "admin" e senha "admin". (O)

**RF02 – Autenticar usuário:** o sistema deve permitir que o usuário informe o nome de usuário e senha para acessar o sistema, bloqueando qualquer funcionalidade enquanto a autenticação não for concluída com sucesso. (E)

- **RF02.1 – Restringir acesso por nível de permissão:** o sistema deve exibir apenas as funcionalidades compatíveis com o nível do usuário autenticado (ADM, EST ou VEND). (O)  
    
- **RF02.2 – Exibir mensagem de erro de autenticação:** o sistema deve exibir mensagem de erro informando que o login ou a senha estão incorretos, caso as informações de login não sejam encontradas. (E)

**RF03 – Encerrar sessão:** o sistema deve permitir que o usuário autenticado encerre sua sessão a qualquer momento, retornando à tela de login. (E)

- **RF03.1 – Confirmar encerramento de sessão:** o sistema deve exibir mensagem de confirmação antes de encerrar a sessão. (E)  
    
- **RF03.2 – Invalidar dados da sessão encerrada:** o sistema deve impedir qualquer acesso às funcionalidades protegidas sem nova autenticação. (O)

#### 3.1.2 Gestão de Usuários

**RF04 – Cadastrar usuário:** o sistema deve permitir o cadastro de novos usuários. (E)

- **RF04.1 – Restrição cadastro de usuário:** somente o Administrador pode cadastrar usuários. (O)  
    
- **RF04.2 – Validar unicidade de nome de usuário:** no momento do cadastro, o sistema deve verificar se o nome de usuário já existe. (O)  
    
  - **RF04.2.1 – Exibir mensagem de erro de nome duplicado:** o sistema deve apresentar mensagem de erro caso o nome de usuário já exista. (E)


- **RF04.3 – Informações de cadastro:** o sistema deve conter as seguintes informações de usuário: (E)  
    
  - Nome de usuário;  
  - Senha;  
  - Nível de usuário;

**RF05 – Editar informações de usuário:** o sistema deve permitir editar as informações de um usuário já cadastrado. (E)

- **RF05.1 – Restrição de edição de usuário:** o sistema deve permitir somente o próprio usuário autenticado editar suas próprias informações de usuário. (O)

**RF06 – Excluir usuário:** o sistema deve permitir excluir o registro de um usuário após confirmação da operação. (E)

- **RF06.1 – Restrição de exclusão de usuário:** somente o Administrador pode excluir usuários. (O)  
    
- **RF06.2 – Impedir auto exclusão:** o sistema deve bloquear a tentativa de um usuário excluir sua própria conta enquanto estiver autenticado. (O)

**RF07 – Listar usuários:** o sistema deve permitir a visualização de todos os usuários registrados com suas informações básicas em formato de tabela. (E)

- **RF07.1 – Listagem automática:** o sistema deve listar automaticamente ao entrar na aba de usuários. (E)

**RF08 – Buscar usuário:** o sistema deve permitir localizar um usuário específico na listagem através do nome do usuário. (E)

#### 3.1.3 Gestão de Estoque

**RF09 \- Cadastrar produtos:** o sistema deve permitir o cadastro de produtos no catálogo. (E)

- **RF09.1 – Validar unicidade do produto:** o sistema deve verificar se já existe um produto com o mesmo cadastro. (O)  
    
  - **RF09.1.1 – Exibir mensagem de erro de produto duplicado:** o sistema deve apresentar mensagem de erro se o produto já estiver cadastrado. (E)


- **RF09.2 – Informações de cadastro:** o sistema deve conter as seguintes informações de produto: (E)  
    
  - Nome do produto;  
  - Código do produto;  
  - Preço do produto;  
  - Quantidade;  
  - Unidade de medida;  
  - Categoria;  
  - Quantidade mínima de estoque;


- **RF09.2.1 \- Unidades de medida:** as unidades de medida dos produtos podem ser: UN (unidade), CX (caixa), KG (quilograma), PCT (pacote) ou L (litro). (E)  
    
- **RF09.2.2 \- Cadastro de Categorias:** O sistema deve permitir o cadastro de categorias. (E)  
    
  - **RF09.2.2.1 \- Exibir Categorias durante cadastro de Produto:** o sistema deve exibir as categorias cadastradas durante o cadastro de produtos. (E)  
      
  - **RF09.2.2.2 \- Edição de categoria:** o sistema deve permitir a edição de categorias. (E)  
      
    - **RF09.2.2.2.1 \- Restrição de edição de categoria:** o sistema deve permitir somente o Administrador editar categorias. (O)

    

  - **RF09.2.2.3 \- Exclusão de categoria:** o sistema deve permitir a exclusão de categorias. (E)  
      
    - **RF09.2.2.3.1 \- Restrição de exclusão de categoria:** o sistema deve permitir somente o Administrador excluir categorias. (O)


- **RF09.3 \- Restrição de cadastro de produtos:** o sistema deve permitir somente o Administrador e Estoquista cadastrar produtos no catálogo. (O)

**RF10 – Editar produto:** o sistema deve permitir editar as informações de um produto já cadastrado. (E)

- **RF10.1 \- Restrição de edição de produto:** o sistema deve permitir somente o Administrador e Estoquista editar produtos do catálogo. (O)  
    
- **RF10.2 \- Informações passíveis de edição:** o sistema deve permitir a edição das seguintes informações do produto: (E)  
    
  - Nome do produto;  
  - Preço do produto;  
  - Código do produto;  
  - Unidade de medida;  
  - Categoria;  
  - Quantidade mínima de estoque;

**RF11 – Excluir produto:** o sistema deve permitir excluir o cadastro de um produto. (E)

- **RF11.1 \- Restrição de exclusão de produto:** o sistema deve permitir somente o Administrador e Estoquista excluir produtos do catálogo. (O)  
    
- **RF11.2 \- Impedir exclusão de produto com estoque:** o sistema deve impedir a exclusão de um produto caso haja estoque disponível. (E)  
    
- **RF11.3 \- Exigir confirmação de exclusão:** o sistema deve exigir confirmação explícita antes de concluir a operação.  
    
- **RF11.4 \- Remoção completa do produto:** o sistema deve remover todos os dados vinculados ao produto. (E)

**RF12 – Listar produtos:** o sistema deve exibir todos os produtos cadastrados com suas informações básicas em formato de tabela. (E)

- **RF12.1 Listagem automática:** o sistema deve listar automaticamente ao entrar na aba de catálogo. (E)

**RF13 – Buscar produtos:** o sistema deve permitir buscar produtos por meio do nome. (E)

- **RF13.1 \- Exibir informações do produto:** o sistema deve permitir exibir as informações do produto, caso encontrado. (E)

**RF14 \- Listar produtos com baixa quantidade**: o sistema deve exibir todos os produtos em que a quantidade é menor que a quantidade mínima. (E)

**RF15 \- Diminuir quantidade dos produtos por meio da venda**: o sistema deve diminuir a quantidade dos produtos vendidos automaticamente. (O)

#### 3.1.4 Gestão de Finanças

**RF16 – Gerar relatório de despesas:** o sistema deve gerar relatório de despesas exibindo o total gasto com representação gráfica. (E)

- **RF16.1 – Filtrar relatório de despesas por período:** o sistema deve gerar gráfico de linha, possibilitando definir intervalo de datas para o relatório, exibindo apenas lançamentos dentro do período informado. (E)  
    
- **RF16.2 – Filtrar relatório de despesas por categoria:** o sistema deve gerar gráfico de pizza, permitindo selecionar uma ou mais categorias para filtrar o relatório de despesas, exibindo apenas os lançamentos das categorias selecionadas. (E)  
    
- **RF16.3 \- Restrição de geração de relatório:** somente o Administrador e Vendedor podem gerar relatórios de despesa. (O)

**RF17 – Gerar relatório de receitas:** o sistema deve gerar relatório de receitas exibindo o total recebido com representação gráfica. (E)

- **RF17.1 – Filtrar relatório de receitas por período:** o sistema deve gerar gráfico de linha, possibilitando definir intervalo de datas para o relatório, exibindo apenas lançamentos dentro do período informado. (E)  
    
- **RF17.2 – Filtrar relatório de receitas por categoria:** o sistema deve gerar gráfico de pizza, permitindo selecionar uma ou mais categorias para filtrar o relatório de receitas, exibindo apenas os lançamentos das categorias selecionadas. (E)  
    
- **RF17.3 \- Restrição de geração de relatório:** somente o Administrador e Vendedor podem gerar relatórios de receita. (O)

**RF18 – Gerar relatório financeiro geral:** o sistema deve gerar relatório consolidado com total de receitas, total de despesas, saldo resultante e representação gráfica da evolução do saldo ao longo de um período. (E)

- **RF18.1 – Filtrar relatório financeiro por período:** o sistema deve gerar gráfico de linha, possibilitando definir intervalo de datas, calculando receitas, despesas e saldo apenas dentro do período selecionado. (E)  
    
- **RF18.2 \- Restrição de geração de relatório:** somente o Administrador e Vendedor podem gerar relatórios de finanças. (O)

**RF19 – Calcular saldo financeiro:** o sistema deve calcular automaticamente o saldo financeiro após cada operação que envolva receita ou despesa, sem necessidade de intervenção do usuário. (O)

- **RF19.1 – Exibição de saldo:** o sistema deve exibir o saldo financeiro em sua tela inicial. (E)

#### 3.1.5 Gestão de Compras de Produtos

**RF20 – Registrar compra:** o sistema deve permitir registrar compras de produtos. (E)

- **RF20.1 – Selecionar produto(s):** o sistema deve exigir a seleção do produto(s) do catálogo. (E)  
    
- **RF20.2 – Validar dados da compra:** o sistema deve validar as informações dos registros de compra. (O)  
    
  - **RF20.2.1 – Erro no registro de compra:** o sistema deve exibir uma mensagem de erro em caso de inconsistência no registro de compra. (E)  
      
  - **RF20.2.2 \- Contas pendentes:** o sistema deve persistir todas as contas a serem pagas. As informações referentes a cada conta persistida são: (E)  
      
    - Data;  
    - Valor;  
    - Status de pagamento da conta;

    

  - **RF20.2.3 \- Pagamento de conta:** quando a conta for paga, o status dela deve ser alterado para “paga”. Além disso, o saldo deve ser recalculado. (E)  
      
  - **RF20.2.4 \- Listar contas:** o sistema deve permitir a visualização de todas as contas registradas com suas informações básicas em formato de tabela. (E)  
      
    - **RF20.2.4.1 \- Listagem automática:** o sistema deve listar automaticamente ao entrar na aba de contas. (E)  
    - **RF20.2.4.2 \- Filtro por status de conta:** o sistema deve permitir filtrar a listagem por contas pagas e não pagas. (E)


- **RF20.3 – Informações de compra:** o sistema deve conter as seguintes informações da compra: (E)  
    
  - Nome dos produtos comprados;  
  - Código de cada produto comprado;  
  - Quantidade de cada produto comprado;  
  - Preço total.  
  - Data da compra;


- **RF20.4 – Recalcular saldo após registro de compra:** o sistema deve recalcular automaticamente o saldo ao registrar uma compra. (O)  
    
- **RF20.5 \- Aumento da quantidade de produtos:** o sistema deve aumentar a quantidade dos produtos que forem comprados, realizando uma edição automática do produto. (O)  
    
- **RF20.6 \- Restrição de registro de compra:** o sistema deve permitir somente o Administrador e Vendedor registrarem compras de produtos. (O)

**RF21 – Listar compras:** o sistema deve permitir a visualização de todas as compras registradas com suas informações básicas em formato de tabela. (E)

- **RF21.1 – Filtrar compras por período:** o sistema deve permitir filtrar as compras de acordo com o período informado pelo usuário. (E)  
    
- **RF21.2 – Filtrar compras por produto:** o sistema deve permitir filtrar as compras de acordo com o produto comprado. (E)  
    
- **RF21.3 Listagem automática:** o sistema deve listar automaticamente ao entrar na aba de compras. (E)

#### 3.1.6 Gestão de Vendas de Produtos

**RF22 – Registrar venda:** o sistema deve permitir registrar vendas de produtos. (E)

- **RF22.1 – Selecionar produto(s):** o sistema deve exigir a seleção de um ou mais produtos do catálogo. (E)  
    
- **RF22.2 – Validar dados da venda:** o sistema deve validar as informações dos registros de venda. (O)  
    
  - **RF22.2.1 – Erro no registro de venda:** o sistema deve exibir uma mensagem de erro em caso de inconsistência no registro de venda. (E)  
      
  - **RF22.2.2 \- Quantidade insuficiente de produto:** caso o sistema identifique que não há a quantidade desejada de determinado produto no estoque, uma mensagem deve ser exibida indicando que não é possível realizar a venda. (E)


- **RF22.3 – Informações de venda:** o sistema deve conter as seguintes informações da venda: (E)  
    
  - Nome dos produtos vendidos;  
  - Código de cada produto vendido;  
  - Quantidade de cada produto vendido;  
  - Preço total;


- **RF22.3.1 – Cálculo do preço total:** o sistema deve calcular automaticamente o preço total da venda usando os preços unitários de cada produto vendido. (O)  
    
- **RF22.4 – Recalcular saldo após registro de venda:** o sistema deve recalcular automaticamente o saldo ao registrar uma venda. (O)  
    
- **RF22.5 \- Diminuição da quantidade de produtos:** o sistema deve diminuir a quantidade dos produtos que forem vendidos, realizando uma edição automática do produto. (O)  
    
- **RF22.6 \- Restrição de registro de venda:** o sistema deve permitir somente o Administrador e Vendedor registrarem vendas. (O)  
    
- **RF22.7 \- Exibição de informações de venda:** o sistema deve mostrar os produtos da venda, a quantidade de cada produto, o valor do subtotal de cada produto e o valor final antes da confirmação da venda. (E)  
    
- **RF22.8 \- Confirmação de venda:** o sistema deve mostrar uma aba para confirmação de venda. (E)

**RF23 – Listar vendas:** o sistema deve permitir a visualização de todas as vendas registradas com suas informações básicas em formato de tabela. (E)

- **RF23.1 – Filtrar vendas por período:** o sistema deve permitir filtrar as vendas de acordo com o período informado pelo usuário. (E)  
    
- **RF23.2 – Filtrar vendas por produto:** o sistema deve permitir filtrar as vendas de acordo com o produto comprado. (E)  
    
- **RF23.3 Listagem automática:** o sistema deve listar automaticamente ao entrar na aba de vendas. (E)

### 3.2 Requisitos Não Funcionais

Os requisitos não funcionais descrevem as características de qualidade que o sistema deve apresentar, independentemente das funcionalidades específicas. Eles abrangem aspectos de desempenho, usabilidade, confiabilidade, segurança, portabilidade e manutenibilidade do software.

#### 3.2.1 Desempenho

**RNF01 – Tempo de resposta para operações comuns:** o sistema deve responder a operações básicas em no máximo 4 (quatro) segundos. (O)

**RNF02 – Tempo de resposta para geração de relatórios:** o sistema deve gerar e exibir qualquer relatório solicitado em no máximo 5 (cinco) segundos. (O)

**RNF03 – Desempenho consistente com crescimento de dados:** o sistema não deve apresentar degradação perceptível de desempenho à medida que o volume de dados cresce, mantendo tempos de resposta aceitáveis para listagens, buscas e relatórios. (O)

#### 3.2.2 Usabilidade

**RNF04 – Interface intuitiva:** o sistema deve ter a interface organizada de forma clara e consistente, permitindo que um usuário com conhecimento básico de informática realize as operações principais. (E)

**RNF05 – Mensagens de erro claras:** o sistema deve exibir mensagens de erro em linguagem simples e objetiva, indicando o que ocorreu e o que o usuário deve fazer para corrigir o problema. (E)

**RNF06 – Confirmação de operações irreversíveis:** o sistema deve solicitar confirmação explícita antes de executar operações irreversíveis, como exclusões de registros. (E)

**RNF07 – Consistência visual da interface:** a interface deve manter padrões visuais consistentes em todas as telas — posicionamento de botões, cores de ação e vocabulário. (E)

**RNF08 – Interface com linguagem simples:** toda a interface deve estar escrita em português brasileiro, sem mistura de idiomas ou termos técnicos sem tradução. (E)

#### 3.2.3 Confiabilidade

**RNF09 – Garantia de persistência de operações confirmadas:** qualquer operação confirmada pelo usuário deve ser gravada no banco de dados antes de ser considerada concluída. (O)

**RNF10 – Consistência do saldo financeiro:** o saldo financeiro exibido deve estar sempre consistente com o conjunto de receitas e despesas registradas. (O)

**RNF11 – Tratamento de erros internos:** o sistema deve tratar internamente todas as exceções não esperadas de entrada de dados, exibindo uma mensagem de erro ao usuário. (O)

#### 3.2.4 Portabilidade

**RNF12 – Compatibilidade com múltiplos sistemas operacionais:** o sistema deve ser executável em sistemas operacionais como Windows e Linux. (O)

### **3.3 Requisitos de Interface**

Os requisitos de interface descrevem as características das interações entre o sistema e os agentes externos com os quais ele se relaciona, incluindo os usuários humanos, o hardware subjacente, os softwares do ambiente de execução e os mecanismos de comunicação de dados.

#### **3.3.1 Interface de Usuário**

Esta subseção descreve os requisitos relacionados à estrutura visual, navegação, formulários e padrões de interação que o sistema deve apresentar ao usuário.

**RI01 – Formulários de cadastro e edição:** o sistema deve apresentar formulários organizados para todas as operações de cadastro e edição, controles de ação distintos para confirmar ou cancelar a operação. (E)

- **RI01.1 – Exibir mensagens de validação inline:** o sistema deve exibir mensagens de erro de validação ao lado ou abaixo do campo que originou o problema, sem redirecionar o usuário para outra tela. (E)  
    
- **RI01.2 – Preservar dados preenchidos após erro de validação:** o sistema deve manter os dados que já foram preenchidos e informar somente qual campo está incorreto. (E)

**RI02 – Telas de listagem:** o sistema deve apresentar os registros cadastrados em formato tabular, contendo colunas com as informações principais de cada item. (E)

- **RI02.1 – Exibir campo de busca nas listagens:** o sistema deve disponibilizar, em todas as telas de listagem, um campo de busca que permita localizar registros específicos. (E)  
    
- **RI02.2 – Exibir mensagem de lista vazia:** quando não houver registros, o sistema deve apresentar uma mensagem indicando a ausência de dados. (E)

**RI03 – Diálogos de confirmação:** o sistema deve apresentar janelas de confirmação antes de executar operações irreversíveis. (E)

- **RI03.1 – Bloquear interação com o restante da interface durante o diálogo:** o sistema deve impedir qualquer interação do usuário com as demais áreas da interface, quando uma janela de diálogo estiver aberta. (O)

**RI04 – Mensagens de feedback de operação:** o sistema deve exibir mensagens de retorno ao usuário após a conclusão de operações. (E)

- **RI04.1 – Diferenciar mensagens de sucesso e de erro visualmente:** o sistema deve utilizar elementos visuais distintos para mensagens de sucesso e de erro. (E)

**RI05 – Telas de relatório:** o sistema deve apresentar os relatórios gerados em tela dedicada, com as informações específicas daquele relatório. (E)

- **RI05.1 – Exibir filtros de relatório em área dedicada:** o sistema deve apresentar os filtros disponíveis para cada relatório. (E)

**RI06 – Padrão visual consistente:** o sistema deve manter padronização visual uniforme em todas as telas. (E)

**RI07 – Exibir saldo atual na tela principal:** o sistema deve exibir o saldo financeiro atual na tela principal. (E)

#### **3.3.2 Interface com Hardware**

Esta subseção descreve os requisitos relacionados às interações entre o sistema e os dispositivos físicos do ambiente de execução.

**RI08 – Dispositivos de entrada:** o sistema deve suportar a entrada de dados exclusivamente por meio dos dispositivos de entrada teclado e mouse. (O)

**RI09 – Requisitos de exibição:** o sistema deve ser executável e utilizável em monitores com resolução mínima de 1024x768 pixels. (O)

**RI10 – Ausência de dependência de hardware especializado:** o sistema não requer quaisquer outros periféricos além dos dispositivos de entrada e saída padrão. (O)

#### **3.3.3 Interface com Software Externo**

Esta subseção descreve os requisitos relacionados à interação do sistema com outros softwares presentes no ambiente de execução, incluindo o sistema operacional, o banco de dados e eventuais integrações com aplicações de terceiros.

**RI11 – Interface com o sistema operacional:** o sistema deve interagir com o sistema operacional hospedeiro exclusivamente por meio da JVM (Java Virtual Machine). (O)

**RI12 – Interface com o banco de dados relacional:** o sistema deve se comunicar com o banco de dados relacional. (O)

- **RI12.1 – Encerrar conexões com o banco de dados após cada operação:** o sistema deve garantir que as conexões abertas com o banco de dados sejam encerradas ao término de cada operação. (O)

**RI13 – Ausência de integração com sistemas externos:** o sistema não realiza integração com APIs externas, de pagamentos, de emissão de Nota Fiscal ou de autenticação. (O)

#### **3.3.4 Interface de Comunicação**

Esta subseção descreve os requisitos relacionados aos mecanismos de troca de dados adotados pelo sistema, incluindo a comunicação interna com o banco de dados e os formatos de exportação e importação de informações.

**RI14 – Comunicação local com o banco de dados:** toda a troca de dados entre o sistema e o banco de dados relacional deve ocorrer localmente. (O)

**RI15 – Ausência de protocolos de comunicação em rede:** o sistema não depende de protocolos de comunicação em rede. (O)

## 4\. Apêndices

Esta seção reúne materiais complementares ao documento principal, oferecendo informações de apoio que auxiliam na compreensão do sistema, de suas regras de negócio e da organização dos requisitos descritos nas seções anteriores.

### 4.1 Apêndice A \- Hierarquia de Perfis de Acesso

O sistema adota um modelo de controle de acesso baseado em perfis hierárquicos. O quadro a seguir sintetiza os módulos acessíveis a cada perfil, servindo como referência consolidada para os requisitos de restrição distribuídos ao longo da seção 3.1.

| Funcionalidade | ADM | EST | VEND |
| :---- | :---- | :---- | :---- |
| Autenticação e Sessão | sim | sim | sim |
| Criação e Exclusão de Usuários | sim | não | não |
| Edição de Usuário | sim | sim | sim |
| Gestão de Estoque (CRUD) | sim | sim | não |
| Compra de Produtos | sim | não | sim |
| Venda de Produtos | sim | não | sim |
| Visualizar Relatório Financeiro | sim | não | sim |
| Visualizar Saldo Financeiro | sim | sim | sim |

Os campos preenchidos com "sim" indicam que o usuário tem acesso àquela funcionalidade, enquanto "não" o usuário não tem acesso.

### **4.2 Apêndice B – Regras de Cálculo**

Este apêndice apresenta as principais fórmulas utilizadas pelo Sistema de Recursos para o cálculo de valores relacionados às operações de estoque, vendas e finanças. As regras apresentadas devem ser consideradas na especificação e implementação dos requisitos funcionais correspondentes.

### 4.2.1 Cálculos de Vendas

#### 4.2.1.1 Subtotal de um item

O subtotal de cada produto refere-se ao valor de um certo produto baseado na quantidade.

> Subtotal\_item \= Quantidade × Preço Unitário

| Produto | Quantidade | Preço unitário | Subtotal |
| :---- | :---- | :---- | :---- |
| Produto A | 3 | R$ 20,00 | R$ 60,00 |
| Produto B | 2 | R$ 15,00 | R$ 30,00 |

#### 4.2.1.2 Valor total da venda

> Total da Venda \= ∑ Subtotal\_item

Exemplo de valor do produto A e B, seguindo a tabela acima:

> 60,00 R$ \+ 30,00 R$ \= R$90,00

### 4.2.2 Cálculos de Estoque

#### 4.2.2.1 Estoque atual

O estoque atual representa a quantidade disponível em unidades de certo produto no momento atual.

> Estoque\_Atual \= Estoque\_Inicial \+ Entradas − Saídas

#### 4.2.2.2 Verificação de estoque mínimo

O estoque mínimo é o valor em unidades de certo produto para que ele seja classificado como estoque baixo. Isso ocorre quando o estoque atual é menor ou igual ao estoque mínimo definido.

> Estoque\_Atual ≤ Estoque\_Mínimo

### 4.2.3 Cálculos Financeiros

#### 4.2.3.1 Saldo Financeiro Atual

O Saldo Financeiro Atual representa o valor real da disponibilidade de caixa. Nesse saldo, são consideradas apenas as despesas que já foram pagas.

> Saldo \= Total de Receitas − Total de Despesas Pagas

#### 4.2.3.2 Saldo Financeiro Projetado

O Saldo Financeiro Projetado representa a estimativa da disponibilidade de caixa. Ele é calculado por meio da diferença entre as receitas totais e as receitas pagas e ainda não pagas.

> Saldo \= Total de Receitas − (Total de Despesas Pagas \+ Total de Despesas Não Pagas)

## 5\. Índice

### 5.1 Sumário

| Seção | Página |
| :---- | :---- |
| 1\. Introdução | 1 |
| 1.1 Propósito do Documento de Requisitos | 1 |
| 1.2 Escopo do Produto | 1 |
| 1.3 Definições, Acrônimos e Abreviações | 1 |
| 1.4 Referências | 3 |
| 1.5 Visão do Restante do Documento | 3 |
| 2\. Descrição Geral | 4 |
| 2.1 Perspectiva do Produto | 4 |
| 2.2 Funcionalidade do Produto | 4 |
| 2.2.1 Módulo de Estoque | 4 |
| 2.2.2 Módulo de Vendas | 5 |
| 2.2.3 Módulo Financeiro | 5 |
| 2.3 Características do Usuário | 5 |
| 2.4 Restrições Gerais | 6 |
| 2.5 Suposições e Dependências | 6 |
| 2.5.1 Suposições | 6 |
| 2.5.2 Dependências | 6 |
| 3\. Requisitos Específicos | 7 |
| 3.1 Requisitos Funcionais | 7 |
| 3.1.1 Autenticação | 7 |
| 3.1.2 Gestão de Usuários | 7 |
| 3.1.3 Gestão de Estoque | 8 |
| 3.1.4 Gestão de Finanças | 11 |
| 3.1.5 Gestão de Compras de Produtos | 12 |
| 3.1.6 Gestão de Vendas de Produtos | 13 |
| 3.2 Requisitos Não Funcionais | 15 |
| 3.2.1 Desempenho | 15 |
| 3.2.2 Usabilidade | 15 |
| 3.2.3 Confiabilidade | 15 |
| 3.2.4 Portabilidade | 16 |
| 3.3 Requisitos de Interface | 16 |
| 3.3.1 Interface de Usuário | 16 |
| 3.3.2 Interface com Hardware | 17 |
| 3.3.3 Interface com Software Externo | 18 |
| 3.3.4 Interface de Comunicação | 18 |
| 4\. Apêndices | 18 |
| 4.1 Apêndice A – Hierarquia de Perfis de Acesso | 18 |
| 4.2 Apêndice B – Regras de Cálculo | 19 |
| 4.2.1 Cálculos de Vendas | 19 |
| 4.2.2 Cálculos de Estoque | 20 |
| 4.2.3 Cálculos Financeiros | 20 |
| 5\. Índice | 21 |

### 5.2 Índice de Termos

| Termo | Página |
| :---- | :---- |
| Administrador | 3 |
| Autenticação | 1 |
| Catálogo | 1 |
| Categoria | 2 |
| Compra | 1 |
| Conta | 6 |
| CRUD | 3 |
| Despesa | 2 |
| Estoque | 1 |
| Estoque mínimo | 2 |
| Estoquista | 3 |
| Login | 2 |
| Logout | 2 |
| Módulo | 3 |
| Movimentação financeira | 3 |
| Produto | 1 |
| Receita | 2 |
| Relatório financeiro | 5 |
| Saldo | 2 |
| Senha | 5 |
| Sessão | 2 |
| Unidade de medida | 9 |
| Usuário | 1 |
| Venda | 1 |
| Vendedor | 3 |