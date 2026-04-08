INSTALACIÓN APP CONDUCTOR - FASE 6
===================================

1. INSTALAR DEPENDENCIAS
   npm install

   o

   yarn install

2. CONFIGURAR API
   Editar src/config/api.js y cambiar:
   - API_BASE_URL en desarrollo: http://TU_IP_LOCAL:8000/api
   - API_BASE_URL en producción: https://api.mudanzascrm.com/api

3. INICIAR LA APP
   npm start

   Luego presionar:
   - 'a' para Android
   - 'i' para iOS
   - 'w' para web

4. CREDENCIALES DE PRUEBA (Conductor)
   Email: conductor@mudanzas.com
   Password: [contraseña del conductor creado en Django admin]

ESTRUCTURA DEL PROYECTO
========================
src/
├── config/           # Configuración de API
├── context/          # Context API (AuthContext)
├── navigation/       # Navegación (React Navigation)
├── screens/          # Pantallas de la app
│   ├── LoginScreen.js
│   ├── ServiciosScreen.js
│   ├── DetalleServicioScreen.js
│   ├── PlanCargaScreen.js
│   └── FirmaScreen.js
└── services/         # Servicios API
    ├── api.js
    ├── auth.js
    └── servicio.js

FUNCIONALIDADES IMPLEMENTADAS
==============================
✅ Login de conductor/cargador
✅ Lista de servicios asignados
✅ Detalle del servicio con timeline
✅ Cambio de estados con GPS automático
✅ Plan de carga con checklist (cargando/descargando)
✅ Captura de firma del cliente
✅ Navegación a Google Maps
✅ Notificaciones en tiempo real al cliente

FLUJO DE ESTADOS
=================
1. asignado → 2. en_camino → 3. en_origen → 4. cargando →
5. en_ruta → 6. en_destino → 7. descargando → 8. completado

PERMISOS NECESARIOS
===================
- Ubicación (GPS)
- Cámara (para firmas)
- Almacenamiento (para cache)
