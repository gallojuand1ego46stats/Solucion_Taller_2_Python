# Solución Taller 2 — Python para APIs e IA (Corte II)

Repositorio de grupo para el **Taller del Corte II — "Pólizas API v0"**, del curso *Python para Desarrollo de APIs e Inteligencia Artificial* (USTA, 2026-II). Clonado del semilla [`JotaMao1985/polizas-api-v0`](https://github.com/JotaMao1985/polizas-api-v0), que arranca y persiste pero arrastra defectos deliberados de configuración, persistencia, contratos HTTP y tests (módulos 6 a 11).

El objetivo: diagnosticar el servicio, refactorizarlo con restricciones concretas, medir y justificar la estrategia de carga de relaciones de SQLAlchemy, auditar una batería de tests generada por IA, y sustentarlo.

## Equipo

| Integrante | Parte(s) a cargo |
|---|---|
| Integrante 1 | A — Diagnóstico · D — Auditoría de tests de IA |
| Integrante 2 | B — Refactor con restricciones |
| Integrante 3 | C — Carga de relaciones · E — Bitácora y sustentación |

(Identidades de Git de cada integrante en `EQUIPO.md`.)

## Estructura de ramas

| Rama | Contenido |
|---|---|
| `main` | Código congelado para entrega — recibe cambios solo vía Pull Request |
| `parte-a-diagnostico` | Hallazgos del diagnóstico (`HALLAZGOS.md`) |
| `parte-b-refactor` | Refactor del servicio (restricciones B1–B10) |
| `parte-c-carga-relaciones` | Estrategias de carga y medición de consultas (`CONSULTAS.csv`) |
| `parte-d-auditoria-ia` | Auditoría de tests generados por IA (`DICTAMEN_IA.md`, `tests/test_ia_corregido.py`) |
| `parte-e-bitacora-sustentacion` | Bitácora de uso de IA (`BITACORA_IA.md`) y preparación de sustentación |

## Puesta en marcha

```bash
pip install -r requirements.txt
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

### En contenedor

```bash
docker build -t polizas-api .
docker run -p 8000:8000 polizas-api
```

## Entregables (plantillas en `plantillas/`)

`EQUIPO.md` · `HALLAZGOS.md` · `CONSULTAS.csv` · `DICTAMEN_IA.md` · `BITACORA_IA.md`

## Entrega

Plazo: **16 de octubre de 2026, 23:59**. El commit del semilla se conserva en el historial de este repositorio.
