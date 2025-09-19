   DROP DATABASE exemplo_sql;
   ```
<br>

<h3 id="select"> 📌 SELECT </h3>

- Usado para consulta dados de uma ou mais tabelas.

    - **Selecionando dados:**

    ```sql
    SELECT * FROM nome_da_tabela;               -- todas as colunas
    SELECT nome, idade FROM Pessoas;            -- colunas específicas
    SELECT nome AS NomeCompleto FROM Pessoas;   -- renomeando coluna
    SELECT DISTINCT cidade FROM Pessoas;        -- valores distintos
    ```

    - **Ordenando resultados:**

    ```sql
    SELECT * FROM Pessoas ORDER BY nome ASC; -- Crescente
    SELECT * FROM Pessoas ORDER BY idade DESC; -- Crescente
    ```

    - **Filtrando com WHERE:**

    ```sql
    SELECT * FROM Pessoas WHERE idade > 18; -- Idades maiores que 18
    SELECT * FROM Pessoas WHERE cidade = 'São Paulo';
    ```

    - **Busca por padrão (LIKE):**

    ```sql
    SELECT * FROM Pessoas WHERE nome LIKE 'A%';       -- começa com A
    SELECT * FROM Pessoas WHERE nome LIKE '%A';       -- termina com A
    SELECT * FROM Pessoas WHERE nome LIKE '%A%';      -- contém A
    ```

    - **Funções de agregação:**

    ```sql
    SELECT COUNT(*) FROM Pessoas;       -- total de registros
    SELECT AVG(idade) FROM Pessoas;     -- idade média
    SELECT MAX(idade) FROM Pessoas;     -- maior idade
    SELECT MIN(idade) FROM Pessoas;     -- menor idade
    SELECT SUM(peso) FROM Pessoas;      -- soma dos pesos
    ```

    - **Agrupando resultados:**

    ```sql
    SELECT cidade, COUNT(*) 
    FROM Pessoas 
    GROUP BY cidade;
    ```

    - **Filtrando grupos (HAVING):**

    ```sql
    SELECT cidade, COUNT(*) 
    FROM Pessoas 
    GROUP BY cidade
    HAVING COUNT(*) > 5;
    ```
