# Obtener el manual

El repositorio es público. Puedes leerlo sin cuenta de GitHub, descargar una copia o clonarlo para conservarlo actualizado.

Repositorio: <https://github.com/ftrinidada/descubrex-playbook>

## Desde el sitio web

1. Abre el [repositorio](https://github.com/ftrinidada/descubrex-playbook).
2. Lee el `README.md` y los archivos dentro de `docs/` directamente en GitHub.
3. Para descargar una copia, pulsa **Code** y después **Download ZIP**.
4. Descomprime el archivo ZIP y abre `README.md` con un editor como VS Code, Cursor o un visor de Markdown.

El ZIP es una fotografía del repositorio en ese momento. Para recibir actualizaciones, vuelve a descargarlo o usa Git.

## macOS: descargar con Terminal

Primero comprueba si Git ya está disponible:

```bash
git --version
```

Si el comando no existe, instala las herramientas de línea de comandos de Xcode:

```bash
xcode-select --install
```

También puedes instalar Git desde [git-scm.com](https://git-scm.com/downloads). Después, en Terminal, elige una carpeta donde guardar tus proyectos y ejecuta:

```bash
git clone https://github.com/ftrinidada/descubrex-playbook.git
cd descubrex-playbook
open README.md
```

Para actualizar una copia que ya clonaste:

```bash
cd descubrex-playbook
git pull
```

## Windows: descargar con PowerShell

Instala [Git for Windows](https://git-scm.com/download/win). Si tu equipo tiene `winget`, también puedes hacerlo desde PowerShell:

```powershell
winget install --id Git.Git -e
```

Cierra y vuelve a abrir PowerShell. Comprueba la instalación y descarga el repositorio:

```powershell
git --version
git clone https://github.com/ftrinidada/descubrex-playbook.git
Set-Location .\descubrex-playbook
start README.md
```

Para actualizarlo en el futuro:

```powershell
Set-Location .\descubrex-playbook
git pull
```

## Si quieres aportar cambios

Para proponer mejoras necesitas una cuenta de GitHub. Haz un *fork*, crea una rama, realiza el cambio y abre un *pull request*. La guía oficial de GitHub explica el [flujo de fork y pull request](https://docs.github.com/es/pull-requests/collaborating-with-pull-requests/working-with-forks/about-permissions-and-visibility-of-forks).

No compartas en un issue, commit o pull request secretos, tokens, certificados, perfiles de firma, datos personales o información privada de un proyecto.
