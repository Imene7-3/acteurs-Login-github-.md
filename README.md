# acteurs-Login-github-.md


```mermaid
classDiagram
    Personne <|-- Etudiant
    Personne <|-- JeuneActif
    Logement <|-- ResidenceEtudiante
    Logement <|-- Appartement
    Service <|-- PlateformeNumerique
    Service <|-- Association
    Service <|-- OrganismeLocal

    class Personne {
        +nom
        +age
        +trouverLogement()  // contrainte principale
    }

    class Etudiant {
    }

    class JeuneActif {
    }

    class Logement {
        +localisation: "Seine-Saint-Denis"
    }

    class ResidenceEtudiante {
    }

    class Appartement {
    }

    class Service {
    }

    class PlateformeNumerique {
        +trouverLogement()
        +soutienLangue()  // pour nouveaux arrivants ou difficultés linguistiques
    }

    class Association {
        +accompagnement()
        +soutienLangue()
    }

    class OrganismeLocal {
        +dispositifsAide()
    }

    Personne --> Logement : postule
    Personne --> PlateformeNumerique : consulte
    Personne --> Association : contacte
    Personne --> OrganismeLocal : consulte
    PlateformeNumerique --> Logement : référence
    Association --> Logement : accompagne
    OrganismeLocal --> Logement : référence

