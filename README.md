# acteurs-Login-github-.md

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


