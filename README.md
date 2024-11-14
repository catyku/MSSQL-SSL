# MSSQL-SSL

## 建立自簽ssl

```
cd ssl
sudo openssl req -x509 -nodes -newkey rsa:2048 -subj '/CN=sql1.test.com' -keyout mssql.key -out mssql.pem -days 3650
chown -R 10001:10001 ssl
chown -R 10001:10001 data
```

## 啟動

```
docker compose up -d 
```
