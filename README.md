# 🛒 API de Produtos — Spring Boot

API REST de gerenciamento de produtos desenvolvida com **Java + Spring Boot**, criada como projeto prático de aprendizado.

---

## Sobre o projeto

API simples e funcional com CRUD completo de produtos, boas práticas de status HTTP e tratamento de erros com `ResponseEntity` e `Optional`.

---

## Funcionalidades

- Listar todos os produtos
- Buscar produto por ID (retorna 404 se não encontrado)
- Adicionar novo produto
- Editar produto existente (retorna 404 se não encontrado)
- Remover produto (retorna 404 se não encontrado)

---

## Endpoints

| Método | Rota | Descrição |
|---|---|---|
| GET | `/produtos` | Lista todos os produtos |
| GET | `/produtos/{id}` | Busca produto por ID |
| POST | `/produtos` | Adiciona novo produto |
| PUT | `/produtos/{id}` | Edita produto existente |
| DELETE | `/produtos/{id}` | Remove produto |

---

## Exemplo de uso

**Adicionar produto — POST /produtos**
```json
{
    "nome": "Sucrilhos",
    "preco": 8.50,
    "emEstoque": true
}
```

**Resposta — 200 OK**
```json
{
    "id": 1,
    "nome": "Sucrilhos",
    "preco": 8.50,
    "emEstoque": true
}
```

**Buscar produto inexistente — GET /produtos/99**
```
404 Not Found
```

---

## Conceitos praticados

| Conceito | Onde aparece |
|---|---|
| `@RestController` | Classe controller |
| `@RequestMapping` | Rota base `/produtos` |
| `@GetMapping` | Listar e buscar |
| `@PostMapping` | Criar produto |
| `@PutMapping` | Editar produto |
| `@DeleteMapping` | Remover produto |
| `@PathVariable` | Captura o `{id}` da URL |
| `@RequestBody` | Converte JSON em objeto Java |
| `ResponseEntity` | Retorna status HTTP corretos |
| `Optional` | Trata produto não encontrado |
| Lombok | `@Getter`, `@Setter`, `@ToString` |

---

## Stack

- Java 17+
- Spring Boot 3.x
- Lombok
- Testado com Postman

---

## Como rodar

**Pré-requisitos:** JDK 17+ e IntelliJ IDEA

```bash
# Clone o repositório
git clone https://github.com/HeniqueSantos/api-produtos-spring

# Abra no IntelliJ e rode a classe principal
# Acesse: http://localhost:8080/produtos
```

---

## Próximos passos

- [ ] Conectar ao PostgreSQL com Spring Data JPA
- [ ] Adicionar camada Service
- [ ] Validações com Bean Validation
- [ ] Deploy na nuvem

---

## Autor

Desenvolvido durante o aprendizado de Java + Spring Boot como parte de um roadmap fullstack.
