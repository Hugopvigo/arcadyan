<p align="center">
  <img src="docs/capturas/00-cabecera.png" alt="Arcadyan — registro de contribuciones con marca de tiempo" width="100%">
</p>

<p align="center">
  <b>Un registro de actividad con marca de tiempo, generado automáticamente.</b><br>
  Casi cinco años de entradas «Contribution» en texto plano, archivados en Git.
</p>

<p align="center">
  <img alt="licencia" src="https://img.shields.io/badge/licencia-CC%20BY--NC--SA%204.0-8E8E93?style=flat-square&labelColor=1a1a1e">
  <img alt="formato" src="https://img.shields.io/badge/formato-texto%20plano-ff5f5f7?style=flat-square&labelColor=1a1a1e">
  <img alt="historial" src="https://img.shields.io/badge/historial-2021--2026-3DDC84?style=flat-square&labelColor=1a1a1e">
</p>

---

## Qué es esto

Un archivo de texto con **2.973 marcas de tiempo**, una por línea, con el
formato `Contribution: AAAA-MM-DD HH:MM`:

```
Contribution: 2021-05-12 20:08
Contribution: 2021-05-12 20:09
Contribution: 2026-04-23 20:06
```

El historial va del **12 de mayo de 2021** al **23 de abril de 2026**, con
registro en **535 días distintos**:

| Año | Entradas |
|---|---|
| 2021 | 432 |
| 2022 | 692 |
| 2023 | 525 |
| 2024 | 580 |
| 2025 | 554 |
| 2026 | 190 |

Todas las entradas caen entre las **20:00 y las 20:09**. Cada día con
actividad lleva entre 1 y 10 marcas, y el reparto está muy igualado: hay 40
días con una sola marca y 46 con diez.

El repositorio no guarda código: el registro vivía dentro del `README.md`
—95 KB de líneas sin explicación— y ahora está en
[`docs/contribuciones.txt`](docs/contribuciones.txt), sin tocar.

## Cómo consultarlo

```bash
# primeras y últimas entradas
head docs/contribuciones.txt
tail docs/contribuciones.txt

# cuántas hay en total
wc -l docs/contribuciones.txt

# cuántas por año
awk '{print substr($2, 1, 4)}' docs/contribuciones.txt | sort | uniq -c

# cuántas por mes
awk '{print substr($2, 1, 7)}' docs/contribuciones.txt | sort | uniq -c

# las entradas de un día concreto
grep "2026-01-21" docs/contribuciones.txt
```

## Estructura

```
arcadyan/
├── docs/contribuciones.txt   2.973 marcas de tiempo
├── docs/capturas/             cabecera del README
└── LICENSE                    CC BY-NC-SA 4.0
```

## Licencia

**CC BY-NC-SA 4.0** — se puede compartir y adaptar con atribución, siempre sin
uso comercial y bajo la misma licencia. Texto completo en
[LICENSE](LICENSE).

---

<div align="center">
  Hugo Pérez Vigo · [@hugopvigo](https://x.com/hugopvigo) ·
  [github.com/Hugopvigo](https://github.com/Hugopvigo)
</div>
