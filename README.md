# BASE-DE-DONNEES-COURS
Base de données d'un site de cours en ligne => Cas de Not-a-Number (NaN)

OBJET: BASE DE DONNEES COURS
GROUPE: 2
NOMBRE DE TABLE: 10


Semaine(
    *id,
    nb_semaine
)

Mois(
    *id,
    name_mois,
    #id_semaine
    #id_module
)

Modules(
    *id,
    name_module,
    status enum["gratuit", "payant"]
    #id_chapitre
    #id_recompense
)

Categories(
    *id,
    name_categorie,
    #id_module
)

users(
    *id,
    name,
    prenom_user,
    email,
    password
)

users_modules(
    #id_user,
    #id_module
)

chapitres(
    *id,
    name_chapitre
    #id_cours
)

cours(
    *id;
    name_cours
)

recompenses(
    *id,
    description_recompense
)

admins(
    *id,
    name,
    prenom,
    email,
    password
    #id_module

)

LEGENDES:
        * CLE PRIMAIRE(PK)
        # CLE ETRANGERE(FK)












OBJET: BASE DE DONNEES E-COMMERCE
GROUPE: 2
NOMBRE DE TABLE: 16



status(
    *id,
    type_statut, => /*Homme, Femme , Enfant*/
    #id_categories
)

images(
    *id,
    name_image
)

Categories(
    *id,
    name_categorie,
    #id_sous_categorie,
    #produit
)

sous-categories(
    *id,
    name_sous_categorie
)

commande(
    *id,
    #id_produit
)

produits(
    *id,
    name,
    description,
    #id_image,
    #id_marque,
    #id_taille,
    #id_avis
)

tailles(
    *id,
    tailles_produit
)

users(
    *id,
    name,
    prenom,
    email,
    password,
    #id_commande
    #id_livraison
)

users-produits(
    #id_produit,
    #id_user
)

admin(
    *id,
    name,
    prenom,
    email,
    password
    #id_produit
)

marques(
    *id,
    name_marque,
    #id_prix
)

prix(
    *id,
    somme
)

couleurs(
    *id,
    name_couleur
)

couleurs-produits(
    #id_couleur,
    #id_produit
)

avis(
    *id,
    description_avis
)

livraison(
    *id,
    #id_produit
)

LEGENDES:
        * CLE PRIMAIRE(PK)
        # CLE ETRANGERE(FK)
