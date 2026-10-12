# Acta de Sprint Review y Retrospectiva

> [!NOTE]
> **Asignatura:** Desarrollo de Software II  
> **Proyecto:** ManosSeguras (Persistencia Local)  
> **Docente:** Mtro. Ing. Yover Collantes Valer  
> **Fecha y hora de inicio:** 11 de octubre de 2026 – 11:00 AM

---

## 1. Asistentes

* **Product Owner / Docente:** Mtro. Ing. Yover Collantes Valer
* **Scrum Master:** Cardenas Carrasco, Leonardo
* **Equipo de Desarrollo (Developers):**
  * Vitorino Duran, Davis Shumager
  * Quispe Dávila, Jose Jose
  * Yabar Latorre, Gonzalo Eduardo

---

## 2. Lo que se mostró en la Sprint Review

* **Capa de Persistencia Local Offline-First:** Demostración del funcionamiento de la base de datos local SQLite utilizando `drift` en arquitectura por capas (Domain, Data, Presentation).
* **Operaciones CRUD y Estado de Auditorías:** Registro, consulta, edición y borrado lógico de auditorías de higiene de manos con almacenamiento de oportunidades.
* **Indicador Nacional OMS Offline-First:** Estrategia de tres niveles en la consulta del indicador (servicio remoto, caché local con vigencia TTL de 24 horas y respaldo empaquetado en `assets`) e insignia indicadora de origen en la interfaz de usuario.
* **Migración de Esquema `v1 → v2`:** Incorporación de la columna `observacion_general` en la tabla `auditorias` sin pérdida de datos existentes y verificada con pruebas automatizadas.
* **Integridad Referencial y Calidad:** Verificación de restricciones de claves foráneas activas (`PRAGMA foreign_keys = ON`), ejecución de `flutter analyze` sin hallazgos y suite de pruebas en verde.

---

## 3. Acuerdos Alcanzados

* **Aprobación del Incremento:** Validar y dar por completado el incremento correspondiente al Sprint de la Semana 10 (Persistencia Local).
* **Continuidad del Backlog:** Trabajar en los siguientes sprints el almacenamiento seguro (Semana 11), gestión de estado con Riverpod (Semanas 12 y 13) y la sincronización con la nube mediante Cloud Firestore (Semana 16).
* **Métricas de Rendimiento:** Ejecutar la medición pendiente del efecto de los índices en consultas para el próximo Sprint.

---

## 4. Puntos de la Retrospectiva (Sprint Retrospective)

### 1. Estructura y Migración de Código
* **Qué funcionó bien:** La base con anotaciones `TODO` permitió ubicar rápidamente lo pendiente, y la prueba automatizada de migración `v1 → v2` dio seguridad de no perder datos.
* **Qué mejorar:** Había comentarios `TODO` desactualizados en el código base.
* **Acción concreta:** Leer y revisar detalladamente el código antes de asumir que falta una funcionalidad.
* **Responsable:** Cardenas Carrasco, Leonardo.

### 2. Ejecución y Verificación de Pruebas
* **Qué funcionó bien:** Las pruebas automatizadas dieron confianza al realizar cambios estructurales en el esquema.
* **Qué mejorar:** Se presentaron fallos temporales en pruebas por tener archivos sin guardar en el editor.
* **Acción concreta:** Guardar explícitamente todos los archivos modificados antes de ejecutar `flutter test`.
* **Responsable:** Vitorino Duran, Davis Shumager.

### 3. Distribución del Trabajo en el Repositorio
* **Qué funcionó bien:** Cumplimiento de las historias principales planificadas para el sprint.
* **Qué mejorar:** El trabajo se concentró en pocas personas y el historial de commits debe reflejar mejor la participación de todo el equipo.
* **Acción concreta:** Repartir equitativamente la asignación de historias y commits desde la sesión de Sprint Planning.
* **Responsable:** Quispe Dávila, Jose Jose y Yabar Latorre, Gonzalo Eduardo.

---

## 5. Porcentaje de Aporte Declarado por Integrante

| Integrante | Rol | Porcentaje de Participación Declarado |
| :--- | :--- | :---: |
| **Cardenas Carrasco, Leonardo** | Scrum Master / Developer | 100% |
| **Vitorino Duran, Davis Shumager** | Developer | 100% |
| **Quispe Dávila, Jose Jose** | Developer | 100% |
| **Yabar Latorre, Gonzalo Eduardo** | Developer | 100% |

> [!TIP]
> *Cada integrante declara el 100% de cumplimiento sobre las responsabilidades asignadas dentro del equipo para esta entrega.*
