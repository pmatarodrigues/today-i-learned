# Update Table based on SELECT Query


´´´
UPDATE firstTable first
INNER JOIN secondTable second ON first.id = second.id
SET first.value = second.value
´´´

[Source](https://stackoverflow.com/a/1262848/14076293)