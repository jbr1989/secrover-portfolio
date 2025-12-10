# Escaneo diario de vulnerabilidades

Este repositorio ejecuta un escaneo de seguridad diario a los dominios y repositorios definidos usando [Secrover](https://github.com/secrover/secrover) (contenedor Docker) y lo gestiona mediante [GitHub Actions](https://docs.github.com/en/actions).

## ¿Qué hace?

- Usando el Github Actions `.github/workflows/secrover.yml`, ejecuta el contenedor `secrover/secrover` diariamente a las 03:00 UTC.
- Usa el `config.yaml` para especificar objetivos.
- Genera los informes en la carpeta `docs/` y los commitea automáticamente.

## Salida

- Los informes se publican en `docs/` (una carpeta por fecha).
- `docs/latest.html` redirige al informe más reciente y `docs/index.html` lista todos los informes.