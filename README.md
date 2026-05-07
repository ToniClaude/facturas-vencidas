# 📋 Seguimiento de Facturas Vencidas

App simple de HTML puro para seguimiento de facturas vencidas integrada con Supabase.

## Características

- ✅ Listado de facturas con días vencidos
- ✅ Filtros por empresa, local, estado y días
- ✅ Registro de gestiones (seguimiento de cada factura)
- ✅ Cambio de estado (activa/pagada/descartada)
- ✅ Estadísticas (total, importe, días promedio)
- ✅ Acceso protegido con clave en URL

## Uso local

```bash
# Opción 1: Python
python3 -m http.server 3000

# Opción 2: Node
npx http-server -p 3000

# Opción 3: Live Server (VS Code)
# Abre en navegador: http://localhost:3000/?key=MICLAVE123
```

## Despliegue en Vercel

```bash
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/TU_USUARIO/facturas-vencidas.git
git push -u origin main
```

Luego:
1. Ve a [Vercel](https://vercel.com)
2. Importa el repositorio
3. Deploy automático

## Configuración

**Cambiar clave de acceso:**
- Edita `REQUIRED_KEY` en `index.html`
- Accede con: `https://tu-app.vercel.app/?key=tu-clave`

**URLs de Supabase:**
- Ya configuradas en `index.html`
- Proyecto: `gastos-familiares`
- Tablas: `facturas`, `gestiones`, `estados`

## Tablas en Supabase

- `facturas`: ID, días, empresa, local, importe, fecha, forma, plazo
- `gestiones`: Registro de seguimiento por factura
- `estados`: Estado actual de cada factura (activa/pagada/descartada)
