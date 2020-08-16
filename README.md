# MEETUP - QLIK
Casas Da Agua

Repositório do Código Fonte
=============================

## RAILEN CONSULTORIA - DISCOVERY NEGÓCIOS


### O que é este Projeto ?

* Criado este projeto para que todos os códigos fonte dos modelos de dados sejam centralizados em um único local

* Qualquer desenvolvedor pode ter acesso , com senha, a este repositório, tendo somente que clonar e depois comitar para que esteja disponível sempre a última versão do código.

* Devido a quantidade de arquivos de projeto a estruturação dos diretórios será feita de acordo com o que já foi estabelecido anteriormente no Projeto sendo que:

Diretório Raiz

--Nome da Pasta

---1.Config          ##Contendo arquivos de configuração ) 

---2.Dados Arquivos  ##Contendo arquivos necessários para a extração  

---3.QVD             ##Pasta contendo todos os dados extraídos

---4.Fonte

----4.1              ##Nome da Aplicação

-----000             ##Começar sempre com 000  + Nome da Sessão Interna, separar por assunto dentro da sessão.

----4.X              ##Nome da Aplicação


### Convenções
- Todo projeto QlikSense, possui uma pasta chamada Main, por isso, todo diretório possui um arquivo chamado Main.qss

- Todo projeto QlikSense  também possui uma **Seção - Biblioteca de Funções**, que contém comandos comuns em todas as aplicações, que pode mudada por aplicação, entretanto, existe um arquivo em 1.Config -> biblioteca_de_funcoes.qss que deve ser atualizado, caso sejam criadas novas funções em comum nas aplicações.

- No arquivo Main.qss, devem constar **TODAS** as chamadas para os outros arquivos, senão incorrerão em erro de leitura

- Todo arquivo deve ser salvo como **UTF-O WITH BOM**, senão o QlikSense não Lê os caracteres especiais.

- Existe uma arquivos README.md para cada pasta, onde devem ser colocados os comentários dos códigos.

- Ao criar uma nova APP no Sense, favor EXCLUIR as variáveis padrões e colocar o include do arquivo Main.qss (caso já esteja criado).



## TABELAS DO SISTEMA

### Informações Importantes
**CES** -> Estoque
**VEN** -> Vendas
**CRE** -> Clientes -> Contas a Receber
**FAP** -> Fornecedores -> Contas a Pagar
**CHP** -> Cheques

### Campos das Tabelas
- Códigos chave geralmente inicial com *CD*

### Tratamento
- O Padrão para utilização de chaves é _KEY_XXXXXX_

### Convenções do SQL

- Caso o projeto contenha um comando SQL em específico, caso encontre um caso semelhante ao abaixo *PAR.Pagamento->TipoPagamento*, isto sinifica que é uma referência ao OBJETO do banco e não a uma coluna do banco de dados

### Cargas Incrementais
- VENNota_Produtos
- VENCupom_Produtos
- VENDevolucaoProduto


## CDA_CodigoFonte
C:\cda_qliksense\trunk\4.Fonte\

## CDA_Config
C:\cda_qliksense\trunk\1.Config\

## Config
C:\Producao\1.Config\

## DadosArquivos
C:\Producao\2.Dados Arquivos\

## DataCloud
C:\Producao\3.QVD\Datacloud\

## Extraido_DELTACON
C:\Producao\3.QVD\extraido_deltacon\

## Extraido_QUESTOR
C:\Producao\3.QVD\extraido_questor\

## Extraido_VETORH
C:\Producao\3.QVD\extraido_vetorh\

## Folder Dados
C:\ETL\Dados\

## Folder QVDs
C:\ETL\QVDs\



## REVISÕES

**2020-02-24** Rafael Encinas
- Nomes Amigáveis - As extrações de dados estão com nomes que somente quem criou sabe identificar, é necessário modificar.
- Trocar todas as gravações pela Sub de Gravação ( Call GravaLimpaMemoria('Nome da Tabela','Caminho e Nome do Arquivo.qvd'); )
