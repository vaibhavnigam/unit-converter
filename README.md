# unit-converter
A sample springboot RESTful project

To run the application:
`$ docker-compose up`

`$ gradle bootRun`


Available endpoints:

### POST/GET `/configurations`

eg: `POST /configurations`
```
{
    "category": "weight",
    "baseUnit": "grams"
}
```

### POST/GET `/configurations/{category}`

eg: `POST /configurations/weight`
```
{
    "targetUnit": "kilograms",
    "factor": "0.001"
}
```

### GET `/conversions/weight?fromUnit=kilograms&value=10`
eg: Response:

```
{
    conversions:[
        {
            "unit": "grams",
            "value": 10000
        },
        {
            "unit": "kilograms",
            "value": 1
        },
        {
            "unit": "pounds",
            "value": 22.04623
        }
    ]
}
```
