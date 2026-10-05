# Restful-Booker API tests

Postman-collection voor de opdracht "API Testing & Postman met restful-booker" (PXL, Gijs Colson).

- `restful-booker.postman_collection.json`: tests per user story (US1-US8)
- `restful-booker.postman_environment.json`: environment met `baseUrl`
- `.github/workflows/api-tests.yml`: draait de collection met Newman bij elke push

De API bevat opzettelijke bugs. Falende tests worden niet aangepast maar gerapporteerd als bug,
dus de run in de Actions-tab is deels rood. Het HTML-rapport staat als artifact `newman-report` bij elke run.

Lokaal uitvoeren:

```bash
npm install -g newman
newman run restful-booker.postman_collection.json -e restful-booker.postman_environment.json
```
