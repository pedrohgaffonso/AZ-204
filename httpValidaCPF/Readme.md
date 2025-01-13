# Validação de CPF

Este projeto contém uma função Azure que valida CPFs.

## Pré-requisitos

- [Postman](https://www.postman.com/downloads/) instalado em sua máquina.

## Como realizar o teste

1. Abra o Postman.
2. Use o endereço no qual a função está hospedada. Por exemplo: `https://fnphgapp001.azurewebsites.net/api/fnvalidacpf?code=-6HLhZByRQGUWo7FGVzYbDsAWpMDGbMZrUXyEKcGWxkjAzFujVibig%3D%3D`
3. Selecione o método `POST`.
4. No corpo da requisição (`Body`), selecione a opção `raw` e escolha o formato `JSON`.
5. Insira um JSON contendo o CPF a ser validado. Exemplo:
    ```json
    {
      "cpf": "12345678909"
    }
    ```
6. Clique em `Send` para enviar a requisição.

### Exemplos de respostas

- Caso o CPF informado seja válido:
    ```json
    {
      "message": "CPF válido."
    }
    ```

- Caso o CPF informado seja inválido:
    ```json
    {
      "message": "CPF inválido."
    }
    ```

- Caso o CPF não seja informado:
    ```json
    {
      "message": "Por favor, informe o CPF."
    }
    ```