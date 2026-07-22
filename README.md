# SubliStudio — Frontend

Aplicación web de la plataforma de membresía SubliStudio. Angular 22 (standalone, sin SSR por ahora).

Ver `../documentacion-sublistudio/plan-de-trabajo-sublistudio-02.md` (fases) y `../documentacion-sublistudio/adr-sublistudio.md` (decisiones de arquitectura).

## Requisitos

- Node.js 20+
- Backend corriendo en `http://localhost:3000` (repo `sublistudio-backend`)

## Puesta en marcha

```bash
npm install
npm start
```

- App: http://localhost:4200

## Entornos

| Archivo | Uso |
|---|---|
| `src/environments/environment.ts` | Desarrollo (`apiUrl: http://localhost:3000`) |
| `src/environments/environment.production.ts` | Producción (actualizar `apiUrl`) |

## Estructura

```
src/app/
  core/api/        servicios que consumen el backend (ej. health.service.ts)
  app.config.ts     providers globales (router, http client)
  app.routes.ts      definición de rutas
```

## Scripts

| Comando | Descripción |
|---|---|
| `npm start` | Arranca `ng serve` en modo desarrollo |
| `npm run build` | Build de producción a `dist/` |
| `npm test` | Tests unitarios (Vitest) |
