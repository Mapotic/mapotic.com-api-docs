
List of POIs (geojson)
---

`/api/v1/maps/<map_id>/pois.geojson/`

Response example

```json
[
    {
        "type": "Feature",
        "properties": {
            "id": 4580,
            "category": 339,
            "slug": "petotem",
            "category_name": {
                "en": "Stanoviště"
            },
            "name": "PETOTEM",
            "rating": null,
            "event_status": "active",
            "is_published": true
        },
        "geometry": {
            "type": "Point",
            "coordinates": [
                12.325107,
                48.72772
            ]
        }
    }
]
```

### Filtering

Query params modificators:

#### Ordering by distance 
`center=13.27|49.73`

#### Limiting 
`limit=10`

#### Filtering by attributes
is provided by GET params. Invalid value (`t` for number field, `1,2,4` for boolean field, ...), or not available attribute is skipped.

`attr<attribute_id>([lt|lte|gt|gte])?=<attribute value>`

Posible values by attribute type:

    Select: <int>
    MultipleSelect: <int>,
    Boolean: t|f
    Number: <number>

#### Extra_fields
Available fields: `owner`, `created`, `address`
    
`extra_fields=owner,address`

#### Image 
`image=100x100`

### Example 

```
?attr297=69&attr245=t&attr549=3,4,7&attr223gte=256&image=256x256 
```


POI detail
---

`/api/v1/maps/<map_id>/public-pois/<poi_id>/`
