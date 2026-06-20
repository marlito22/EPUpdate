# EP Update

Repositorio publico de actualizaciones para `EP`, el sistema de escritorio `EPC` del ecosistema EP.

## Version actual

- Version: `1.0.4.11`
- Instalador Windows x64: <https://github.com/marlito22/EPUpdate/releases/download/v1.0.4.11/EP-Setup-v1.0.4.11-win-x64.exe>
- Paquete ZIP para actualizacion automatica: <https://github.com/marlito22/EPUpdate/releases/download/v1.0.4.11/EP-v1.0.4.11-win-x64-self-contained.zip>
- Release: <https://github.com/marlito22/EPUpdate/releases/tag/v1.0.4.11>

## Que es EP

`EP` es una solucion de escritorio WPF orientada a operacion comercial y administrativa. El cliente principal es `EPC`, que trabaja junto con `EP.Servicios` como backend local para logica de negocio, sincronizacion y actualizaciones funcionales por dominio.

## Funcionalidades principales del software

- Aplicacion y shell principal: login, sesion activa, splash, ventana principal, navegacion por modulos, menus segun tipo de negocio, alertas DIAN y avisos de lotes por vencer.
- Configuracion inicial e instalacion operativa: validacion de prerrequisitos, preparacion de entorno local, configuracion inicial y arranque del servicio `EP.Servicios`.
- Ventas y facturacion: ventas de mostrador, documentos de facturacion, conversion desde cotizaciones, planes separe y entregas parciales.
- Caja y tesoreria: apertura de turnos, movimientos, arqueos, cuadres y cierres de caja.
- Cartera: manejo de saldos de clientes y proveedores, pagos, abonos y saldo a favor.
- Cotizaciones: creacion, actualizacion, anulacion y conversion posterior a factura.
- Plan separe: registro, seguimiento, abonos, cancelacion y carga a facturacion.
- Entrega parcial: remisiones, detalle de entregas, abonos, devoluciones y carga a factura.
- Compras y devoluciones de compra: registro de compras, medios de pago asociados y devoluciones enlazadas al flujo de inventario y cartera.
- Clientes, proveedores y vendedores: CRUD, validaciones, soporte de importacion y exportacion, y operaciones relacionadas con multiempresa.
- Catalogo de productos: administracion de productos, clasificaciones, homologaciones y estructuras del catalogo.
- Inventario y bodegas: existencias, movimientos, documentos, kardex, conteos, etiquetas, lotes, bodegas y consultas operativas.
- Reportes: consultas y salidas por dominio para operacion administrativa y comercial.
- Herramientas: utilidades auxiliares del sistema y exportaciones de apoyo a la operacion.
- DIAN y facturacion electronica: soporte para rangos, numeracion, validaciones y seguimiento de componentes asociados a DIAN.
- Multiempresa: vinculos interempresa, sincronizacion de productos y transferencias entre sedes o empresas.
- Negocios especiales y minimarket: comportamientos adaptados a flujos particulares del negocio, incluyendo escenarios de POS y operaciones especializadas.
- Configuracion y contexto operativo: parametros de trabajo, identidad local, contexto de sede/empresa y ajustes funcionales del sistema.
- Licencias y plataforma administrativa: validacion de licencia, estado de version y administracion de componentes transversales de plataforma.

## Como se instala y actualiza

### Instalacion inicial

1. Ejecutar el instalador `.exe` como administrador.
2. El instalador copia `EPC` y deja `EP.Servicios.Host` dentro de la carpeta de `EPC`.
3. En el primer arranque, `EPC` crea o repara el servicio `EP.Servicios` usando esos binarios locales.
4. A partir de ese momento, `EPC` y `EP.Servicios` trabajan juntos en el mismo equipo.

### Actualizacion automatica

1. `EPC` consulta la ultima release publicada en este repositorio.
2. Si existe una version superior, descarga el asset `.zip`.
3. Antes de reemplazar archivos, intenta detener `EP.Servicios`.
4. El paquete actualiza tanto `EPC` como `EP.Servicios.Host`.
5. Al terminar, `EPC` intenta iniciar otra vez `EP.Servicios`.

## Archivos publicados

- `actualizacion.xml`: manifiesto compatible con el actualizador anterior.
- `version.json`: metadata de version para integraciones nuevas.
- `cambios.html`: resumen publico de cambios.

Los instaladores y paquetes grandes se publican como assets del Release para evitar subir binarios pesados directamente a `gh-pages`.
