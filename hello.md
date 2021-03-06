FORMAT: 1A
HOST: http://innovated.qinmoxi.cn/service/public/index.php

# Quotation API

This is a API to query some information of quotation system.

# Group Manufacturer & Model
API-related resources of *Make & Model API*.

## Manufacturer [/makeModel/all-makes]
Query information of makes

The Manufacturer resource has the following attributes:

- success 
- data
- msg

### List All Manufacturer [POST]
This API will get all of the *Manufacturers*.

+ Response 200 (application/json)

        [
            {
                "success": true,
                "msg": "",
                "data": [
                    {
                        "vcode_id": "Audi",
                        "vcode_name": 1
                    }, {
                        "vcode_id": "BMW",
                        "vcode_name": 2
                    }, {
                        "vcode_id": "Mazda",
                        "vcode_name": 3
                    }
                ]
            }
        ]
    
## Model [/makeModel/models]
Query information of models of one make

The Model resource has the following attributes:

- success 
- data
- msg


### List Models of One Manufacturer [POST]

To query the models of the manufacturer provide a JSON hash of *ID number of the make*

+ Request (application/json)

        {
            "make_id": "12"
        }

+ Response 200 (application/json)

        [
            {
                "success": true,
                "msg": "",
                "data": [
                    {
                        "vcode_id": "Audi",
                        "vcode_name": 1
                    }, {
                        "vcode_id": "BMW",
                        "vcode_name": 2
                    }
                ]
            }
        ]

