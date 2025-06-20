# Compilación del Documento LaTeX - Monografía ODS

## Requisitos del Sistema

### Software Necesario
- **TeXLive** (recomendado) o **MiKTeX** (Windows)
- **Biber** (para gestión de bibliografía)
- **Editor de LaTeX** (opcional): TeXStudio, Overleaf, VS Code con extensión LaTeX

### Paquetes LaTeX Requeridos
Los siguientes paquetes deben estar instalados:
- `babel` (soporte para español)
- `biblatex` (bibliografía en formato APA)
- `geometry` (configuración de márgenes)
- `setspace` (espaciado)
- `graphicx` (inserción de imágenes)
- `hyperref` (enlaces y marcadores)
- `fancyhdr` (encabezados y pies de página)

## Instrucciones de Compilación

### Opción 1: Línea de Comandos

```bash
# Navegar al directorio del proyecto
cd latex/

# Primera compilación
pdflatex main.tex

# Generar bibliografía
biber main

# Segunda compilación (para referencias cruzadas)
pdflatex main.tex

# Tercera compilación (para tabla de contenidos final)
pdflatex main.tex
```

### Opción 2: Using VS Code

1. Instalar la extensión **LaTeX Workshop**
2. Abrir el archivo `main.tex`
3. Usar `Ctrl+Alt+B` para compilar automáticamente

### Opción 3: TeXStudio

1. Abrir `main.tex` en TeXStudio
2. Configurar en Options > Configure TeXstudio > Build:
   - Default Compiler: `pdflatex`
   - Default Bibliography Tool: `biber`
3. Usar F5 para compilar y visualizar

### Opción 4: Overleaf (Online)

1. Crear nuevo proyecto en [Overleaf](https://www.overleaf.com)
2. Subir todos los archivos `.tex` y `.bib`
3. Configurar:
   - Compiler: `pdfLaTeX`
   - TeX Live version: 2023 (o más reciente)
4. Compilar automáticamente

## Estructura de Archivos

```
latex/
├── main.tex                    # Archivo principal
├── portada.tex                 # Página de título
├── resumen.tex                 # Resumen y abstract
├── referencias.bib             # Base de datos bibliográfica
├── capitulos/
│   ├── introduccion.tex        # Capítulo 1
│   ├── marco-teorico.tex       # Capítulo 2
│   ├── metodologia.tex         # Capítulo 3
│   ├── desarrollo.tex          # Capítulo 4
│   ├── resultados.tex          # Capítulo 5
│   └── conclusiones.tex        # Capítulo 6
├── imagenes/                   # Directorio para figuras
└── anexos/
    └── anexos.tex              # Anexos del documento
```

## Configuración APA 7

El documento está configurado para cumplir con las normas APA 7:

- **Fuente:** Times New Roman, 12pt
- **Espaciado:** 1.5
- **Márgenes:** Superior/Inferior 3cm, Izquierdo 4cm, Derecho 2cm
- **Numeración:** Esquina superior derecha
- **Referencias:** Formato APA 7 con biblatex

## Personalización

### Información del Autor
Editar en `portada.tex`:
- Nombre de la universidad
- Facultad y programa
- Nombre del autor
- Código estudiantil
- Director de la monografía

### Contenido
Completar los siguientes archivos:
- `capitulos/metodologia.tex`
- `capitulos/desarrollo.tex`
- `capitulos/resultados.tex`
- `capitulos/conclusiones.tex`

### Referencias
Agregar nuevas referencias en `referencias.bib` siguiendo el formato BibTeX.

## Solución de Problemas Comunes

### Error de Compilación
- Verificar que todos los paquetes estén instalados
- Revisar sintaxis en archivos `.tex`
- Asegurar que `referencias.bib` tenga formato correcto

### Bibliografía No Aparece
- Ejecutar secuencia completa: pdflatex → biber → pdflatex → pdflatex
- Verificar que las citas estén correctamente referenciadas con `\citep{}` o `\citet{}`

### Caracteres Especiales
- Usar codificación UTF-8
- Para caracteres especiales: `\'a` (á), `\~n` (ñ), etc.

## Checklist Final

- [ ] Todas las secciones completadas
- [ ] Referencias bibliográficas actualizadas
- [ ] Imágenes y tablas numeradas correctamente
- [ ] Formato APA 7 aplicado consistentemente
- [ ] Ortografía y gramática revisadas
- [ ] Documento compila sin errores
- [ ] PDF final generado correctamente

---
**Última actualización:** 19 de junio de 2025
