<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheethouse.svg" width="96" alt="Sheethouse logo">
</p>

<h1 align="center">Sheethouse</h1>

<p align="center"><b>A columnar OLAP engine — spreadsheets are already columnar.</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> project · the spreadsheet-native <b>ClickHouse</b></p>

---

**Status:** 📝 Unsaved Draft (design). Data & Storage TAG.

## The mapping

- Columns are the native storage; **GROUP BY / aggregations** via `QUERY()` and **pivot tables** (OLAP cubes for free).
- **materialized view** = a tab recomputed by a trigger; **partitions** = sheets by date.

## Honest limit

ClickHouse's point is **billions of rows, fast** — here the ceiling is ~10M cells and aggregations are slow. Toy OLAP, real semantics.

## Connect with real clients

Paired with [SheetWire](https://github.com/sncfoundation/sheetwire), real ClickHouse clients can connect to a Google Sheet over the native wire protocol.

- 🗺️ [SNCF Landscape](https://sncfoundation.github.io/landscape.html) · 🧩 [Projects](https://sncfoundation.github.io/projects.html) · 🎓 [Certification](https://sncfoundation.github.io/certification.html)

---

<sub>Apache-2.0. Do not run production data on a spreadsheet. If you do, please film the query plan.</sub>
