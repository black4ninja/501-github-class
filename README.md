# Proyecto Node.js

## Descripción
Proyecto de desarrollo en Node.js

## Instalación

```bash
npm install
```

## Uso

```bash
npm start
```

## Estándar de Commits

Este proyecto sigue la convención de [Conventional Commits](https://www.conventionalcommits.org/).

### Formato
```
<tipo>[ámbito opcional]: <descripción>

[cuerpo opcional]

[nota de pie opcional]
```

### Tipos de commits

- `feat`: Nueva funcionalidad
- `fix`: Corrección de bugs
- `docs`: Cambios en documentación
- `style`: Cambios de formato (espacios, punto y coma, etc)
- `refactor`: Refactorización de código
- `test`: Añadir o modificar tests
- `chore`: Tareas de mantenimiento
- `perf`: Mejoras de rendimiento
- `ci`: Cambios en configuración de CI/CD
- `build`: Cambios en el sistema de build

### Ejemplos
```bash
feat: agregar endpoint de autenticación
fix: corregir validación de email
docs: actualizar guía de instalación
refactor: optimizar consultas a base de datos
test: agregar tests unitarios para usuario
```

## Estándar de Branches

### Branches principales

- `main`: Branch principal de producción
- `develop`: Branch de desarrollo

### Branches de trabajo

#### Feature branches
- Formato: `feature/<nombre-descriptivo>`
- Uso: Nuevas funcionalidades
- Ejemplo: `feature/user-authentication`

#### Bugfix branches
- Formato: `bugfix/<nombre-descriptivo>`
- Uso: Corrección de bugs en develop
- Ejemplo: `bugfix/login-validation`

#### Hotfix branches
- Formato: `hotfix/<nombre-descriptivo>`
- Uso: Correcciones urgentes en producción
- Ejemplo: `hotfix/security-patch`

#### Release branches
- Formato: `release/<version>`
- Uso: Preparación de nuevas versiones
- Ejemplo: `release/1.0.0`

### Flujo de trabajo

1. Crear branch desde `develop`:
```bash
git checkout develop
git pull origin develop
git checkout -b feature/nueva-funcionalidad
```

2. Hacer commits siguiendo el estándar
3. Crear Pull Request hacia `develop`
4. Después de revisión y aprobación, hacer merge
5. Eliminar la branch de trabajo

## Estándar de Versionado

Este proyecto utiliza [Semantic Versioning](https://semver.org/) (SemVer) para el manejo de versiones.

### Formato
```
x.y.z
MAJOR.MINOR.PATCH
```

### Componentes

- **MAJOR (x)**: Cambios incompatibles con versiones anteriores
  - Modificaciones que rompen la compatibilidad
  - Cambios en la API que requieren modificaciones en código existente
  - Ejemplo: `1.0.0` → `2.0.0`

- **MINOR (y)**: Nueva funcionalidad compatible con versiones anteriores
  - Nuevas características que no rompen compatibilidad
  - Mejoras y adiciones a la funcionalidad existente
  - Ejemplo: `1.0.0` → `1.1.0`

- **PATCH (z)**: Correcciones de bugs compatibles con versiones anteriores
  - Corrección de errores
  - Mejoras de rendimiento
  - Actualizaciones de seguridad menores
  - Ejemplo: `1.0.0` → `1.0.1`

### Reglas de incremento

1. Al hacer cambios incompatibles: incrementar MAJOR y resetear MINOR y PATCH a 0
2. Al agregar funcionalidad compatible: incrementar MINOR y resetear PATCH a 0
3. Al corregir bugs: incrementar PATCH

### Ejemplos

```
1.0.0 → Primera versión estable
1.0.1 → Corrección de bugs
1.1.0 → Nueva funcionalidad compatible
2.0.0 → Cambios incompatibles (breaking changes)
```

### Crear versión con Git

```bash
# Crear tag de versión
git tag -a v1.0.0 -m "Versión 1.0.0"

# Subir tag al repositorio
git push origin v1.0.0

# Listar tags existentes
git tag -l
```

## Licencia
MIT
