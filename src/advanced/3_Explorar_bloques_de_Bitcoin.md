## **Explorar bloques de Bitcoin:**
  
   - Decodificar un bloque desde un archivo en formato binario.
   - Extraer las transacciones y analizarlas.
  
   - **_Guía_**
  
       ### 1. **Conceptos Previos**
       **Bloques de Bitcoin:**
       - Cada bloque contiene un conjunto de transacciones y un encabezado que incluye información crítica como el hash previo y el nonce.
       **Estructura de un Bloque:**
       - Encabezado: Hash previo, Merkle root, timestamp, etc.
       - Transacciones: Lista de transacciones incluidas en el bloque.
  
       ***
  
       ### 2. **Objetivo del Ejercicio**
       Decodificar un bloque en formato binario, extraer sus transacciones, y analizar su contenido.
  
       ***
  
       ### 3. **Pasos Detallados**
       **Paso 1: Leer un archivo de bloque**
       - Carga un archivo que contenga un bloque en formato binario.
       **Paso 2: Decodificar el bloque**
       - Usa funciones de `rust-bitcoin` para parsear el encabezado y las transacciones.
       **Paso 3: Analizar las transacciones**
       - Extrae detalles como direcciones de entrada/salida y valores.
  
       ***
  
       ### 4. **Código Base**
       ```rust
       extern crate bitcoin;

       use bitcoin::consensus::deserialize;
       use bitcoin::blockdata::block::Block;

       fn main() {
           // Leer un archivo binario que contiene un bloque (reemplazar con datos reales)
           let block_data = include_bytes!("block.dat");

           // Decodificar el bloque
           let block: Block = deserialize(block_data).unwrap();

           // Analizar el bloque
           println!("Bloque decodificado: {:?}", block);
       }

       ```
       
       ***
       
       ### 5. **Tareas para Resolver**
       1. Decodifica un bloque real desde un archivo.
       2. Extrae y analiza las transacciones incluidas en el bloque.
       
       ***
       
       ### 6. **Validación**
       - Compara los datos extraídos con los de un explorador de bloques.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio ayuda a entender la estructura interna de los bloques y cómo se conectan a la cadena.
