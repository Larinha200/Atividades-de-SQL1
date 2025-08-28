# Atividades-de-SQL1
NÍVEL 1

->2603

<img width="1049" height="312" alt="Image" src="https://github.com/user-attachments/assets/2b0ccda3-d9bf-496c-b797-76fffd436a19" />
<img width="1078" height="52" alt="Image" src="https://github.com/user-attachments/assets/e9176d3a-a974-4013-b551-1817ec45a910" />

Código:
```sql
SELECT 
	name,
	street
FROM 
	customers
WHERE
	city LIKE '%Porto Alegre%';
```

->2607

<img width="1050" height="316" alt="Image" src="https://github.com/user-attachments/assets/891c01a5-4af1-4d96-a3d7-d833bb4e1640" />
<img width="1079" height="43" alt="Image" src="https://github.com/user-attachments/assets/1d00e8d4-8f8e-4c47-a05c-5f5b864bba29" />

Código:
```sql
SELECT 
		city
FROM
		providers
ORDER BY
		city
ASC;
```

->2608

<img width="1074" height="429" alt="Image" src="https://github.com/user-attachments/assets/0403156c-8a78-48d5-8c21-2420bf8fcf08" />
<img width="1069" height="31" alt="Image" src="https://github.com/user-attachments/assets/144aac27-8b82-4b7f-922f-191fae814cd5" />

Código:
```sql
SELECT
		MAX(price),
		MIN(price)
FROM
		products;
```

->2615

<img width="1074" height="318" alt="Image" src="https://github.com/user-attachments/assets/0e34e404-3df9-4bca-a062-5fe018647f2e" />
<img width="1072" height="42" alt="Image" src="https://github.com/user-attachments/assets/2dcbcb3f-44f1-4966-ac9e-05e50ec57085" />

Código:
```sql
SELECT
		city
FROM
		customers;
```

->2617

<img width="957" height="279" alt="Image" src="https://github.com/user-attachments/assets/92a27786-1864-4dda-9529-cb7aa552749d" />
<img width="1081" height="42" alt="Image" src="https://github.com/user-attachments/assets/170200e3-9a1e-473d-a6db-0979639d251c" />

Código:
```sql
SELECT
		A.name,B.name
FROM 
		products AS A
INNER JOIN 
		providers AS B ON A.id_providers = B.id
WHERE 
		B.name = 'Ajax SA';
```

NÍVEL 2

->2604

<img width="1057" height="310" alt="Image" src="https://github.com/user-attachments/assets/7dd73c87-fb12-4e1b-9f29-cfc3c41b1dd3" />
<img width="1089" height="43" alt="Image" src="https://github.com/user-attachments/assets/6d2891ec-7a39-4e7d-8aed-0884f5ff1172" />

Código:
```sql
SELECT
		id,
		name
FROM
		products
WHERE
		price<10 OR price>100;
```

->2613

<img width="1022" height="300" alt="Image" src="https://github.com/user-attachments/assets/41a6770b-f905-4dc1-bb29-b04f667245a4" />
<img width="810" height="37" alt="Image" src="https://github.com/user-attachments/assets/a10cfc6d-dc87-49a0-b653-9205ce734b29" />

Código:
```sql
SELECT
		movies.id, 
		movies.name
FROM
		movies
INNER JOIN 
		prices ON movies.id_prices = prices.id
WHERE value<2;
```

NÍVEL 3 

->2610

<img width="1070" height="318" alt="Image" src="https://github.com/user-attachments/assets/ef7141d4-e43e-46ec-97d8-e1e6f0b47a8b" />
<img width="788" height="25" alt="Image" src="https://github.com/user-attachments/assets/c1c74c44-cbe4-4bf7-a737-1dcf667fdb80" />

Código:
```sql
SELECT
		ROUND(AVG(price),2) AS Media
FROM
		products;
```

->2618

<img width="1075" height="315" alt="Image" src="https://github.com/user-attachments/assets/c756901f-f3fd-4423-ab78-8af9de8df406" />
<img width="815" height="34" alt="Image" src="https://github.com/user-attachments/assets/691cb9f3-b92a-440b-91b1-d98a3da823be" />

Código:
```sql
SELECT
		A.name,
		providers.name,
		categories.name
FROM
		products AS A 
INNER JOIN
		providers ON A.id_providers = providers.id
INNER JOIN
		categories ON A.id_categories = categories.id
WHERE 
		providers.name= 'Sansul SA' AND categories.name = 'Imported';
```

NÍVEL 4

->2602

<img width="1044" height="307" alt="Image" src="https://github.com/user-attachments/assets/4fad7ee9-8f4e-421a-a913-3cc995f1fdec" />
<img width="818" height="28" alt="Image" src="https://github.com/user-attachments/assets/f70300bb-208e-4539-9606-475adae5332a" />

Código:
```sql
SELECT
		name
FROM
		customers
WHERE
		state LIKE '%RS%';
```

NÍVEL 5

->2616

<img width="1025" height="305" alt="Image" src="https://github.com/user-attachments/assets/48a9250f-da7f-44f6-9390-9d33fe850585" />
<img width="814" height="30" alt="Image" src="https://github.com/user-attachments/assets/3d2ff834-e55a-4294-a109-2157e0a659fa" />

Código:
```sql
SELECT 
		customers.id,
		customers.name
FROM
		customers
LEFT JOIN
		locations ON customers.id = locations.id_customers
WHERE
		locations.id_customers IS NULL
```
