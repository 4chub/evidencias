# Consolidado de Cobranças

Este endpoint fornece informações consolidadas sobre a cobrança por empresa em um intervalo de datas.

## Endpoint de Login

### **POST** `/api/Login`

**Descrição:** Efetua login na API para obter o token necessário para autenticação.

### Parâmetros

- **Sem parâmetros de URL**

### Corpo da Requisição

Formato `application/json`:

```json
{
  "username": "string",
  "password": "string"
}
```

### Respostas

- **200 OK**: Retorna o token e a validade.
- **400 Bad Request**: Falha na autenticação.

---

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
