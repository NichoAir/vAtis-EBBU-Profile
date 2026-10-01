# BELUX vACC vATIS Profile

This project contains the unofficial vATIS Profile for the Belux vACC.  
To use this profile you need the [vATIS](https://vatis.app/) program.  
Once you imported the profile to vATIS, the profile are automatically updated, whenever you launch vATIS.  

## Getting Started as Controller
1. Download vATIS from https://vatis.app/  
2. Download the [Profile](https://github.com/NichoAir/vAtis-EBBU-Profile/releases). 
3. Import Profile to vATIS
4. Add your Vatsim Login Data
5. Select RWY config for the Airport at the bottom
6. Click on the Title "Airport Conditions" and select the relevant items, repeat for NOTAMs (See more information below)
7. Connect

---

You can use vATIS to simulate both voice ATIS and D-ATIS (datalink ATIS in text format) more realistically. Therefore it is important to use the correct text format to ensure that both the ATIS text looks reasonable, using plain language or common abbrevations (*contractions* in vATIS terminology), and that audio output is sensible.

<b>Always check that the ATIS output is reasonable</b>, especially when using free text in the AIRPORT CONDITIONS or NOTAMS fields. vATIS may not recognise certain abbreviations. If this is the case use plain language instead. ATIS output can be checked by selecting "Get ATIS" for the relevant ATIS in the ES controller list or by hovering above the AITS Letter in vATIS in small mode. Audio output can be checked by using the sandbox feature in vATIS or listening to the ATIS through Trackaudio.

#### LVO:

When LVO is in force it can be added to the *AIRPORT CONDITIONS* window with `LVO_INPR` by clicking on the AIRPORT CONDITIONS text above the text field, and selecting `LVO_INPR` in the list. <b>In EBBR and ELLX this is part of the NOTAMS.</b>

#### Adding free text in AIRPORT CONDITIONS and NOTAMS windows:

**AIRPORT CONDITIONS** window:
- The *AIRPORT CONDITIONS* window is used to add runway surface conditions, LVO (exception EBBR and ELLX) and in ELLX the Departure Frequency.
- The RSCD is mandatory at all belgian Airports
- The RSCD has pre-defined Items. If in doubt use wet when rain is reported and dry without rain.

**NOTAMS** window:
- NOTAMS can be selected equivalently to the AIRPORT CONDITIONS
- Some Airports have pre-defined NOTAMs or other Informations, then can be used on ATC discretion or depending on the Conditions.
- **Runway dependent NOTAMs should only be used, when the concerned runway is in use**
- NOTAMs can be added as free text to the NOTAMS window, too: 
  - e.g. `TWY A1 CLSD` or `PAPI RWY 25L U/S`

**Text formatting:**

- vATIS interprets certain phrases and abbrevations differently depending on context.
  - `B1` will be read out as "bee one" whereas `TWY B1` will be read out as "taxiway Bravo One".
  - Runway designators will only be interpreted correctly if preceded by `RWY`, i.e. write `RWY 25L` instead of just `25L`.
  - You may edit runway surface conditions manually to the real condition, if required

<b>Note:</b> Text added in the AIRPORT CONDITIONS and NOTAMS fields will remain in place for that <i>preset</i> until it is edited or deleted (including after closing and re-opening vATIS). Pre-defined airport conditions (such as LVP) will also remain in place until deselected. <b>When setting up an ATIS, make sure that no old/irrelevant ATIS text is present.</b>

## Airport specific set up and formatting:

### EBAW
- /

### EBBR 
- LVO is set through the NOTAMs window.
- In EBBR the ATIS can display the usage of ACDM through the selection of "ACDM_INUSE"
- In EBBR in 25 config with Tailwind "TAIL OPS" should be selected. In the <b>Arrival</b> ATIS you can manually add reported Tailwind at an altitude
  - e.g. `WIND at 1000ft 090/7`
- The Departure ATIS should only display relevant NOTAMs and RSCD for the Departure Runway and Taxiways and the Arrival ATIS the Arrival Runway and Taxiway RSCD and NOTAMS.
- In real life, the ATIS designator letter for DEP ATIS and ARR ATIS are usually different.

### EBCI
- You may select `CAT 2 OR 3 AVBL ONREQ` as NOTAM, this is used outside of LVO but in worsening weather

### EBLG
- In 04R config, you may select `REPORT_UNABLE_S2` as NOTAM. It will say "ADZ ON GND FREQ IF UNABLE S2" (ADVISE ON GROUND FREQUENCY IF UNABLE SIERRA 2).
- IRL the APP type is added on ATC discretion. In the config, it will give no expected Procedure or APP Type by default. You can select the ILS configs, then it will give the information, that Pilots may expect the Transitions

### EBOS
- /

### ELLX
- When Delivery is online, it should be selected as NOTAM.
- LVO is set through the NOTAMs window.
- RSCD can be left out if the weather was good for a long time.

---

#### Documentation and more information available on [the vATIS website](https://vatis.app/docs/).

