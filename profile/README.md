# MAC Projects

This flowchart outlines the vaious steps of HGCal Silicon Module Assembly at a Module Assembly Center (MAC). The code associated with the various steps are linked below.

```mermaid
graph TD
    K[CERN INT2R DB] <--> A
    A{<br>Local<br>MAC Database<br>Setup} <--> B[OGP Inspection GUI - Under Development]
    A{<br>Local<br>MAC Database<br>Setup} <--> C[Gantry Assembly<br>LabVIEW code]
    B <--> C
    A <--> D[Wirebonding<br>and Encapsulation<br>GUI]
    D <--> E[Electrical Testing GUI]
    E <--> A
    click A href "https://github.com/cmu-hgc-mac/HGC_DB_postgres/"
    click B href "https://github.com/cmu-hgc-mac/HGC_OGP_DB"
    click C href "https://github.com/kai-ucsb/Gantry"
    click D href "https://github.com/nkalliney1/wirebonder_gui"
    click E href "https://gitlab.cern.ch/acrobert/hgcal-module-testing-gui/"

```
<!-- https://github.com/jparshook/UCSB-Gantry-master-main -->
