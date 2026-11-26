## 🔗 Link Prototip Interactiv (Figma)
* **[Accesează prototipul interactiv în Figma](https://www.figma.com/design/7zZWDF6OqKrezDOUc4EmF0/Librarius-%E2%80%93-Gestionarea-unei-biblioteci?node-id=0-1&t=IJFT3B23nv9wzENr-1)**

---

## 📁 Structura Repository-ului
* `prototype/` — Exportul ecranelor principale ale interfeței grafice (PDF/PNG).
* `diagrams/` — Diagrama UML a cazurilor de utilizare (Use Case).
* `docs/` — Documentația arhitecturii modulare a aplicației.

---

## 🏗️ Schema Arhitecturii Modulare

Aplicația este structurată pe 3 niveluri (arhitectură stratificată), separând interfața grafică de regulile de business și de stocarea datelor:
```text
+---------------------------------------------------------------+
|                1. NIVELUL DE PREZENTARE (UI)                  |
|  - Prezentare generală (Dashboard & statistici colecție)      |
|  - Catalog cărți (Căutare, filtrare după categorie, status)   |
|  - Ferestre modale (Adăugare carte nouă, Împrumut / Retur)    |
+---------------------------------------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|              2. NIVELUL LOGICII APLICAȚIEI (BLL)              |
|  - Validare date carte și disponibilitate exemplar            |
|  - Gestionare reguli de împrumut, termene limită și retururi  |
|  - Calcul statistici și distribuție pe categorii              |
+---------------------------------------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|                 3. STRATUL DE DATE (DAL / DB)                 |
|  - Persistență entități: Cărți, Cititori, Împrumuturi         |
|  - Operații CRUD și interogări de filtrare                    |
+---------------------------------------------------------------+
