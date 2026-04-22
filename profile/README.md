# MAC Projects

This flowchart outlines the various steps of HGCal Silicon Module Assembly at a Module Assembly Center (MAC). The [repositories](https://github.com/orgs/cmu-hgc-mac/repositories) associated with the various steps are linked below.

```mermaid
graph TD
    
    subgraph AI [Assembly & Inspection]
        direction TB
        L[Gantry Assembly<br>LabVIEW code] <--> I[OGP-DB Python Helper<br>WORK IN PROGRESS]
        IS@{ shape: docs, label: "OGP Inspection Surveys" }
        I --- IS

    end

    subgraph WEN [Wirebonding and Encapsulation]
        direction TB
        W[Wirebonding and<br> Encapsulation GUI]
        EP@{ shape: docs, label: "Encapsulation procedure and programs for LD Full" }
        W --- EP
    end

    subgraph ET [Electrical Testing]
        direction TB
        SMT[Single Module<br> Testing GUI]
        MMT[MultiModule<br> Testing GUI]
        PLC[PLC Toolkit]
    end

    subgraph EM [Environment monitoring]
        direction LR
        H(Ambient Temperature & Humidity DB Logging) 
        P(Ambient Particulate Counts DB Logging) 
    end

    K[(CERN INT2R/CMSR DB)] <==> A[(MAC<br>Postgres Database<br>Setup)]
    G>Grafana-Postgres Visualization Dashboard] e1@ === A
    A e2@--- EM
    A <--> AI
    A <--> WEN
    A <--> ET
    
    click A href "https://github.com/cmu-hgc-mac/HGC_DB_postgres/"
    click I href "https://github.com/cmu-hgc-mac/HGC_OGP_DB"
    click L href "https://github.com/cmu-hgc-mac/Gantry"
    click W href "https://github.com/cmu-hgc-mac/wirebonder_gui"
    click SMT href "https://gitlab.cern.ch/acrobert/hgcal-module-testing-gui/"
    click MMT href "https://github.com/ltsai323/MultiModuleTeststandUI/tree/main"
    click PLC href "https://github.com/Xingfu23/PLC_toolkits_mqtt_NTU/tree/master"
    click K href "https://gitlab.cern.ch/groups/hgcal-database/-/issues"
    click G href "https://github.com/cmu-hgc-mac/grafana_hgcdb_dashboard"
    click P href "https://github.com/cmu-hgc-mac/ambient-particulate-counts"
    click H href "https://github.com/cmu-hgc-mac/ambient-temp-humidity"
    click EP href "https://github.com/cmu-hgc-mac/encapsulation"
    click IS href "https://github.com/cmu-hgc-mac/OGP-inspection-surveys"
    e1@{ animate: true }
    e2@{ animate: true }
    

```
<!-- https://github.com/jparshook/UCSB-Gantry-master-main -->


