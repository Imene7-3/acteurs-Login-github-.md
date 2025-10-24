# acteurs-Login-github-.md
https://mermaid.live/edit#pako:eNp1VF2L2zAQ_CtGTy1NQr58MaYU0msfWnLl4B4OSl5ke-0I7JW7ksJd0_z3yo7tSHeOIRBrdmdnd0c-sVRmwGK2x7TkSn0TvCBe7TGwzyOQkogQfP43nQbftckERz2G_QSDsE21yC_oThZQAeoLuq1rTro9GIPvD7xKCC7QE9BRpB3tY8k15JIq6DNGgrYig1-mAhJ_jCW5RLTNXEWeLqfN8-lJk8AiQFk5h8KK4QU4J-kBqPn1lT98dMBaKm1KIO8wMVkB-oG_7OQrkAOgOAI3O46F6SqcfZ39aMd0miablNCuuAQQcpEKoKb7XsUb1utSxnhtSwQ1CeXyEhwBzQOgMlCOkg6rG6HkGYHy-Jqxlm-m0ZwpQzlP3chMqFqiSERpO_XGytMU1LDgG706FvOUNcUw6RymHODA1VdephJvEHYpHlkiZRlUYJLSVa5MDdQuY5So9-q4BTvUwXJpCAX9wMb3XIurwmEatQa655iJjGtDt0by_vKMaWiM9QyJA1SgrTO2iBJTfxM242JiX5F7_26tx43xZNgZ2N2VIm1b9YpJc7xx_ezIa0naFzOUHG79dPrl6tc46C6t_wlpYoaEOGiaeR_gkBDkQID9yrxaIxOPA2sxZUo9Fu9PJQ6Mtu5XwCasIJGxWJOBCbN4xZtX1s5tz_TBcu9ZbP9mkHNLvref77NNqzn-lrLqM-0EiwOLc14q-2ZqaxfoPvBDCGBmzSQNahaHLQOLT-yFxatlNAujxWZ5N9-sl4toY9FXFk-ju9lytZqvN-soXIWL8O48YX_boovZOpwv19FqHkZhZBPD838VZfms

classDiagram
    Personne <|-- Etudiant
    Personne <|-- JeuneActif
    Logement <|-- Appartement
    Logement <|-- Chambre
    Service <|-- PlateformeLogement
    Service <|-- AideNumerique

    class Personne {
        +String nom
        +int age
        +chercherLogement()
        +postuler()
        +budgetMaxLoyer
        +niveauLangue
    }

    class Etudiant {
        +String universite
        +beneficierAide()
    }

    class JeuneActif {
        +String entreprise
        +revenuMensuel
    }

    class Logement {
        +String adresse
        +int loyer
        +int surface
        +disponibilite()
        +accesNumerique()
    }

    class Appartement {
        +int nbChambres
        +hasBalcon()
    }

    class Chambre {
        +bool meuble
        +superficie
    }

    class Service {
        +String nomService
        +fournirInformation()
        +accepterCandidature()
    }

    class PlateformeLogement {
        +String siteWeb
        +mettreAnnonce()
        +triLangue()
        +aideNumerique()
    }

    class AideNumerique {
        +nomApplication
        +trouverLogement()
        +supportLangue()
    }

    Personne --> Logement : postule
    Service --> Personne : aide
    Service --> Logement : reference
    Personne --> PlateformeLogement : consulte
    Personne --> AideNumerique : utilise
