=====================
2. Demand projections
=====================

In the Ukraine WESM, demand curves are calculated exogenously and then provided to OSeMOSYS as inputs. A dedicated demand workbook has been developed to estimate energy service demand values across all sectors. This section outlines the underlying data sources, assumptions, and methodology behind the demand projections. Section 2.1 presents the method used to derive the initial baseline values for 2020, based on the official 2020 Ukrainian energy balance. Section 2.2 describes the main demand drivers used to develop projections, while Section 2.3 explains in greater detail how sectoral demands were defined and translated into projection pathways.

2.1 Current energy balance
==========================
An energy balance provides a comprehensive overview of energy flows within a country over a given year. It breaks down primary supply—defined as Total Energy Supply (TES)—and final consumption—defined as Total Final Consumption (TFC).

A particular focus is placed on transformation processes in line with the Ukrainian 2020 energy balance. These cover the conversion of primary energy into secondary carriers in:
* Electricity plants (large producers generating electricity for the grid),
* Combined Heat and Power (CHP) plants, where both electricity and heat are supplied, and
* Dedicated heat plants, providing thermal energy for district heating systems.

The 2020 Ukrainian national energy balance (originally in kilotonnes of oil equivalent, ktoe, converted into petajoules, PJ) served as the benchmark dataset [#f1]_ . The consumption of each fuel was then disaggregated into the main demand sectors: Residential, Industry, Commerce & Services, Agriculture, Transport, Non-Energy Use, and Other.

2.2 Demand projections
======================

The energy service demand projections were derived from the sectoral consumption values reported in the 2020 Ukrainian energy balance. Projections were built using a set of socio‑economic and technical drivers that reflect different development pathways. These included population, in millions of people, Gross Domestic Product (GDP), as well as the share of GDP per sector of the Economy. These drivers could aid in deriving demands under High, Central, and Low scenarios, and are currently under the Central/Mid scenario. Together, these drivers were linked to the sectoral demand categories to generate projections of useful energy demand. The accompanying table details how each projection driver was applied to individual service demands.

.. csv-table:: 
   :file: ./data/projections.csv
   :widths: 30, 30, 30, 70
   :header-rows: 1


2.3 Sectors
===========

Agriculture
-----------
In the agricultural sector, fuel consumption from the 2020 Ukrainian energy balance was aggregated across subsectors and then distributed into percentage shares according to the relevant energy service demands by fuel type, including electricity, biomass, and heat, among others. These allocations were expressed directly as final energy demand values (in petajoules, PJ), without conversion to useful energy.

Commercial sector
-----------------

In the commercial and public services sector, fuel consumption from the 2020 Ukrainian energy balance was taken as the baseline and disaggregated into final energy demand categories. The sector covers a wide range of energy uses in offices, retail, public administration, education, health facilities, and other service buildings. Each type of demand is represented directly in the model as final energy demand, expressed in petajoules (PJ).

Industry
--------

In the industrial sector, fuel consumption from the 2020 Ukrainian energy balance was disaggregated across three subsectors: non-metallic minerals (cement), food and drink, and Other industries. For each subsector, the share of consumption by fuel category was calculated as a percentage of the total allocation. The representation of industrial demand in the model is done directly at the final energy demand level, expressed in petajoules (PJ), without further conversion into useful energy.

Residential sector
------------------

In the residential sector, fuel consumption from the 2020 Ukrainian energy balance is divided between urban and rural households. For each fuel, a percentage split between urban and rural demand was calculated, summing to 100%. On this basis, residential final energy demand (PJ) was computed separately for urban and rural areas.

Within each area, fuel consumption is further mapped to specific technologies under distinct energy service demands: cooling, cooking, heating & hot water, lighting, and other electrical uses. Each demand is therefore represented both by its fuel category and by the relevant technology, which defines the base efficiency of conversion.

The key demand–technology mappings are:

* Cooling

* Urban: Electricity – Base efficiency
* Rural: Electricity – Base efficiency

* Cooking

* Urban:

* Coal – Base efficiency
* Electricity (induction) – Base efficiency
* Natural gas – Base efficiency
* LPG – Base efficiency
* Biomass (wood, charcoal) – Improved efficiency (e.g. improved stoves)

* Rural:

* Coal – Base efficiency
* Electricity (induction) – Base efficiency
* Natural gas – Base efficiency
* LPG – Base efficiency
* Biomass – Improved efficiency (improved traditional stoves)

* Lighting

Urban: Electricity – Base efficiency
Rural: Electricity – Base efficiency

* Heating & Hot Water
* Urban:
* Coal – Base efficiency
* Oil products – Base efficiency
* Natural gas – Base efficiency
* Biomass – Base efficiency
* Electricity – Base efficiency
* District heating – Base efficiency
* Rural:
* Coal – Base efficiency
* Oil products – Base efficiency
* Natural gas – Base efficiency
* Biomass – Base efficiency
* Electricity – Base efficiency
* District heating – Base efficiency
This detailed representation enables the model to capture both fuel use and technology choices within households, allowing for the analysis of fuel switching, electrification, efficiency improvements (e.g., modern biomass cookstoves, induction cooking), and the role of district heating in urban areas. It also accounts for the urban–rural divide in Ukraine's residential energy system, where reliance on solid fuels remains higher in rural areas. In contrast, urban households are more integrated into the electricity and district heating networks.

Transports
----------

In the transport sector, demand is represented in terms of transport services rather than direct fuel consumption. Drawing on the 2020 Ukrainian energy balance, passenger and freight activity levels were established and expressed in billion passenger-kilometres (BPKM) for passenger travel and billion tonne-kilometres (BTKM) for freight movement. These service demands are then met by specific transport technologies linked to different fuels.

* Passenger transport (BPKM):
* Buses (road transport): petroleum products, natural gas (CNG/LNG), biodiesel
* Rail transport: coal, diesel, electricity (reflecting both the diesel and electrified portions of Ukraine's rail system)
* Navigation: petroleum products (mainly diesel and heavy fuel oil used in inland/coastal shipping)
* Freight transport (BTKM):
* Road freight: petroleum products, natural gas, biodiesel
* Rail freight: coal, diesel, electricity
* Navigation (shipping): petroleum products
In the model, the final demands are expressed explicitly as BPKM for passenger transport and BTKM for freight transport, rather than in energy terms. The corresponding fuel use (in PJ) is then calculated based on the efficiency of the associated technologies. This design reflects the actual transport service demand in Ukraine's economy, capturing the high share of rail in freight movement, the dominant role of petroleum products in road modes, and the potential for fuel switching and electrification in long-term transition pathways.

.. rubric:: Footnotes

.. [#f1] United Nations Statistics Division. (2025). UN Energy Statistics Data Portal. United Nations. https://unstats.un.org/unsd/energystats/dataPortal/