# Base URL

https://reference.azure.net/v1

# RESOURCES

## Country

| Name | Description |
|:-----|:------------|
| Id | Identifier | 
| Code | Country Code. Uses the ISO 3166-1 alpha-2 standard | 
| Name | Country name | 
| Version | Latest version number | 
| States | States/Provinces | 

## State

| Name | Description |
|:-----|:------------|
| Name | Country name | 
| Code | State/Province Code. Based off the ISO 3166-2 standard | 

## TimeZone

| Name | Description |
|:-----|:------------|
| Id  | Identifier | 
| Name | Name | 
| SupportsDaylightSavingTime | A flag to indicate if this TimeZone observes Daylight Savings Time | 

## Currency

To represent a Currency symbol in unicode, use the format <code>&#(Code);</code>, for USD this would be <code>&#36;</code> which is displayed as &#36;.

| Name | Description |
|:-----|:------------|
| Id | Identifier | 
| Name | Currency Name | 
| Code | Identifier for the Currency | 
| Symbol | Unicode decimal value for symbols associated with this currency | 
| Version | Latest version number | 

# REQUESTS

## Get All Countries

### Request

```
GET /Countries
```

### Example Request

```javascript
GET /Countries
Accept: application/json
```

### Example Response

> Example Response

```
HTTP 200 Content-Type: application/json
```

```json
[
    {
        "Id": 1,
        "Code": "CA",
        "Name": "Canada",
        "Version": 1,
        "States": [
            {
                "Name": "Alberta",
                "Code": "AB"
            }
        ]
    }
]
```

## Get All Time Zones

### Request

```
GET /TimeZones
```

### Example Request

```javascript
GET /TimeZones
Accept: application/json
```

### Example Response

```
HTTP 200 Content-Type: application/json
```

```json
[
    {
        "Id": "Alaskan Standard Time",
        "Name": "(UTC-09:00) Alaska",
        "SupportsDaylightSavingTime": true
    }
]
```

## Get All Currencies

Currency resources are returned in ascending alphabetical order by Code.

### Request

```
GET /Currencies
```

### Example Request

```javascript
GET /Currencies
Accept: application/json
```

### Example Response

```
HTTP 200 Content-Type: application/json
```

```json
[
    {
        "Id": 106,
        "Name": "United States Dollar",
        "Code": "USD",
        "Symbol": [
            36
        ],
        "Version": 1
    }
]
```