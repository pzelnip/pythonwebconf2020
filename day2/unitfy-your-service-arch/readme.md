# Unify Your Service Architecture With OpenAPI

This talk will go through understanding what OpenAPI and JSON Schema is, how it
can help your organization write better endpoints, why it is superior to
alternatives like grpc and how to utilize it in your python projects.

We will also describe approaches to integrating OpenAPI and JSON schema into
your python projects with simple patterns utilizing dependency injection,
automatic definition testing with pytest and output validation. Also, it will
demonstrate how using libraries like pydantic will also give you automatic mypy
support along with JSON Schema.

We’ll utilize patterns that can be translated to any Python framework.

(talk started 8 minutes late)

---

Overview of Open API

---

Overview of Swagger/redoc

---

Overview of JSON Schema

- what is this? Not clear how it relates to oapi or swagger
- ahh, this is just "JSON" as a way to describe data

---

History

SGML through to XML to SOAP etc

---

Example of pydantic with FastAPI

uses type hits to validate requests
quite elegant

get open api spec for free

---

It's come for your database too

Mongo, Couch, etc

---

Validate with JSON Schema

Utilize JSON Schema to validate data you store in db, jsonschema package

---

Compared to GRPC

Largely just ripped on GRPC

---

json-schema-env-validator https://pypi.org/project/json-schema-env-validator/
freddy https://pypi.org/project/freddy/

https://www.stavros.io/posts/fastapi-with-django/
