# Tasks Backend

## Endpoints

1. Registrar => <b>{Host}/signup (POST)</b>
    - Recebe um JSON com os dados: {name, email e password}, todos do tipo String;
    - Retorna status (204 No Content) caso a requisição funcione.
2. Login => <b>{Host}/signin (POST)</b>
    - Recebe um JSON com os dados: {email e password}, todos do tipo String;
    - Retorna status (200 OK) quando os dados estão corretos;
    - Retorna no corpo da resposta um JSON contendo: {name, email e token}.
3. Create => <b>{Host}/tasks (POST)</b>
    - Recebe JSON contendo { desc e estimateAt }, desc = String, estimateAt = Date.
    - Retorna status (204 No Content)
4. List All => <b>{Host}/tasks (GET)</b>
    - Retorna um JSON de todas as Tasks cadastradas.
5. Task Toggle => <b>{Host}/tasks/{{id}}/toggle (PUT)</b>
    - Retorna status (204 No Content);
    - Este endpoint serve para marcar tarefa como concluida
6. Delete => <b>{Host}/tasks/{{id}} (DELETE)</b>
    - Retorna status (204 No Content);
    - Deleta a task com o id informado.