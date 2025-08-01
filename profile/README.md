# MAC Projects

This flowchart outlines the various steps of HGCal Silicon Module Assembly at a Module Assembly Center (MAC). The code associated with the various steps are linked below.

## Related projects
- [Encapsulation procedure and programs for LD Full](https://github.com/cmu-hgc-mac/encapsulation)
- [Grafana Visualization Dashboard](https://github.com/cmu-hgc-mac/grafana_hgcdb_dashboard)
- [Ambient Temperature & Humidity DB Logging](https://github.com/cmu-hgc-mac/ambient-temp-humidity)
- [Ambient Particulate Counts DB Logging](https://github.com/cmu-hgc-mac/ambient-particulate-counts)

```mermaid
graph TD
    K[CERN INT2R/CMSR DB] <--> A
    A{<br>Local<br>MAC Database<br>Setup} <--> B[OGP Inspection GUI<br>WORK IN PROGRESS]
    A{<br>Local<br>MAC Database<br>Setup} <--> C[Gantry Assembly<br>LabVIEW code]
    B <--> C
    A <--> D[Wirebonding<br>and Encapsulation<br>GUI]
    D <--> E[Electrical Testing GUI]
    E <--> A
    click A href "https://github.com/cmu-hgc-mac/HGC_DB_postgres/"
    click B href "https://github.com/cmu-hgc-mac/HGC_OGP_DB"
    click C href "https://github.com/cmu-hgc-mac/Gantry"
    click D href "https://github.com/cmu-hgc-mac/wirebonder_gui"
    click E href "https://gitlab.cern.ch/acrobert/hgcal-module-testing-gui/"

```
<!-- https://github.com/jparshook/UCSB-Gantry-master-main -->


