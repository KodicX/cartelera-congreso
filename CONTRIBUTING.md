# Cómo contribuir

Nadie del taller tiene permiso de escritura en `KodicX/cartelera-congreso`. Todo cambio entra por **fork** y **pull request**, y solo los instructores hacen merge.

## 1. Fork y clone

1. Abre `https://github.com/KodicX/cartelera-congreso` y haz clic en **Fork** → **Create fork**.
2. Clona **tu fork**, no el original:

   ```bash
   git clone git@github.com:USUARIO/cartelera-congreso.git
   cd cartelera-congreso
   git remote -v
   ```

   `origin` debe mostrar tu usuario, no `KodicX`.

## 2. Una rama por cambio

Nunca trabajes en `main`. Crea una rama para cada pull request:

| Cambio | Nombre de la rama |
|---|---|
| Tu perfil | `agrega-USUARIO` |
| Cambio en `programa.md` | `actualiza-programa-equipo-X` |

## 3. Commits

- Un commit explica un cambio. Usa un prefijo: `feat:` para algo nuevo y `fix:` para una corrección.
- Ejemplo: `feat: agrega perfil de USUARIO`.
- Incluye solo los archivos que tu pull request dice que cambia.

## 4. Pull request

- `base repository`: **KodicX/cartelera-congreso**, `base`: **main**.
- `head repository`: **tu fork**, `compare`: tu rama.
- Llena los tres encabezados de la plantilla: **Qué cambia**, **Por qué** y **Cómo revisarlo**.
- Deja marcada **Allow edits by maintainers**.

## 5. Revisión

- Revisa **Files changed** completo antes de aprobar.
- Si te piden cambios, corrige en la **misma rama**, haz commit y `git push`. El pull request se actualiza solo.
- Nunca uses `git push --force`.

## 6. Si tu rama tiene conflictos

1. En tu fork, haz clic en **Sync fork** → **Update branch**.
2. En tu computadora:

   ```bash
   git switch main
   git pull
   git switch tu-rama
   git merge main
   ```

3. Resuelve el conflicto, quita los marcadores `<<<<<<<`, `=======` y `>>>>>>>`, y termina con `git add`, `git commit --no-edit` y `git push`.
