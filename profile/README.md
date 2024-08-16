# MAC Projects


```mermaid
graph TD
    A{<br>Local<br>MAC Database<br>Setup} <--> B[OGP Inspection GUI]
    A{<br>Local<br>MAC Database<br>Setup} <--> C[Gantry Assembly<br>LabVIEW code]
    B <--> C
    A <--> D[Wirebonding<br>and Encapsulation<br>GUI]
    D <--> E[Electrical Testing GUI]
    E <--> A
    click A href "https://github.com/murthysindhu/HGC_DB_postgres/"
    click B href "https://github.com/cmu-hgc-mac/HGC_OGP_DB"
    click D href "https://github.com/nkalliney1/wirebonder_gui"
    click E href "https://gitlab.cern.ch/acrobert/hgcal-module-testing-gui/"

```