# icarus-mods

Collection of mods I created for the game Icarus.

## Pinkys_Speed_Bandage

**Game version : v1.2.48.110271**

Adds additional bonus statuses to the Basic Bandage, giving the player super speed.

```json
"AdditionalStats": {
    "(Value=\"BaseMovementSpeed_+%\")": 500,
    "(Value=\"BaseSprintingStaminaActionCost_+%\")": -500,
    "(Value=\"BaseChanceToResistSprain_%\")": 500,
    "(Value=\"BaseSprainModifierDuration_+%\")": -500,
    "(Value=\"BaseFallDamageResistance_%\")": 500
},
```

### Command to repack

```powershell
'"{0}\Pinkys_Speed_Bandage\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Speed_Bandage_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Speed_Bandage_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Speed_Bandage_autogen.txt"
```

## Pinkys_Fast_Extractor

**Game version : v1.2.48.110271**

Changes the Workshop Extractor speed to make it faster.

```json
"AdditionalStats": {
    "(Value=\"BaseExtractorDrillSpeed_+%\")": 9999
},
```

### Command to repack

```powershell
'"{0}\Pinkys_Fast_Extractor\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Fast_Extractor_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Fast_Extractor_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Fast_Extractor_autogen.txt"
```

## Pinkys_Dropship_Slots_30

**Game version : v1.2.48.110271**

Adds 15 more slots to the Dropship for a total of 30 slots.

```json
{
    "Name": "DropShip_Equipment",
    "InventoryID": {
        "Value": "General"
    },
    "SlotTemplate": {
        "RowName": "No_Exotics"
    },
    "StartingSlots": 30
},
{
    "Name": "Space_Player_Loadout",
    "InventoryID": {
        "Value": "Loadout"
    },
    "StartingSlots": 30
},
```

### Command to repack

```powershell
'"{0}\Pinkys_Dropship_Slots_30\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Dropship_Slots_30_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Dropship_Slots_30_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Dropship_Slots_30_autogen.txt"
```

## Pinkys_Healing_Bandage

**Game version : v1.2.48.110271**

Adds a healing effect to the bandages.

```json
"Stats": {
    "(Value=\"BaseHealthRecovery_+\")": 120
},
```

### Command to repack

```powershell
'"{0}\Pinkys_Healing_Bandage\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Healing_Bandage_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Healing_Bandage_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Healing_Bandage_autogen.txt"
```

## Pinkys_Fast_Furnace

**Game version : v1.2.48.110271**

Makes all furnaces 75% faster.

```json
"AdditionalStats": {
    "(Value=\"BaseEnergyTransmutationResourceCost_+%\")": -25,
    "(Value=\"BaseSmeltingSpeed_+%\")": 50
},
```

## Pinkys_Fast_Composter

**Game version : v1.2.48.110271**

Makes all composters 75% faster.

```json
"RequiredMillijoules": 625,
```

### Command to repack

```powershell
'"{0}\Pinkys_Fast_Composter\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Fast_Composter_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Fast_Composter_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Fast_Composter_autogen.txt"
```

## Pinkys_Durable_Workshop_Items

**Game version : v1.2.48.110271**

Makes all workshop items more durable.

```json
"Name": "Meta_Item_Shengong",
"Max_Durability": 50000 -> 60000,
...
"Name": "Meta_Item_Inaris",
"Max_Durability": 60000 -> 200000,
...
"Name": "Meta_Item_Larkwell",
"Max_Durability": 40000 -> 150000,
...
"Name": "Meta_Item_Printed",
"Max_Durability": 30000 -> 40000,
```

### Command to repack

```powershell
'"{0}\Pinkys_Durable_Workshop_Items\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Durable_Workshop_Items_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Durable_Workshop_Items_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Durable_Workshop_Items_autogen.txt"
```

## Command to repack all mods

```powershell
'"{0}\Pinkys_Speed_Bandage\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Speed_Bandage_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Speed_Bandage_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Speed_Bandage_autogen.txt"; '"{0}\Pinkys_Fast_Extractor\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Fast_Extractor_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Fast_Extractor_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Fast_Extractor_autogen.txt"; '"{0}\Pinkys_Dropship_Slots_30\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Dropship_Slots_30_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Dropship_Slots_30_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Dropship_Slots_30_autogen.txt"; '"{0}\Pinkys_Healing_Bandage\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Healing_Bandage_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Healing_Bandage_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Healing_Bandage_autogen.txt"; '"{0}\Pinkys_Fast_Furnace\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Fast_Furnace_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Fast_Furnace_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Fast_Furnace_autogen.txt"; '"{0}\Pinkys_Fast_Composter\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Fast_Composter_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Fast_Composter_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Fast_Composter_autogen.txt"; '"{0}\Pinkys_Durable_Workshop_Items\*.*" "..\..\..\Icarus\Content\*.*"' -f $pwd | Out-File release\Pinkys_Durable_Workshop_Items_autogen.txt; .\UnrealPak\Engine\Binaries\Win64\UnrealPak.exe "$pwd\release\Pinkys_Durable_Workshop_Items_P.pak" -platform="Windows" -create="$pwd\release\Pinkys_Durable_Workshop_Items_autogen.txt"
```
