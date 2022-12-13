# QuantifiedSelf - coordinated collected data
## System Requirements
### Functional Requirements
- Data
    - Store data
- Interface
    - Interfaces to add data
    - Interfaces to query data
- Types
    - Easily & rapidly introduce new recordtypes
    - New recordtypes integrate with old tools
### Non-Functional Requirements
- Hopefully, run on Thufir
## What restricts the scope of this project?
- Data follows causality
    - Each datum includes a timestamp of the last instant it could depend on
    - The only reason to modify data in place is to correct a mistake
- All entries are descriptive
    - No part of QS makes assignments or describes expectations