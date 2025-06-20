# Guía de Trabajo con el Repositorio GitHub

## 📁 Repositorio del Proyecto
**URL:** https://github.com/efrenbohorquez/MONOGRAFIA

## 🔄 Comandos Git Básicos para el Proyecto

### Clonar el Repositorio (Primera vez)
```bash
git clone https://github.com/efrenbohorquez/MONOGRAFIA.git
cd MONOGRAFIA
```

### Flujo de Trabajo Diario

#### 1. Antes de comenzar a trabajar
```bash
# Obtener los últimos cambios del repositorio
git pull origin main
```

#### 2. Hacer cambios y guardarlos
```bash
# Ver el estado de los archivos
git status

# Agregar archivos modificados
git add .
# O agregar archivos específicos
git add archivo_especifico.tex

# Confirmar cambios con un mensaje descriptivo
git commit -m "Descripción clara de los cambios realizados"
```

#### 3. Subir cambios al repositorio
```bash
# Enviar cambios a GitHub
git push origin main
```

### Ejemplos de Mensajes de Commit

```bash
# Ejemplos de buenos mensajes de commit
git commit -m "Completar capítulo 1: Introducción"
git commit -m "Agregar referencias bibliográficas sobre ODS en Colombia"
git commit -m "Corregir formato APA en citas del marco teórico"
git commit -m "Actualizar metodología de investigación"
git commit -m "Añadir resultados preliminares del análisis"
```

## 🏗️ Estructura del Repositorio

```
MONOGRAFIA/
├── README.md                           # Descripción del proyecto
├── .gitignore                          # Archivos excluidos del control de versiones
├── seguimiento-proyecto.md             # Control de avance
├── capitulos/                          # Versiones en Markdown
│   ├── 01-introduccion.md
│   ├── 02-marco-teorico.md
│   ├── 03-metodologia.md
│   ├── 04-desarrollo.md
│   ├── 05-resultados.md
│   └── 06-conclusiones.md
├── latex/                              # Versión final en LaTeX
│   ├── main.tex                        # Documento principal
│   ├── portada.tex
│   ├── resumen.tex
│   ├── referencias.bib
│   ├── INSTRUCCIONES_COMPILACION.md
│   └── capitulos/
│       ├── introduccion.tex
│       └── marco-teorico.tex
├── referencias/                        # Bibliografía organizada
├── anexos/                             # Material complementario
├── imagenes/                           # Figuras y gráficos
└── plantillas/                         # Formatos y guías
```

## 💡 Mejores Prácticas

### 1. Frecuencia de Commits
- Hacer commits frecuentes con cambios pequeños y específicos
- No acumular muchos cambios en un solo commit
- Commit al menos una vez por sesión de trabajo

### 2. Mensajes Descriptivos
- Usar presente ("Agregar", no "Agregué")
- Ser específico sobre qué se cambió
- Mencionar el capítulo o sección modificada

### 3. Sincronización
- Siempre hacer `git pull` antes de comenzar a trabajar
- Hacer `git push` al finalizar cada sesión
- Resolver conflictos inmediatamente si aparecen

## 🔧 Comandos Útiles Adicionales

### Ver el historial de cambios
```bash
git log --oneline
```

### Ver diferencias en archivos
```bash
git diff archivo.tex
```

### Deshacer cambios no confirmados
```bash
git checkout -- archivo.tex
```

### Crear una rama para trabajar en características específicas
```bash
# Crear y cambiar a nueva rama
git checkout -b capitulo-metodologia

# Trabajar normalmente...
git add .
git commit -m "Desarrollar metodología de investigación"

# Cambiar de vuelta a main y fusionar
git checkout main
git merge capitulo-metodologia
```

## 📋 Lista de Verificación para Commits

- [ ] ¿Los archivos LaTeX compilan correctamente?
- [ ] ¿El mensaje de commit es descriptivo?
- [ ] ¿Se han agregado todos los archivos relevantes?
- [ ] ¿Se actualizó el seguimiento del proyecto si es necesario?
- [ ] ¿Las referencias bibliográficas están completas?

## 🆘 Solución de Problemas Comunes

### Error: "Updates were rejected"
```bash
git pull origin main
# Resolver conflictos si los hay
git push origin main
```

### Olvidé agregar un archivo al último commit
```bash
git add archivo_olvidado.tex
git commit --amend --no-edit
```

### Quiero deshacer el último commit (sin perder cambios)
```bash
git reset --soft HEAD~1
```

---
**Configuración inicial completada el:** 19 de junio de 2025
**Repositorio:** https://github.com/efrenbohorquez/MONOGRAFIA
