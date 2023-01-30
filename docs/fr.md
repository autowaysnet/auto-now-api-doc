
# AUTO-NOW  FR
## Endpoint :

> `https://app.auto-ways.net/api/v1/fr`
>

## Method :

> `GET`
>

## Headers :

> `None`
>

## Parameters :

| Parameter  | Example | required |
| --- | --- | --- |
| plaque | "AB123CD" or “AA-123-BC” | true |
| token | YOUR_TOKEN_WILL_BE_HERE | true |

## cURL request :

```c
curl -L -X GET 'https://app.auto-ways.net/api/v1/fr?plaque=AA123BC&token=YOUR_TOKEN_WILL_BE_HERE'
```

## Success Response :

> Status Code: 200 OK
>
- Content-Type: application/json
- Body:

    ```json
    {
        "error": false,
        "data": {
            "AWN_k_type": 31164,
            "AWN_VIN": "VF1DZ0N0641118804",
            "AWN_marque": "RENAULT",
            "AWN_modele": "MEGANE",
            "AWN_version": "III DCI",
            "AWN_immat": "aa123bc",
            "AWN_marque_id": "44",
            "AWN_modele_id": "625",
            "AWN_modele_etude": "MEGANE",
            "AWN_type_mine": "MRE5531A0421",
            "AWN_couleur": "NOIR",
            "AWN_Hauteur": "142",
            "AWN_largeur": "180",
            "AWN_longueur": "430",
            "AWN_poids_vide": "1807",
            "AWN_poids_total_roulant": "1310",
            "AWN_puissance_chevaux": "131",
            "AWN_puissance_fiscale": "7",
            "AWN_carrosserie": "COUPE",
            "AWN_marque_carrosserie": "RENAULT",
            "AWN_carrosserie_carte_grise": "CI",
            "AWN_genre": "COUPE",
            "AWN_genre_carte_grise": "VP",
            "AWN_energie": "Gazole",
            "AWN_emission_co_2": "134",
            "AWN_date_mise_en_circulation": "2009-04-18",
            "AWN_date_30": "2009-04-18",
            "AWN_numero_de_serie": "641118804",
            "AWN_nbr_cylindres": "4",
            "AWN_nbr_cylindre_energie": "1870",
            "AWN_collection": "NON",
            "AWN_puissance_KW": "96",
            "AWN_code_moteur": "C010377",
            "AWN_nbr_volume": "2",
            "AWN_nbr_vitesses": "6",
            "AWN_nbr_portes": "3",
            "AWN_nbr_de_places": "5",
            "AWN_nbr_soupapes": "2",
            "AWN_type_boite_vites": "Mecanique",
            "AWN_turbo_Comprressor": "TURBO",
            "AWN_depollution": "NON",
            "AWN_empattement": "264",
            "AWN_consommation_urbaine": "0.0",
            "AWN_consommation_ex_urbaine": "0.0",
            "AWN_consommation_mixte": "0.0",
            "AWN_mode_injection": "COMMON RAIL",
            "AWN_prix": "0.00",
            "AWN_propulsion": "Avant",
            "AWN_libelle": "III DCI",
            "AWN_TID": "57428",
            "AWN_country": "fr",
            "AWN_brand_img_path": "/brands/renault.png",
            "AWN_brand_img_full_path": "https://app.auto-ways.net/autoways/public/storage/brands/renault.png",
            "AWN_output_lang": "fr"
        }
    }
    ```


## Error Responses:

> Status Code: 401 Unauthorized
>
- Content-Type: application/json
- Body:

    ```json
    {"error": true,"message": "Invalid token"}
    ```


> Status Code : 400 Bad Request
>
- Content-Type: application/json
- Body:

```json
{"error": true,"message": "Invalid plaque "}
```

## API References :

The request was successful. The response body contains the following properties:

- **`error`** (Boolean): Specifies whether the request resulted in an error. If false, the request was successful and the data property contains the relevant data. If true, the error property contains a description of the error.
- **`data`** (Object): An object containing the following properties:
    - **`AWN_k_type`** (Integer): The type of the vehicle.
    - **`AWN_VIN`** (String): The Vehicle Identification Number (VIN) of the vehicle.
    - **`AWN_marque`** (String): The brand name of the vehicle.
    - **`AWN_modele`** (String): The model name of the vehicle.
    - **`AWN_version`** (String): The version of the model.
    - **`AWN_immat`** (String): The license plate number of the vehicle.
    - **`AWN_marque_id`** (String): The ID of the brand.
    - **`AWN_modele_id`** (String): The ID of the model.
    - **`AWN_modele_etude`** (String): The study model of the vehicle.
    - **`AWN_type_mine`** (String): The mine type of the vehicle.
    - **`AWN_couleur`** (String): The color of the vehicle.
    - **`AWN_Hauteur`** (String): The height of the vehicle.
    - **`AWN_largeur`** (String): The width of the vehicle.
    - **`AWN_longueur`** (String): The length of the vehicle.
    - **`AWN_poids_vide`** (String): The weight of the vehicle when empty.
    - **`AWN_poids_total_roulant`** (String): The total weight of the vehicle when in motion.
    - **`AWN_puissance_chevaux`** (String): The horsepower of the vehicle.
    - **`AWN_puissance_fiscale`** (String): The fiscal horsepower of the vehicle.
    - **`AWN_carrosserie`** (String): The body style of the vehicle.
    - **`AWN_marque_carrosserie`** (String): The brand of the body of the vehicle.
    - **`AWN_carrosserie_carte_grise`** (String): The body style on the vehicle registration card.
    - **`AWN_genre`** (String): The genre of the vehicle.
    - **`AWN_genre_carte_grise`** (String): The genre on the vehicle registration card.
    - **`AWN_energie`** (String): The energy source of the vehicle.
    - **`AWN_emission_co_2`** (String): The CO2 emissions of the vehicle.
    - **`AWN_date_mise_en_circulation`** (String): The date the vehicle was put into circulation.
    - **`AWN_date_30`** (String): The date the vehicle was put into circulation.
    - **`AWN_numero_de_serie`** (String): The serial number of the vehicle.
    - **`AWN_nbr_cylindres`** (String): The number of cylinders of the vehicle.
    - **`AWN_nbr_cylindre_energie`**: The number of cylinders in the vehicle's engine.
    - **`AWN_collection`**: A string indicating whether the vehicle is part of a collection or not.
    - **`AWN_puissance_KW`**: The power output of the engine in kilowatts.
    - **`AWN_code_moteur`**: The engine code.
    - **`AWN_nbr_volume`**: The number of engine cylinders.
    - **`AWN_nbr_vitesses`**: The number of gears in the transmission.
    - **`AWN_nbr_portes`**: The number of doors on the vehicle.
    - **`AWN_nbr_de_places`**: The number of seats in the vehicle.
    - **`AWN_nbr_soupapes`**: The number of engine valves.
    - **`AWN_type_boite_vites`**: The type of transmission, either manual or automatic.
    - **`AWN_turbo_Comprressor`**: A string indicating whether the engine is turbocharged or not.
    - **`AWN_depollution`**: A string indicating the level of emission control on the engine.
    - **`AWN_empattement`**: The wheelbase of the vehicle.
    - **`AWN_consommation_urbaine`**: The average fuel consumption of the vehicle in an urban setting.
    - **`AWN_consommation_ex_urbaine`**: The average fuel consumption of the vehicle in an extra-urban setting.
    - **`AWN_consommation_mixte`**: The average combined fuel consumption of the vehicle.
    - **`AWN_mode_injection`**: The type of fuel injection used by the engine.
    - **`AWN_prix`**: The price of the vehicle.
    - **`AWN_propulsion`**: The drive configuration of the vehicle, either front-wheel or rear-wheel.
    - **`AWN_libelle`**: A string describing the engine.
    - **`AWN_TID`**: A unique identifier for the vehicle.
    - **`AWN_country`**: The country of origin for the vehicle.
    - **`AWN_brand_img_path`**: The relative path to the brand's logo.
    - **`AWN_brand_img_full_path`**: The full URL to the brand's logo.
    - **`AWN_output_lang`**: The language in which the response was generated.

## Notes :

- The API requires a valid token for authentication.
- The plaque parameter must be in the format "AB123CD" or “AA-123-BC”.