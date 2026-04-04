# 🏆 Polla Mundialista · FIFA 2026

> Aplicación web para gestionar predicciones del Mundial de Fútbol FIFA 2026 (Canadá · México · USA). Permite a los participantes registrar sus pronósticos de partidos, predecir el podio final y competir en un ranking en tiempo real.
>
> ## 📌 Repositorios del Proyecto
>
> | Repositorio | Enlace |
> |-------------|--------|
> | Frontend (React) | _Próximamente_ |
> | Backend (API) | _Próximamente_ |
> | **Documentación** | [wc2026-polla-docs](https://github.com/efgonzalezca/wc2026-polla-docs) |

---

## 🔐 Autenticación

### Login

Pantalla de inicio con **contador regresivo** hasta el inicio del torneo, formulario de acceso con correo electrónico y contraseña, enlace para recuperar contraseña y opción para registrarse.

![Login](01-login.png)

📱 **Vista Mobile (390×844)**

![Login Mobile](01-login-mobile.png)

### Registro

Formulario completo con: correo electrónico, nickname (alias), nombres, apellidos, celular (con código de país +57), contraseña y confirmación.

![Registro](02-registro.png)

📱 **Vista Mobile (390×844)**

![Registro Mobile](02-registro-mobile.png)

---

## ⚽ Partidos — Fase de Grupos

Muestra los **96 partidos** de la Fase de Grupos divididos en 12 grupos (A–L). Cada tarjeta incluye: fecha y hora, banderas y nombres de equipos, resultado final, predicción del usuario y puntos obtenidos.

![Partidos Fase de Grupos](03-partidos-fase-grupos.png)

📱 **Vista Mobile (390×844)**

![Partidos Fase de Grupos Mobile](03-partidos-fase-grupos-mobile.png)

### Modal: Detalle del Partido

Al hacer clic en "Ver Detalles..." se abre un modal con: resultado real, predicción del usuario, puntos obtenidos, y una tabla comparativa con las predicciones de todos los participantes.

![Modal Detalle](04-modal-detalle.png)

📱 **Vista Mobile (390×844)**

![Modal Detalle Mobile](04-modal-detalle-mobile.png)

---

## 🏟️ Partidos — Eliminatorias

Vista tipo bracket que representa el árbol completo del torneo: Dieciseisavos → Octavos → Cuartos → Semifinal → Final → Semifinal → 3er Puesto. Los usuarios pueden ingresar sus predicciones directamente en el bracket.

![Eliminatorias](05-eliminatorias.png)

📱 **Vista Mobile (390×844)**

![Eliminatorias Mobile](05-eliminatorias-mobile.png)

---

## 📊 Clasificación

Ranking en tiempo real con podio visual (Top 3 con medallas 🥇🥈🥉) y tabla completa mostrando: posición, participante, puntos por partidos, puntos por podio y total.

![Clasificación](06-clasificacion.png)

📱 **Vista Mobile (390×844)**

![Clasificación Mobile](06-clasificacion-mobile.png)

---

## 🏅 Predicción de Podio

Permite predecir Campeón (+30 pts), Subcampeón (+20 pts) y 3er Lugar (+10 pts) con fecha límite antes de la final. Incluye podio visual interactivo y selección mediante dropdowns.

![Podio](07-podio.png)

📱 **Vista Mobile (390×844)**

![Podio Mobile](07-podio-mobile.png)

---

## 🌎 Equipos

Los **48 equipos** participantes organizados en 12 grupos (A–L), mostrando bandera, código FIFA, nombre completo y **ranking FIFA** actual.

![Equipos](08-equipos.png)

📱 **Vista Mobile (390×844)**

![Equipos Mobile](08-equipos-mobile.png)

---

## 🧮 Simulador de Puntos

Herramienta didáctica para calcular cuántos puntos obtendrías con una predicción. Muestra desglose detallado: acertar resultado (+2), goles local (+1), goles visitante (+1), bonus exacto (+3), bonus empate (+1). **Máximo: 7 pts por partido.**

![Simulador](09-simulador.png)

📱 **Vista Mobile (390×844)**

![Simulador Mobile](09-simulador-mobile.png)

---

## 📖 Reglamento

Reglas completas organizadas en acordeones: Sistema de Puntuación, Puntos de Podio, Distribución de Premios, Ejemplos de Cálculo y Reglas Generales.

![Reglamento](10-reglamento.png)

📱 **Vista Mobile (390×844)**

![Reglamento Mobile](10-reglamento-mobile.png)

---

## 🛡️ Panel de Administración

> Acceso exclusivo para usuarios con rol **admin**. El botón "Administrar" aparece en el sidebar solo con cuentas administradoras.

### Administrar Resultados — Fase de Grupos

Vista de todos los partidos organizados por fase (Fase de Grupos, Dieciseisavos, Octavos, Cuartos, Semifinales, 3er Puesto, Final) con filtro por grupo. Contador de partidos jugados vs pendientes.

![Admin Panel](11-admin-panel.png)

📱 **Vista Mobile (390×844)**

![Admin Panel Mobile](11-admin-panel-mobile.png)

### Administrar Resultados — Dieciseisavos (Pendientes)

Los partidos pendientes tienen campos editables inline para ingresar goles. El admin ingresa el marcador y confirma con el botón ✓ azul. El sistema recalcula automáticamente los puntos de todos los participantes.

![Admin Dieciseisavos](12-admin-dieciseisavos.png)

📱 **Vista Mobile (390×844)**

![Admin Dieciseisavos Mobile](12-admin-dieciseisavos-mobile.png)

---

## 🎯 Sistema de Puntuación

### Por partido (máximo 7 puntos)

| Criterio | Puntos |
|----------|--------|
| Acertar resultado (G/E/P) | +2 pts |
| Acertar goles local | +1 pt |
| Acertar goles visitante | +1 pt |
| Bonus marcador exacto | +3 pts |
| Bonus empate no exacto | +1 pt |
| **Total máximo** | **7 pts** |

### Por predicción de podio

| Posición | Puntos |
|----------|--------|
| 🥇 Campeón | +30 pts |
| 🥈 Subcampeón | +20 pts |
| 🥉 3er Lugar | +10 pts |

---

## 🗂️ Navegación

| Sección | Ruta | Rol |
|---------|------|-----|
| Partidos | `/` | Todos |
| Clasificación | `/ranking` | Todos |
| Podio | `/podium` | Todos |
| Equipos | `/teams` | Todos |
| Simulador | `/simulator` | Todos |
| Reglamento | `/rules` | Todos |
| Administrar | `/admin` | Solo admin |

---

## 🛠️ Stack Tecnológico

- **Frontend**: React + Vite
- **Estilos**: CSS con diseño responsive
- **Autenticación**: Sistema de login con sesiones y roles (admin / usuario)
- **Tiempo real**: Ranking actualizado en tiempo real

---

*Documentación generada mediante recorrido automatizado de la aplicación · FIFA 2026™ · Canadá · México · USA*
