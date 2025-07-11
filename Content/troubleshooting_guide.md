
# 🛠️ Guía de Troubleshooting - GitHub API con Google Colab

Esta guía te ayudará a identificar y solucionar errores comunes al interactuar con la API de GitHub desde Google Colab usando Python.

## ⚙️ Autenticación y Token

Si encuentras el error:

```
Error 401: No autorizado - revisa tu token
```

### Posibles causas y soluciones:

- ❌ El token está mal escrito o ha caducado.
- ✅ Solución: Ve a [https://github.com/settings/tokens](https://github.com/settings/tokens) y genera un nuevo token personal con los siguientes permisos:
  - `public_repo`
  - `read:user`

- ✅ Asegúrate de que el token esté definido correctamente en el código:
```python
TOKEN = "tu_token_personal"
HEADERS = {
    "Authorization": f"Bearer {TOKEN}",
    "Accept": "application/vnd.github+json"
}
```

---

## 🚫 Error 403: Rate Limit

```
Error 403: Límite de tasa alcanzado o acceso prohibido
```

### Posibles causas:

- Has realizado muchas peticiones en un corto período de tiempo.
- GitHub impone límites de uso dependiendo si estás autenticado o no.

### Soluciones:

- ✅ Esperar unos minutos e intentarlo nuevamente.
- ✅ Asegurarte de usar autenticación con token (así el límite es más alto).
- ✅ Consultar tu límite actual con este endpoint:
```python
url = "https://api.github.com/rate_limit"
response = requests.get(url, headers=HEADERS)
print(response.json())
```

---

## ❓ Otros códigos de error

- `404`: El recurso no fue encontrado. Verifica bien la URL del endpoint.
- `422`: Error de validación, usualmente por parámetros mal pasados.
- `500` o `502`: Errores del servidor de GitHub. Espera e intenta de nuevo.

---

## 🧪 Tips Adicionales

- Siempre revisa `response.status_code` para identificar qué tipo de error ocurre.
- Puedes imprimir `response.text` para ver más detalles.
- Revisa la documentación oficial: [GitHub REST API docs](https://docs.github.com/en/rest)

---

> Última actualización basada en el script de autenticación y extracción de repositorios públicos desde la API de GitHub usando Google Colab.
