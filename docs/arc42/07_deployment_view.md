# 7. Vista de Despliegue

## 7.1 Despliegue propuesto (fase inicial)

| Nodo | Contenido | Notas |
|---|---|---|
| Servidor de aplicaciones (VM Linux o contenedor Docker) | API Spring Boot (JAR ejecutable) | Expone la API REST por HTTPS detrás de un proxy inverso (Nginx). |
| Servidor web / CDN | Build estático de la SPA React | Servido por Nginx o un hosting estático. |
| Servidor de base de datos | PostgreSQL 16 | Backups diarios automáticos; acceso solo desde la API. |

## 7.2 Diagrama textual

```
[Navegador] --HTTPS--> [Nginx] --> [SPA estática]
                          |--/api--> [Spring Boot JAR] --JDBC--> [PostgreSQL]
```

En fases posteriores puede migrarse a contenedores orquestados (Docker Compose o Kubernetes) sin cambiar la arquitectura lógica.
