# JSharp.Net 🚀

**JSharp.Net** (basado en el legado de Visual J#) es un entorno de ejecución e implementación de alto rendimiento diseñado como **lenguaje transicional** para desarrolladores de Java que buscan migrar o interoperar sin fricción con el ecosistema .NET.

Desarrollado sobre la plataforma de código abierto **Mono**, JSharp.Net traduce y ejecuta la sintaxis y semántica de Java/J# directamente sobre el Common Language Runtime (CLR) de Mono, facilitando la adopción gradual de bibliotecas .NET y la reutilización de código Java sin depender de la JVM.

---

## 🌟 Características Principales

* **Sintaxis Java / Semántica .NET Nativa:** Permite a los desarrolladores escribir sintaxis conocida de Java mientras consumen de manera directa la Base Class Library (BCL) de .NET (`System.*`).
* **Ejecución Multiplataforma con Mono:** Compatibilidad completa con Linux, macOS y Windows gracias a la madurez e integración del runtime de Mono.
* **Transición de Código Legado:** Reutilización e interoperabilidad directa de librerías bytecode/fuente de Java en aplicaciones .NET sin reescrituras complejas.
* **Compilación AOT e Instalación Nativa:** Soporte para compilación ahead-of-time (AOT) mediante `mono --aot` para reducir tiempos de inicio y huella de memoria.

---

## 🏗️ Arquitectura de la Plataforma

* **JSharp Compiler (jsc):** Transpila el código fuente de JSharp.Net (`.jsl`) a CIL (Common Intermediate Language) compatible con el estándar ECMA CLI.
* **Mono CLR Runtime:** Motor de ejecución encargado de gestionar la recolección de basura, hilos y seguridad de tipos en la plataforma .NET.
* **Java-to-BCL Binding Layer:** Capa de mapeo que conecta de forma transparente los tipos primitivos y colecciones de Java con la biblioteca de clases de Mono/NET.

---

## 2. 🚦 Inicio Rápido

### Prerrequisitos

* **Mono Runtime & Development Tools** (`mono-complete` versión 6.x o superior).
* Variables de entorno `PATH` y `MONO_PATH` configuradas adecuadamente.

### Instalación

```bash
# Clonar el repositorio
git clone [https://github.com/tu-usuario/jsharp-net.git](https://github.com/tu-usuario/jsharp-net.git)
cd jsharp-net

# Construir los componentes con Mono / xbuild / msbuild
msbuild JSharp.Net.sln
