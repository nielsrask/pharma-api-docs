# E-Prescription API endpoints
## URL
`https://eprescriptionapi.prodentor.se`

# Pharmaceutical Articles
`/api/pharmaceutical-articles`

Pharmaceutical Articles resource representation.

## Get Pharmaceutical Articles
`GET /api/pharmaceutical-articles/{occupational_code,?query,?article_code}`


+ Parameters
    + occupational_code: (string, required) - LAK,ATL,LMF,TAN,TAH,SSK,BMO,HJM,VET.
    + query: (string, optional) - For additional filtering.
    + npl_pack_id: (string, optional) - Get first pharmaceutical article by npl pack Id.
    + npl_id: (string, optional) - Get unique pharmaceutical article by npl pack Id and npl Id.
    + article_code: (string, optional) - Get first pharmaceutical article by article code.

+ Request (application/json)
    + Headers

            Accept: application/x.eprescription.v1+json
            Content-Type: application/json
    + Body

            {
                "occupational_code": "required|string",
                "query": "optional|string"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "type": "pharmaceutical_article",
                        "id": "8",
                        "attributes": {
                            "article_code": "487579",
                            "article_name": "Brufen Retard",
                            "is_pharmaceutical": true,
                            "assortment_code": null,
                            "drug_form": "Depottablett",
                            "high_risk_pharmaceutical": false,
                            "is_reimbursed": true,
                            "manufacturer_name": "BGP Products AB",
                            "non_approved": false,
                            "npl_pack_id": "19931001100315",
                            "npl_id": "19901012000010",
                            "package_text": "Blister, 30 tabletter",
                            "prescription_required": true,
                            "quantity_text": "30 styck",
                            "reference_price": "99.9600000000",
                            "sales_stopped": true,
                            "strength": "800 mg"
                        }
                    },
                    {
                        "type": "pharmaceutical_article",
                        "id": "9",
                        "attributes": {
                            "article_code": "463273",
                            "article_name": "Brufen Retard",
                            "is_pharmaceutical": true,
                            "assortment_code": null,
                            "drug_form": "Depottablett",
                            "high_risk_pharmaceutical": false,
                            "is_reimbursed": true,
                            "manufacturer_name": "BGP Products AB",
                            "non_approved": false,
                            "npl_pack_id": "19901001100189",
                            "npl_id": "19901012000010",
                            "package_text": "Burk, 100 tabletter",
                            "prescription_required": true,
                            "quantity_text": "100 styck",
                            "reference_price": "187.5900000000",
                            "sales_stopped": true,
                            "strength": "800 mg"
                        }
                    }
                ]
            }

+ Request (application/json)
    + Headers

            Accept: application/x.eprescription.v1+json
            Content-Type: application/json
    + Body

            {
                "occupational_code": "required|string",
                "article_code": "required|string"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "type": "pharmaceutical_article",
                    "id": "9",
                    "attributes": {
                        "article_code": "463273",
                        "article_name": "Brufen Retard",
                        "is_pharmaceutical": true,
                        "assortment_code": null,
                        "drug_form": "Depottablett",
                        "high_risk_pharmaceutical": false,
                        "is_reimbursed": true,
                        "manufacturer_name": "BGP Products AB",
                        "non_approved": false,
                        "npl_pack_id": "19901001100189",
                        "npl_id": "19901012000010",
                        "package_text": "Burk, 100 tabletter",
                        "prescription_required": true,
                        "quantity_text": "100 styck",
                        "reference_price": "187.5900000000",
                        "sales_stopped": true,
                        "strength": "800 mg"
                    }
                }
            }

+ Request (application/json)
    + Headers

            Accept: application/x.eprescription.v1+json
            Content-Type: application/json
    + Body

            {
                "occupational_code": "required|string",
                "npl_pack_id": "required|string",
                "npl_id": "optional|string"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "type": "pharmaceutical_article",
                    "id": "9",
                    "attributes": {
                        "article_code": "463273",
                        "article_name": "Brufen Retard",
                        "is_pharmaceutical": true,
                        "assortment_code": null,
                        "drug_form": "Depottablett",
                        "high_risk_pharmaceutical": false,
                        "is_reimbursed": true,
                        "manufacturer_name": "BGP Products AB",
                        "non_approved": false,
                        "npl_pack_id": "19901001100189",
                        "npl_id": "19901012000010",
                        "package_text": "Burk, 100 tabletter",
                        "prescription_required": true,
                        "quantity_text": "100 styck",
                        "reference_price": "187.5900000000",
                        "sales_stopped": true,
                        "strength": "800 mg"
                    }
                }
            }

# Pharmacies
`/api/pharmacies`

Pharmacies resource representation.

## Get Pharmacies
`GET /api/pharmacies/{occupational_code,?query,?code}`


+ Parameters
    + occupational_code: (string, required) - LAK,ATL,LMF,TAN,TAH,SSK,BMO,HJM,VET.
    + query: (string, optional) - For additional filtering.
    + code: (string, optional) - Get first pharmacy by code.

+ Request (application/json)
    + Headers

            Accept: application/x.eprescription.v1+json
            Content-Type: application/json
    + Body

            {
                "occupational_code": "required|string",
                "query": "optional|string"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": [
                    {
                        "type": "pharmacy",
                        "id": "1393",
                        "attributes": {
                            "code": "7312527003048",
                            "label": "KRONANS APOTEK ÄLMHULT SHOPPING",
                            "city": "ÄLMHULT"
                        }
                    },
                    {
                        "type": "pharmacy",
                        "id": "1400",
                        "attributes": {
                            "code": "7312527003444",
                            "label": "KRONANS APOTEK ÄLVSJÖ",
                            "city": "ÄLVSJÖ"
                        }
                    }
                ]
            }

+ Request (application/json)
    + Headers

            Accept: application/x.eprescription.v1+json
            Content-Type: application/json
    + Body

            {
                "occupational_code": "required|string",
                "code": "required|string"
            }

+ Response 200 (application/json)
    + Body

            {
                "data": {
                    "type": "pharmacy",
                    "id": "1393",
                    "attributes": {
                        "code": "7312527003048",
                        "label": "KRONANS APOTEK ÄLMHULT SHOPPING",
                        "city": "ÄLMHULT"
                    }
                }
            }
