# 👑 PADRINO SAVE VAULT — Guía de Instalación y Uso Oficial

> **Herramienta:** Padrino Save Vault (Gestor Universal de Partidas para PS5)  
> **Firmwares Compatibles:** 3.00 hasta 13.60 (CFI-1000/1100/1200 Fat, CFI-2000 Slim y PS5 Pro)  
> **Requisitos:** Consola PlayStation 5 con Jailbreak activo (etaHEN, Relapse, ShadowMount o Webkit/Netcat) y un Disco Duro Externo USB (exFAT/FAT32).

---

## 🚀 Método 1: Instalación en Payload Manager (Recomendado)

Si tu consola cuenta con **etaHEN** o **ItemzFlow**:

1. Conecta con la PS5 a través de **FTP** o **Web File Manager**.
2. Navega a la ruta de payloads en el almacenamiento interno:
   ```
   /data/payloads/
   ```
   *(o crea la carpeta `/mnt/usb0/payloads/` directamente en tu disco duro externo o pendrive)*.
3. Copia el archivo `PadrinoSaveVault.elf` en esa carpeta.
4. En el menú de tu PS5, entra a **Payload Manager**.
5. Verás en la lista:  
   👉 **`[📦] PadrinoSaveVault.elf`**
6. Presiona **X** para ejecutarlo.

---

## 🌐 Método 2: Inyección Clásica por Red (Netcat)

1. En tu PS5 abre el navegador web y carga el Jailbreak (Webkit / BD-JB).
2. Asegúrate de que el **ELF Loader** esté esperando en el puerto `9020` o `9021`.
3. Desde tu PC (usando Netcat GUI o terminal):
   ```bash
   nc -w 3 <IP_DE_TU_PS5> 9020 < PadrinoSaveVault.elf
   ```
4. El televisor mostrará inmediatamente el pop-up de inicio de Padrino Save Vault.

---

## 🖥️ Cómo Acceder al Dashboard y Pantalla de Carga

Padrino Save Vault levanta automáticamente su interfaz visual:
* **En el Televisor:** Si tienes instalado el lanzador visual homebrew en pantalla.
* **Desde tu Teléfono Móvil o PC:** Con tu móvil o PC conectado al mismo WiFi de la consola, abre el navegador y entra a:
  ```
  http://<IP_DE_TU_PS5>:1455
  ```
  Verás la **Pantalla de Carga Splash 1080p** y el **Dashboard Interactivo Obsidian & Gold**, con el medidor de tu disco duro externo y los botones de respaldo y restauración.

---

## 💾 ¿Cómo Respaldar tus Partidas al Disco Externo?

1. Conecta tu **Disco Duro Externo USB** (formateado en exFAT o FAT32) en cualquiera de los puertos traseros USB 3.2 de la PS5.
2. En el Dashboard presiona el botón:  
   👉 **`[ 🚀 Respaldar Todo el Progreso ]`** *(o simplemente ejecuta el `.elf` sin argumentos)*.
3. El sistema comenzará a copiar a más de **140 MB/s**:
   * Partidas de PS5 (`savedata_ps5/`).
   * Partidas de PS4 (`savedata/`) y sus archivos criptográficos esenciales `keystone`.
   * Bases de datos del sistema `savedata.db` y trofeos locales.
4. Al finalizar, la pantalla mostrará:  
   `"✅ ¡Respaldo completado con éxito! Tus partidas están seguras en el disco externo."`

---

## 🔄 ¿Cómo Restaurar tus Partidas tras un Formateo o Brick?

Si tuviste que reinstalar el software del sistema o formatear la PS5:

1. Vuelve a conectar tu disco duro externo con los backups a la PS5.
2. Abre Padrino Save Vault.
3. El sistema detectará automáticamente tu copia de seguridad anterior.
4. Presiona el botón:  
   👉 **`[ 🔄 Restaurar desde el Disco ]`**
5. El motor de Padrino Save Vault:
   * **Re-vincula tu cuenta automáticamente:** Asocia las partidas a tu usuario activo actual sin importar si el ID cambió.
   * **Restaura los keystones:** Evita para siempre el error de *"Datos Dañados"*.
   * **Indexa las partidas:** Actualiza la base de datos `savedata.db` para que el sistema las reconozca al instante.
   * **Asigna permisos `chmod 0777`:** Permitiendo que los juegos lean y guarden partidas con normalidad.
6. ¡Listo! Al abrir tus juegos continuará tu partida exactamente donde la dejaste.
