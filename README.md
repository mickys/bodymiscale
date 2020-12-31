# bodymiscale

EN :

Hello at this stage this component is to be built. The purpose of this component is to have additional information when weighing yourself with a Miscale Xiaomi connected scale. Currently the weight is sent to Hassio with an ESPHOME. The calculator is the bodmiscale.py file. The database is in the user.yaml file we find name, weight, height, age, gender and impedance (only for miscale2). The sensor information.txt file corresponds to the attributes that we want generated in the sensor. The name of the sensor should be sensor.bodymiscale.username

FR : 

Bonjour à ce stade ce compossant est à construire. Le but de ce composant est d'avoir des informations supplémentaires lorsque l'on se pese avec une balance connectée Miscale Xiaomi. Actuellement le poids est envoyé sur Hassio avec un ESPHOME. Le calculateur est le fichier bodmiscale.py. La base de données est dans le fichier user.yaml on y retrouve name, le poids, la taille, l'age, le genre et l'impedance (uniquement pour la miscale2). Le fichier sensor information.txt correspond aux attributs que l'on souhaite généré dans le sensor. Le nom du sensor devra être sensor.bodymiscale.username

The generated data is :

For miscale

- Weight
- Bmi
- Basal metabolism
- Visceral fat
- Ideal weight
- Bmi label

For miscale 2 (thanks to impedance)

- Weight
- Bmi
- Basal metabolism
- Visceral fat
- Ideal weight
- Bmi label
- Lean_body_mass
- Body fat
- Water
- Bone mass
- Muscle mass
- Protein
- Body type
- Metabolic age 
 
 ## Installation

- Vous pouvez l'installer manuellement. Copiez-collez simplement le contenu du
Dossier `bodymiscale/custom_components` dans votre` config/custom_components`
annuaire. Par exemple, vous obtiendrez le fichier `__init__.py` dans le chemin suivant:
`/config/custom_components/bodymiscale/__init__.py`.

## Configuration
clé | type | la description
:--- | :--- | :---
**plateforme (obligatoire) ** | chaîne | `bodymiscale`
**nom (obligatoire) ** | chaîne | Nom personnalisé du capteur. `bodymiscale.nom`
**weight (obligatoire) ** | sensor / sensor.weight_ | Votre sensor retournant votre poids.
**height (obligatoire) ** | nombre | Votre taille en cm. 
**born (facultatif) ** | chaîne | Votre date d'anniversaire. Année/Mois/Jour `"1990-04-10"`
**gender (facultatif) ** | chaîne | Femme(female) ou Homme(male). `"male"` 

## Example
**Configuration with default settings:**
```yaml
aurelien:
  sensors:
    weight: sensor.weight_aurelien
  height: 176
  born: "1990-04-10"
  gender: "male"
```

