# Boas-vindas ao repositório do projeto Car Shop!

### Interface `IModel` genérica

Crie a interface `IModel`, que será usada para a conexão com o banco de dados. Ela deverá ter, pelo menos, as funções `create()`, `read()`, `readOne()`, `update()` e `delete()`.

Por ser genérica, nossa interface deverá receber um tipo `T` qualquer, e ela deve esperar, em cada função, as seguintes especificações:
 - `create()`: deve receber um objeto do tipo `T`e retornar uma Promise do tipo `T`.
 - `read()`: deve retornar uma Promise contendo um array de objetos do tipo `T`.
 - `readOne()`: deve receber uma string e retornar uma Promise do tipo `T` ou nula.
 - `update()`: deve receber uma string e um objeto do tipo `T` e retornar uma Promise do tipo `T` ou nula.
 - `delete()`: deve receber uma string e retornar uma Promise do tipo `T` ou nula.
 - O arquivo deve ficar no diretório `/src/interfaces/` e  ter o nome de `IModel.ts`.
 - A interface deve ser exportada com o nome de `IModel` e não deve ser exportada de forma padrão.

### Interface `IVehicle` genérica

A interface `IVehicle` que será usada para criarmos nossos tipos de carro, moto e caminhão.
Ela deverá ter todos os atributos comuns de todos os veículos que listaremos aqui. São eles:

 | Atributo | Descrição |
 | :-------: | :-------- |
 | `model`   | Marca e/ou modelo do veículo. Deve ser uma string com, pelo menos, 3 caracteres |
 | `year`    | Ano de fabricação do veículo. Deve ser um valor inteiro positivo maior ou igual a 1900, porém menor ou igual a 2022 |
 | `color`   | Cor principal do veículo. Deve ser uma string com, pelo menos, 3 caracteres |
 | `status`  | Status que define se um veículo pode ou não ser comprado. Deve receber valores booleanos e deve ser opcional |
 | `buyValue` | Valor de compra do veículo. Deve receber apenas números inteiros |

### Interface `ICar` a partir da interface `IVehicle`

A interface `ICar` de modo que ela possua todos os atributos da interface `IVehicle` e, também, os atributos:

 | Atributo  | Descrição |
 | :--------: | :-------- |
 | `doorsQty` | Quantidade de portas de um carro. Deve ser um valor inteiro positivo maior ou igual a 2 e menor ou igual a 4 |
 | `seatsQty` | Quantidade de assentos disponíveis no carro. Deve ser maior ou igual a 2 e menor ou igual a 7 |
 
<details>
  <summary>Será verificado se:</summary>

  - A interface `ICar` estende a interface `IVehicle`;
  - É possível criar um objeto do tipo `ICar`;
  - A interface `ICar` possui as propriedades `doorsQty` e `seatsQty`;
  - A interface está com local, nome e forma de exportação correta.

</details>


### Rota para o endpoint `/cars` onde seja possível cadastrar um novo carro

Requisição `POST` para cadastrar um veículo do tipo carro.

### Rota para o endpoint `/cars` onde seja possível listar todos os carros registrados

Rota que recebe uma requisição `GET` para receber todos os veículos do tipo carro registrados no banco de dados.

### Rota para o endpoint `/cars/id` onde seja possível listar um único carro através do seu id

Rota que recebe uma requisição `GET` para receber determinado veículo do tipo carro que possua o `id` passado como parâmetro na rota.

### Rota para o endpoint `/cars/id`, onde é possível atualizar o registro de um carro através do seu id

Rota que recebe uma requisição `PUT` para atualizar determinado veículo do tipo carro que possua o `id` passado como parâmetro na rota.

### Rota para o endpoint `/cars/id` para excluir os registros de um carro

Rota que receba uma requisição `DELETE` para excluir determinado veículo do tipo carro que possua o `id` passado como parâmetro na rota. 
