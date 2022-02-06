# Exercice 2 (pt.2)

> la FK #num_agence, pointe vers le magasin que l'employé gère
Employe (
        *num_employe*,
        employe_nom,
        employe_prenom,
        poste,
        salaire,
        #num_agence
)

EstEmployeAu(
        *#num_employe*,
        #num_agence
)

Magasin (
        *num_agence*,
        magasin_num_telephone,
        magasin_addr_num_civique,
        magasin_addr_rue,
        magasin_addr_ville,
        magasin_addr_code_postal
)

Categorie (
        categorie
)

PrenomActeur (
        *#acteur_id*,
        *acteur_prenom*
)

> Besoin d'un acteur_id, pour que 2 acteurs puissent avoir le même nom sur
> un même film
Acteur (
        *acteur_id*,
        acteur_nom
)

PrenomRealisateur (
        *#realisateur_id*,
        *realisateur_prenom*
)

Realisateur (
        *realisateur_id*,
        *realisateur_nom*
)

Film (
        *num_catalogue*,
        titre,
        #realisateur_id,
        #categorie
)

Casette (
        *num_casette*,
        #num_catalogue,
        #num_agence,
        montant_location,
        prix_achat,
        etat
)

Membre (
        *num_membre*,
        membre_nom,
        membre_prenom,
        membre_num_telephone
        membre_addr_num_civique,
        membre_addr_rue,
        membre_addr_ville,
        membre_addr_code_postal,
        inscription_date_jour,
        inscription_date_mois,
        inscription_date_annee
)

LouePar (
        *num_location*,
        location_date_jour,
        location_date_mois,
        location_date_annee,
        restitution_date_jour,
        restitution_date_mois,
        restitution_date_annee,
        location_fin_date_jour,
        location_fin_date_mois,
        location_fin_date_annee
)