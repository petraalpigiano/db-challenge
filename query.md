<!-- 1. Seleziona tutti gli utenti e calcolane l'età media (25) -->

```SQL
SELECT *,
TIMESTAMPDIFF(YEAR, `birthdate`, CURDATE()) AS `age`
FROM `users`;
```

<!-- 2. Seleziona tutti i post senza Like (13) -->

```SQL
SELECT *
FROM `posts`
LEFT JOIN `likes`
ON `likes`.post_id = `posts`.id
WHERE `likes`.post_id IS NULL;
```
