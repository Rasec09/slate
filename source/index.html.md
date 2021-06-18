---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - c++

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>
  
search: true

code_clipboard: true
---

# Introduccion

Bienvenido a la API del Nopal Judge. A cotinuacion se explican todas las funciones con las cuales puedes interactuar con el juez.

This example API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to edit it and use it as a base for your own API's documentation.

# API

## POST

```shell
curl --header "Content-Type: application/json" --request POST --data '["3","1","#include <bits/stdc++.h>\n\nusing namespace std;\n\n\nint main()\n{​​​​​​​\n\tint x , a = 0;\n\tcin >> x;\n\tfor( int i = 0 ; i < x ; ++i){​​​​​​​\n\t\tfor(int j = 0 ; j < x ; ++j){​​​​​​​\n\t\t\tfor(int k = 0 ; k < x ; ++k){​​​​​​​\n\t\t\t\ta += 1;\n\t\t\t}​​​​​​​\n\t\t}​​​​​​​\n\t}​​​​​​​\n\tcout << x << \"\\n\";\t\n}​​​​​​​","user1"]' http://localhost:8080/restAPI
```

> El comando de arriba devuelve un objeto JSON estructurado de la siguiente forma:

```json
{"ID_Evaluacion":"STATUS"}
```

Envia un codigo para evaluarlo. La peticion se hace mediante el metodo POST. Devuelve el ID de evaluacion.

### Parametros

Parametro | Tipo | Descripcion
--------- | ---- | -----------
request | http_request | La peticion lleva el formato [ID_Problema, ID_Lenguaje, Codigo]

## GET

> El comando de arriba devuelve un objeto JSON estructurado de la siguiente forma:

```json
{"ID_Evaluacion":"ID_Veredicto"}
```

Consulta el resultado de una evaluacion. Se realiza mediante el metodo GET. Devuelve el ID del veredicto.

### Parametros
Parametro | Tipo | Descripcion
--------- | ---- | -----------
request | http_request | La peticion requiere de un ID_Evaluacion
