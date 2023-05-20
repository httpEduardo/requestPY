<p align="center">
   <a href="https://aiqfome.com/" rel="noopener" target="_blank"><img width="150" src="https://www.suafranquia.com/views/sources/images /franquias/logos/271b399b0a004c781779ec805e8d7ab7.png" alt="aiqfome logo"></a></p>
</p>

<h1 align="center">requestPY</h1>

<p align="">requestPY Uma estrutura para validar o json da solicitação/resposta e criar documentação para aplicativos mantidos pelos desenvolvedores do <a href="https://aiqfome.com/">aplicativo mais ganancioso da internet </a>!</p>

<p align="center">
   <a href="https://github.com/aiqfome" style="text-decoration:none" target="_blank">
     <img alt="Feito por VOID" src="https://img.shields.io/badge/made%20by-HttpEduardo-blueviolet">
   </a>
</p>

---

### Instalar com pip3

`pip3 instalar requestPY`

### Init na pasta do projeto

`requestPY --init`

Será criada a pasta **data_scructures_io** e **static**.

No **data_scructures_io**, estão os arquivos json para testar a requisição. [Exemplo](https://github.com/aiqfome/requestPY-example/blob/master/data_structures_io/transfers.json)

Estamos usando [Cerberus](https://docs.python-cerberus.org/en/stable/) para validar a estrutura. Portanto, se algum válido na resposta json for um nome, digite ou não envie. Ocorrerá uma exceção nos testes.

Na pasta **static**, estará o arquivo json para [Swagger](https://swagger.io), com este arquivo você pode fazer qualquer pacote em qualquer idioma que você queira ler.
Este swagger.json é gerado, então toda vez que você executar o comando `requestPY -g` na pasta este arquivo será atualizado.

### O arquivo _.requestPY.config_

Este arquivo json é para configuração, então as pastas de nomes e outras coisas podem ser personalizáveis.

#### docs_url
com o comando `requestPY --docs` será ativado um servidor flask na porta 3000 e lerá o arquivo swagger, este valor é para o qual a url será executada. **_padrão: localhost:3000/docs_**

#### save_file_swagger
O arquivo de nome gerado para swagger. **_padrão: swagger.json_**

#### data_structures_folder
A pasta de nomes que são as estruturas de dados para solicitações. **_padrão: data_structures_io_**

#### pasta_testes
O nome da pasta que serão os testes. **_padrão: testes_**

####tests_before_cmd
Às vezes, no projeto, queremos executar o comando/script antes de iniciar os testes, por exemplo, criar as tabelas no bd. Irá executar este comando antes de iniciar os testes.

####tests_between_cmd
Este comando é para rodar entre testes, no **tearDown**, então **após** rodar um teste, isso é para um script ou migration que você quer rodar para limpar o bd por exemplo.
