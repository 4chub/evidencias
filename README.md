# Endpoint: ConsolidadoCobrancaEmpresa

Este endpoint fornece informações consolidadas sobre a cobrança por empresa em um intervalo de datas.

## **URL**

`https://api.4ciweb.com/api/Dashboard/ConsolidadoCobrancaEmpresa`

---

## **Método**

`POST`

---

## **Headers**

- `Content-Type`: `application/json`
- `Authorization`: `Bearer <seu_token>`

---

## **Body Parameters**

| Campo             | Tipo     | Obrigatório | Descrição                                                                 |
|--------------------|----------|-------------|---------------------------------------------------------------------------|
| `initalDateStr`   | `string` | Sim         | Data inicial no formato `YYYY-MM-DD`.                                    |
| `finalDateStr`    | `string` | Sim         | Data final no formato `YYYY-MM-DD`.                                      |
| `addIdentificador`| `boolean`| Sim         | Indica se o identificador deve ser adicionado ao retorno.                |
| `Page`            | `int`    | Sim         | Número da página a ser consultada (utilizado para paginação de resultados). |

### **Exemplo do Body**

```json
{
  "initalDateStr": "2024-11-21",
  "finalDateStr": "2024-11-21",
  "addIdentificador": true,
  "Page": 1
}
