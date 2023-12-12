# Play with mysql

```
kubectl exec -it
```

```
mysql -h catalog-mysql -u catalog -p
```

```
USE catalog;
```

```
SHOW TABLES;
```

```
SELECT * FROM product;
```

```
INSERT INTO product (product_id, name, description, price, count, image_url)
VALUES ('demo-id', 'Demo Product', 'This is a demo product for illustration.', 99, 10, '/assets/demo_product.jpg');
```

```
kubectl get secret catalog-db -o jsonpath='{.data.username}' | ForEach-Object { [System.Text.Encoding]::Utf8.GetString([System.Convert]::FromBase64String($\_)) }
```

```
kubectl get secret catalog-db -o jsonpath='{.data.password}' | ForEach-Object { [System.Text.Encoding]::Utf8.GetString([System.Convert]::FromBase64String($\_)) }
```
