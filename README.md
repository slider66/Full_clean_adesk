# Limpiador de Residuos Autodesk

## ⚠️ ADVERTENCIA IMPORTANTE ⚠️

Este script está diseñado para eliminar residuos de instalaciones de software Autodesk **SOLO DESPUÉS** de haber desinstalado el software mediante el desinstalador oficial de Windows o el desinstalador de Autodesk.

**NO UTILICE ESTE SCRIPT SI:**
- Todavía tiene instalado algún software de Autodesk que desea mantener
- No ha desinstalado el software mediante el método oficial
- Tiene dudas sobre si algún programa de Autodesk está en uso

## Descripción

Este script elimina archivos residuales y entradas del registro de Windows relacionadas con productos Autodesk. Es útil cuando:
- La desinstalación oficial no eliminó todos los archivos
- Quiere asegurarse de que no quedan rastros de instalaciones anteriores
- Está teniendo problemas para reinstalar software de Autodesk

## Requisitos

- Windows 10 o superior
- Privilegios de administrador
- Python 3.6 o superior
- Módulos Python requeridos:
  - os
  - shutil
  - subprocess
  - ctypes
  - logging
  - datetime

## Instrucciones de Uso

1. **IMPORTANTE**: Desinstale primero todos los productos Autodesk que desee eliminar mediante:
   - Panel de Control > Programas y características
   - O el desinstalador oficial de Autodesk

2. Ejecute el script como administrador:
   ```powershell
   python remove_autodesk.py
   ```

3. El script le pedirá confirmación antes de proceder

4. Se creará un archivo de log con el nombre `autodesk_cleanup_YYYYMMDD_HHMMSS.log`

## Qué hace el script

1. **Elimina carpetas**:
   - C:\Program Files\Autodesk
   - C:\Program Files (x86)\Autodesk
   - C:\ProgramData\Autodesk
   - Carpetas de AppData (Local y Roaming)
   - Carpetas de documentos
   - Archivos temporales relacionados con Autodesk

2. **Elimina claves del registro**:
   - HKEY_LOCAL_MACHINE\SOFTWARE\Autodesk
   - HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Autodesk
   - HKEY_CURRENT_USER\SOFTWARE\Autodesk
   - HKEY_CLASSES_ROOT\Autodesk

## Precauciones

1. **Haga una copia de seguridad** de su sistema antes de ejecutar el script
2. Asegúrese de que no tiene ningún software de Autodesk en ejecución
3. Verifique que realmente ha desinstalado todo el software que desea eliminar
4. Si tiene dudas, consulte con el soporte técnico de Autodesk

## Limitaciones

- El script no puede eliminar archivos que están en uso por otros procesos
- Algunas claves del registro pueden requerir permisos adicionales
- No elimina configuraciones personalizadas guardadas en otros lugares

## Solución de Problemas

Si encuentra errores:
1. Revise el archivo de log generado
2. Asegúrese de tener privilegios de administrador
3. Cierre todos los programas relacionados con Autodesk
4. Intente ejecutar el script en modo seguro

## Soporte

Este script se proporciona "tal cual" sin garantías. Si necesita ayuda:
1. Revise la documentación oficial de Autodesk
2. Contacte al soporte técnico de Autodesk
3. Consulte con un profesional de TI

## Licencia

Este script es de uso libre, pero se recomienda encarecidamente seguir las instrucciones y advertencias proporcionadas.

## Historial de Cambios

- v1.0: Versión inicial
- v1.1: Mejoras en el manejo de errores y logging
- v1.2: Mejor manejo de archivos en uso y carpetas temporales 