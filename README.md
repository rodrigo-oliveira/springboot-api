# springboot-api

## Spring Boot 3: API Rest em Java
API de uma clínica médica fictícia chamada Voll Med que precisa de um aplicativo para monitorar o cadastro de médicos, pacientes e agendamento de consultas.

## Objetivo
Esse repositório foi criado para acompanhar o curso "Spring Boot 3: desenvolva uma API Rest em Java" da Alura.

## Tecnologias
Spring Boot 3
Java 17
Lombok
MySQL/ Flyway
JPA/Hibernate
Maven
Insomnia

### Rotas:
#### Adicionar novos médicos:
POST: http://localhost:8080/medicos
Payload:
```json
{
    "nome": "Nome do médico",
    "email": "teste@email.com",
    "crm": "1234",
    "especialidade": "ORTOPEDIA",
    "endereco": {
    "logradouro": "rua 1",
    "bairro": "bairro",
    "cep": "18000000",
    "cidade": "São Paulo",
    "uf": "SP",
    "numero": "1",
    "complemento": "complemento"
    }
}
```

#### Adicionar novos pacientes:
POST: http://localhost:8080/pacientes
Payload:
```json
{
    "nome": "Nome do paciente",
    "email": "teste@email.com",
    "endereco": {
    "logradouro": "rua 1",
    "bairro": "bairro",
    "cep": "18000000",
    "cidade": "São Paulo",
    "uf": "SP",
    "numero": "1",
    "complemento": "complemento"
    }
}
```

#### Recuperar lista de médicos: (parâmetros opcionais de paginação)
GET: http://localhost:8080/medicos?tamanho=5&pagina=1&ordem=email,desc

#### Recuperar lista de pacientes: (parâmetros opcionais de paginação)
GET: http://localhost:8080/pacientes?tamanho=5&pagina=1&ordem=email,desc