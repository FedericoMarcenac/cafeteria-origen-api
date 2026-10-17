# Cafetería Origen – API

API REST (Node.js + Express) para organizar los pedidos de la cafetería Origen.

## Cómo correrlo
```bash
npm install
npm test     # 54 tests con Jest + Supertest
npm start    # http://localhost:3000
```

## Endpoints
| Método | Ruta | Descripción |
|---|---|---|
| GET | /productos | Lista de productos (20) |
| GET | /productos/:id | Producto por id |
| POST | /pedidos | Crea pedido y devuelve total calculado |
| GET | /pedidos | Lista de pedidos |
| GET | /pedidos/:id | Pedido por id |
| GET | /reportes/facturacion | Facturación total |
| GET | /reportes/mas-vendido | Producto más vendido |

## Ejemplo
```bash
curl -X POST http://localhost:3000/pedidos -H "Content-Type: application/json" \
  -d '{"items":[{"productoId":1,"cantidad":2},{"productoId":19,"cantidad":1}]}'
```
