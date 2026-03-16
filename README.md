# Projeto4-Pontos

Documentação do Objeto de Estoque (Stock)

Schema de validação para o arquivo de estoque:

Arquivo: stock.json

{
"product_id": <number>
"location_id": <number
"available_quantity": <number>
"reserved_quantity": <number>
}

Regras das Propriedades:
- product_id         (number, Obrigatório): ID do produto.
- location_id        (number, Obrigatório): ID do local de armazenamento.
- available_quantity (number, Obrigatório): Quantidade livre.
- reserved_quantity  (number, Opcional)   : Quantidade reservada (Padrão: 0).

---------------------------------------------------------

Documentação do Objeto de Local Físico (Physical Location)

Schema de validação para cadastro ou consulta de locais físicos:

Arquivo: physical_location.json

Exemplo de estrutura do arquivo (JSON válido):

{
"location_name": "<string>",
"location_type": "<string>",
"description": "<string>",
"max_capacity": <number>,
"status": "<string>"
}

Regras das Propriedades:
- location_name      (string, Obrigatório): O nome de identificação do local.
- location_type      (string, Obrigatório): A categoria ou classificação do local.
- description        (string, Opcional)   : Detalhes ou observações adicionais sobre o local.
- max_capacity       (number, Opcional)   : Limite máximo de itens ou volume suportado.
- status             (string, Opcional)   : A situação atual de operação do local. 
↳ Regra de Enumeração: Só aceita os valores exatos "ACTIVE" ou "INACTIVE".
↳ Regra Padrão: Se o campo não for enviado, assumirá o valor "ACTIVE".

---------------------------------------------------------

projeto/
|
├─ database.sql
├─ README.md
├─ stock.json
└─ physical_location.json
