# Finglow Documentation Folder Structure

```
finglow_organized/
│
├── README.md                    # Landing page for GitBook
├── SUMMARY.md                   # Table of contents for GitBook navigation
├── .gitbook.yaml               # GitBook configuration
│
├── 01-getting-started/         # Installation and basic operations
│   ├── Finglow-PDF-Manual.md
│   ├── H8200.md
│   ├── h9800.md
│   └── ... (9 files total)
│
├── 02-pd5500/                  # PD 5500 Design Code
│   ├── h0001.md               # Shells - Internal Pressure
│   ├── h0002.md               # Shells - External Pressure
│   ├── h0003.md               # Nozzles & Openings
│   └── ... (17 files total)
│
├── 03-asme-div1/              # ASME VIII Division 1
│   ├── h0101.md               # Shells - Internal Pressure
│   ├── h0102.md               # Shells - External Pressure
│   └── ... (17 files total)
│
├── 04-asme-div2/              # ASME VIII Division 2
│   ├── H0508.md               # Bolted or Welded Flat Heads
│   ├── H0514.md               # Cyclic Loading
│   └── ... (17 files total)
│
├── 05-en13445/                # EN 13445 Design Code
│   ├── H0208.md               # Bolted or Welded Flat Heads
│   ├── H0210.md               # Floating Tubesheets
│   └── ... (17 files total)
│
├── 06-materials/              # Materials and Properties
│   ├── h9980.md               # Material properties
│   ├── h9981.md
│   └── ... (3 files total)
│
├── 07-calculations/           # Calculations and Analysis
│   ├── h8900.md               # Calculation procedures
│   ├── h8901.md               # Running a calculation
│   └── ... (18 files total)
│
├── 08-components/             # Components and Elements
│   ├── h9120.md
│   ├── h9133.md
│   └── ... (18 files total)
│
├── 09-templates/              # Templates and Presets
│   ├── h9200.md
│   ├── h9201.md
│   └── ... (3 files total)
│
├── 10-reports/                # Reports and Output
│   ├── h9300.md
│   ├── h9301.md
│   └── ... (7 files total)
│
├── 11-data-input/             # Data Input and Management
│   ├── h9400.md
│   ├── h9500.md
│   └── ... (10 files total)
│
├── 12-reference/              # Reference and Definitions
│   ├── h9970.md
│   ├── h9997.md               # Units and conversions
│   ├── h9998.md
│   └── ... (21 files total)
│
├── 13-advanced/               # Advanced Features
│   └── ... (5 files total)
│
└── 99-other/                  # Other Documentation
    └── ... (7 files total)
```

## Quick Reference

| Folder | Files | Purpose |
|--------|-------|---------|
| 01-getting-started | 9 | Installation, setup, file operations |
| 02-pd5500 | 17 | PD 5500 design code calculations |
| 03-asme-div1 | 17 | ASME VIII Div.1 calculations |
| 04-asme-div2 | 17 | ASME VIII Div.2 calculations |
| 05-en13445 | 17 | EN 13445 calculations |
| 06-materials | 3 | Material properties and specs |
| 07-calculations | 18 | Calculation procedures |
| 08-components | 18 | Vessel components |
| 09-templates | 3 | Templates and presets |
| 10-reports | 7 | Report generation |
| 11-data-input | 10 | Data management |
| 12-reference | 21 | Reference material |
| 13-advanced | 5 | Advanced features |
| 99-other | 7 | Miscellaneous |
| **Total** | **169** | **All documentation** |

## Finding What You Need

**For installation help**: Look in `01-getting-started/`

**For design code calculations**: Check the appropriate code folder (`02-pd5500/`, `03-asme-div1/`, etc.)

**For material information**: See `06-materials/`

**For component details**: Browse `08-components/`

**For reference info**: Check `12-reference/`

**For how to run calculations**: See `07-calculations/`
