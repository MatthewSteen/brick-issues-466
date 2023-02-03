# Equipment

## Air_Handler_(Unit) vs. Air_Handling_Unit

Consensus seems to be `Air_Handling_Unit` based on below.

### Air_Handler_(Unit)
- ASHRAE Handbook indices have an entry for `Air handlers`. 
- IFC 7.5.2.31 IfcUnitaryEquipmentTypeEnum has an enumeration for `AirHandler`.

**IFC 7.5.2.31 IfcUnitaryEquipmentTypeEnum**
Constant | Description
:- | :-
AIRHANDLER | A unitary air handling unit typically containing a fan, economizer, and coils.
AIRCONDITIONINGUNIT | A unitary packaged air-conditioning unit typically used in residential or light commercial applications.
DEHUMIDIFIER | A unitary packaged dehumidification unit. Note: units supporting multiple modes (dehumidification, cooling, and/or heating) should use AIRCONDITIONINGUNIT.
SPLITSYSTEM | A system which separates the compressor from the evaporator, but acts as a unitary component typically within residential or light commercial applications.
ROOFTOPUNIT | A packaged assembly that is either field-erected or manufactured atop the roof of a large residential or commercial building and acts as a unitary component.
USERDEFINED | User-defined unitary equipment type.
NOTDEFINED | Undefined unitary equipment type.

### Air_Handling_Unit (AHU)
- See [AHRI Standard 430/1](https://www.ahrinet.org/sites/default/files/2022-06/AHRI_Standard_430_I-P_2020.pdf).
- ASHRAE Terminology = https://terminology.ashrae.org/?entry=air-handling%20unit%20(AHU)
- ASHRAE Handbook of HVAC Systems and Equipment uses `Air-Handling`.

## Box vs. Terminal
TODO

## Computer_Room_Air_Conditioning and Computer_Room_Air_Handler
- These definitions need clarification. ASHRAE and AHRI distinguish between CRACs and CRAHs by cooling type. See [AHRI Standard 1360/1](https://www.ahrinet.org/sites/default/files/2022-12/AHRI%20Standard%201361-2022%20%28SI%29.pdf).
  - Computuer_Room_Air_Conditioner (CRAC) = DX cooling
  - Computuer_Room_Air_Handler (CRAH) = hydronic cooling
- General term for both is apparently [computer and data processing room (CDPR) unitary air conditioner](https://terminology.ashrae.org/?entry=computer%20and%20data%20processing%20room%20(CDPR)%20unitary%20air%20conditioner).

## Discharge_Fan vs. Supply_Fan
- `Supply_Fan` per AHRI Standard 920/1 above.

## Discharge_Air_Plenum vs. Supply_Air_Plenum
- `Supply_Plenum` to follow Supply_Fan.
- Suggest removing `_Air` from class name because plenums are by definition for air systems like fans. See https://terminology.ashrae.org/?entry=plenum.
  - Same for `Return_Air_Plenum`.

## Dual_Duct_Air_Handling_Unit
- Consider removing. Canonical sources refer to dual duct *terminals* not AHUs. 

## Embedded_Surface_System_Panel
- Consider renaming `Embedded_Surface_[Heating_And_Cooling]_System` per [ISO 11855](https://www.iso.org/obp/ui#iso:std:iso:11855:-1:ed-2:v1:en:term:3.28).
- Consider updating defintion per above link.

## Fan_Coil_Unit
- See [AHRI Standard 440/1](https://www.ahrinet.org/sites/default/files/2022-06/AHRI_Standard_440_I-P_2019.pdf).
  - Does not apply to DX cooling.
  - Does not apply to steam heating.
- ASHRAE Terminology = https://terminology.ashrae.org/?entry=fan+coil+unit

## Heat_Exchanger vs. Coil
TODO

## Heating_Ventilation_Air_Conditioning_System
- Rename `Heating_Ventilating_Air_Conditioning_System` per ASHRAE.
  - https://github.com/BrickSchema/Brick/issues/464.

## Network_Video_Recorder
I don't have expertise in this field.

## Radiant_Ceiling_Panel
TODO

## Rooftop_Unit (RTU)
- Consider removing because an RTU is just an AHU with a location, i.e. `brick:hasLocation bldg:roof`. 
- IFC 7.5.2.31 IfcUnitaryEquipmentTypeEnum has an enumeration for `RooftopUnit` (see table above), which seems incomplete.
- ASHRAE Terminology = https://terminology.ashrae.org/?entry=rooftop%20air%20conditioner

## Thermally_Activated_Building_System_Panel
- Consider renaming `Thermally_Active_Building_System` (TABS) per [ISO 11855](https://www.iso.org/obp/ui#iso:std:iso:11855:-1:ed-2:v1:en:term:3.81).
- Consider updating definition per above link.

## Variable Frequency Drive
- ASHRAE Terminology = https://terminology.ashrae.org/?entry=variable-frequency drive (VFD)
