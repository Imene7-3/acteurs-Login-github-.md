classDiagram
    Personne <|-- Etudiant
    Personne <|-- JeuneActif
    Logement <|-- ResidenceEtudiante
    Logement <|-- Appartement
    Service <|-- PlateformeNumerique
    Service <|-- GroupeEntraide
    Service <|-- OrganismePublic

    class Personne {
        +nom
        +age
        +trouverLogement()  // contrainte principale
    }

    class Etudiant {
        +nationalite
        +maitriseLangue
    }

    class JeuneActif {
        +salaire
        +mobilite
    }

    class Logement {
        +localisation
        +type
        +loyer
    }

    class ResidenceEtudiante {
        +crousSubvention
    }

    class Appartement {
        +proprietaire
    }

    class Service {
        +nom
    }

    class PlateformeNumerique {
        +trouverLogement()
        +rechercheRapide()
        +soutienLangue()  // pour étudiants internationaux
    }

    class GroupeEntraide {
        +partageConseils()
        +recommandations()
    }

    class OrganismePublic {
        +dispositifsAide()
        +informationAdministrative()
    }

    %% Relations
    Personne --> Logement : postule
    Personne --> PlateformeNumerique : consulte
    Personne --> GroupeEntraide : contacte
    Personne --> OrganismePublic : consulte
    PlateformeNumerique --> Logement : référence
    GroupeEntraide --> Logement : accompagne
    OrganismePublic --> Logement : référence


