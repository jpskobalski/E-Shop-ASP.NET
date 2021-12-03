# Feedback 📢

# Table of Contents
1. [Entrega 1](#entrega-1)
2. [Entrega 2](#entrega-2)

## entrega-1

Muy bien en general, pocas pequeñas cositas para comentarles en esta entrega: 

Aunque sea de la segunda entrega ya que lo hicieron les doy feedback respecto a las validaciones: todas las validaciones deben ir con sus correspondientes mensajes de error (les puse como ejemplo la propiedad `Nombre` de la clase `Usuario` para que tengan como guía).

Cuando apliquen restricciones a un modelo (por ejemplo con `[Required]`) fíjense que no se quiera aplicar sobre una propiedad que sea del tipo Referencia (por ejemplo una clase), porque en ese caso van a tener problemas después (por ejemplo en la clase `Producto` la propiedad `Categoria` no debe estar marcada como `[Required]`).

### Clase Usuario

- Todavía no se vio el tema en clase, pero la propiedad `Password` la ponemos como tipo array de bytes para almacenarla encriptada.

## entrega-2

- Una vez más chicos, muy buen laburo. Está muy bien encarado el tp.
- Lo único que les corrijo es algo que les dije en clase y me faltó pasarles un parámetro para crear los scaffolding (por supuesto que es culpa mía que se me olvidó pasarles el parámetro, el `-udl` para que tome el default `Layout` en lugar de ponerles null). 
El comando completo sería:
```bash
dotnet aspnet-codegenerator controller -m MODELO_CON_NAMESPACE -dc DB_CONTEXT_NAMESPACE -name NOMBRE_DEL_CONTROLADOR -outDir Controllers -async -scripts -udl -f
```

```bash
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Sucursal -dc tp_nt1.Database.CarritoDbContext -name SucursalesController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.StockItem -dc tp_nt1.Database.CarritoDbContext -name StockItemsController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Carrito -dc tp_nt1.Database.CarritoDbContext -name CarritosController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.CarritoItem -dc tp_nt1.Database.CarritoDbContext -name CarritoItemsController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Categoria -dc tp_nt1.Database.CarritoDbContext -name CategoriasController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Cliente -dc tp_nt1.Database.CarritoDbContext -name ClientesController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Compra -dc tp_nt1.Database.CarritoDbContext -name ComprasController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Empleado -dc tp_nt1.Database.CarritoDbContext -name EmpleadosController -outDir Controllers -async -scripts -udl -f
dotnet aspnet-codegenerator controller -m tp_nt1.Models.Producto -dc tp_nt1.Database.CarritoDbContext -name ProductosController -outDir Controllers -async -scripts -udl -f
```
