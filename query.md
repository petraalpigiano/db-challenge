<!-- 1. Seleziona tutti gli utenti e calcolane l'età (25) -->

```SQL
SELECT * FROM `likes`;
```

<!-- 2. Seleziona tutti i post senza Like (13) -->

```SQL
SELECT *
FROM `posts`
LEFT JOIN `likes`
ON `likes`.post_id = `posts`.id
WHERE `likes`.post_id IS NULL;
```
