# Architecture

Kaushal Lens is currently a static frontend prototype.

```mermaid
flowchart TD
    A[Published government datasets] --> B[Embedded JS data]
    B --> C[Dashboard calculations]
    C --> D[HTML/CSS interface]
    C --> E[Chart.js charts]
    C --> F[Tables and observations]
```

## Current implementation

- `index.html` contains the interface, styles, data and application logic.
- Chart.js provides visualisations.
- No server-side API is required.
- No database is required.

## Suggested next architecture

```mermaid
flowchart LR
    CSV[CSV / JSON datasets] --> API[Flask / Node API]
    API --> UI[Web dashboard]
    API --> VALIDATE[Data validation]
    UI --> CHARTS[Charts]
    UI --> TABLES[Tables]
```

This separation would make it easier to update the dataset without editing the UI code.
