```mermaid
graph TD
    %% ==========================================
    %% ESTRUCTURA GENERAL DE LA UDG
    %% ==========================================
    subgraph Red_Universitaria ["Estructura General UDG"]
        CGU["Consejo General Universitario<br/><i>(Conformado por: Administrativos, Académicos, Alumnos y Directivos)</i>"]
        RG["Rectoría General"]
        SG["Secretaría General"]

        CGU --> RG
        CGU --> SG

        VGAI["VGAI<br/>(Vicerrectoría Executiva / Académica)"]
        ADMIN_GEN["Administrativa"]

        RG --> VGAI
        RG --> ADMIN_GEN

        %% Ramas de VGAI
        ACAD["Académicos"]
        INV_POS["Investigación de Posgrado"]
        VINC["Vinculación"]

        VGAI --> ACAD
        VGAI --> INV_POS
        VGAI --> VINC

        CEMS["CEMS"]
        LIC["Licenciaturas"]
        PROF["Profesores"]

        ACAD --> CEMS
        ACAD --> LIC
        ACAD --> PROF

        BECAS_G["Becas"]
        INTER["Intercambios"]
        LENG["Lenguas"]

        VINC --> BECAS_G
        VINC --> INTER
        VINC --> LENG

        %% Ramas de Administrativa
        CE_G["Control Escolar"]
        SG_G["Servicios Generales"]
        FIN_G["Finanzas"]

        ADMIN_GEN --> CE_G
        ADMIN_GEN --> SG_G
        ADMIN_GEN --> FIN_G
    end

    %% ==========================================
    %% ESTRUCTURA DEL CONSEJO DE CENTRO
    %% ==========================================
    subgraph Centro_Universitario ["Estructura de Centro Universitario"]
        CC["Consejo de Centro<br/><i>(Conformado por: Estudiantes, Profesores, Directivos, Administración y Sociedad)</i>"]
        RC["Rectoría del Centro"]

        CC --> RC

        SA["Secretaría Académica"]
        SADM["Secretaría Administrativa"]
        DIR["Direcciones"]

        RC --> SA
        RC --> SADM
        RC --> DIR

        %% Ramas de Secretaría Académica
        CC_ARR["Coordinación de Carrera"]
        POS["Posgrado"]
        INV["Investigación"]
        SA_SERV["Servicios Académicos"]

        SA --> CC_ARR
        SA --> POS
        SA --> INV
        SA --> SA_SERV

        BECAS_C["Becas"]
        SALUD["Salud Integral"]
        BIB["Biblioteca"]
        TFF["TFF"]
        DDU["DDU"]
        TEC["Tecnologías"]

        SA_SERV --> BECAS_C
        SA_SERV --> SALUD
        SA_SERV --> BIB
        SA_SERV --> TFF
        SA_SERV --> DDU
        SA_SERV --> TEC

        %% Ramas de Secretaría Administrativa
        FIN_C["Finanzas"]
        CE_C["Control Escolar"]
        SG_C["Servicios Generales"]
        CP["Coordinación de Personal"]

        SADM --> FIN_C
        SADM --> CE_C
        SADM --> SG_C
        SADM --> CP

        %% Ramas de Direcciones
        DEES["DEES"]
        DEST["DEST"]
        DES["DES"]

        DIR --> DEES
        DIR --> DEST
        DIR --> DES
    end
