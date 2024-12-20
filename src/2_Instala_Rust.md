### Instalación de Rust en macOS

Rust tiene excelente soporte en macOS, y puedes instalarlo rápidamente usando `rustup`.

1. **Instalar Homebrew (si no lo tienes instalado):**
   - Homebrew es un gestor de paquetes para macOS, útil para instalar dependencias y herramientas.
   - Si no lo tienes, instálalo ejecutando:
     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
2. **Instalar Rust usando rustup:**
   - Ejecuta este comando en el terminal:
     ```bash
     curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
     ```
   - Sigue las instrucciones. Esto instalará `rustc` (el compilador de Rust), `cargo` (el gestor de paquetes) y `rustup` (el gestor de versiones).
3. **Configurar el entorno:**
   - Rustup configurará automáticamente tu entorno. Para asegurarte, añade Rust al `PATH` ejecutando:
     ```bash
     export PATH="$HOME/.cargo/bin:$PATH"
     ```
   - Luego, verifica la instalación:Deberías ver la versión instalada de Rust.
     ```bash
     rustc --version
     ```
4. **Actualizar Rust:**
   - Mantén tu instalación de Rust actualizada con:
     ```bash
     rustup update
     ```
   - **Instalar la extensión de Rust:**
     - Abre Visual Studio Code.
     - Ve a "Extensiones" (ícono de cuadrado en el lado izquierdo).
     - Busca `rust-analyzer` e instálalo.
   - **Instalar herramientas adicionales de Rust:**
     - Clippy (para análisis estático de código):
       ```bash
       rustup component add clippy
       ```
     - Rustfmt (para formateo automático de código):
       ```bash
       rustup component add rustfmt
       ```
