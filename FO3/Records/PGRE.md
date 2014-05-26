PGRE
====

Placed Grenade

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
+ | NAME | Base | formid | FormID of a [PROJ](PROJ.md) record.
 | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.md) record.
 | XRGD | Ragdoll Data | uint8[] | 
 | XRGB | Ragdoll Biped Data | uint8[] |
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.md) record, or null.
+ | | [Embedded Script](Fields/Script.md) | | Patrol data. A field collection.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.md) record, or null.
 | XOWN | Owner | formid | Ownership data. FormID of a [FACT](FACT.md), [ACHR](ACHR.md) or [NPC_](NPC_.md) record.
 | XRNK | Faction rank | int32 | Ownership data 
 | XCNT | Count | int32 |
 | XRDS | Radius | float32 |
 | XHLP | Health | float32 |
-* | XPWR | Water Reflection / Refraction | struct |
-* | [XDCR](Fields/XDCR.md) | Decal | struct | Linked decals
 | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.md), [ACRE](ACRE.md), [ACHR](ACHR.md), [PGRE](PGRE.md) or [PMIS](PMIS.md) record.
 | [XCLP](Fields/XCLP.md) | Linked Reference Color | struct |
 | [XAPD](Fields/XAPD.md) | Flags | uint8 | Activate parents.
-*| [XAPR](Fields/XAPR.md) | Activate Parent Ref | struct | Activate parents
 | [XESP](Fields/XESP.md) | Enable Parent | struct |
 | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.md) or [REGN](REGN.md) record.
 | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.md) record.
 | XIBS | Ignored By Sandbox | null | Flag
 | XSCL | Scale | float32 |
+ | [DATA](Fields/DATA (ACHR, ACRE).md) | Position / Rotation | struct |
 
### XPWR

Count | Name | Type | Info
------|------|------|-----
 | Reference | formid | FormID of a [REFR](REFR.md) record.
 | Type | uint32 | Flags - see below for values.
 
#### Type Flag Values

Value | Meaning
------|--------
0x00000001 | Reflection
0x00000002 | Refraction

