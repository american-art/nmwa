# NMWA_Data.csv

## Add Column

## Add Node/Literal
#### Literal Node: `http://vocab.getty.edu/aat/300404670`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404672`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`


## PyTransforms
#### _ConstituentURI_
From column: _Display Name_
``` python
return "constituent/"+SM.fingerprint_string(getValue("Display Name"))
```

#### _NameLabel_
From column: _Display Name_
``` python
return getValue("Display Name")
```

#### _PrimaryNameURI_
From column: _Column_3_
``` python
return getValue("ConstituentURI")+"/name"
```

#### _AlphaSortURI_
From column: _Alpha Sort_
``` python
return getValue("ConstituentURI")+"/alpha_sort"
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Alpha Sort_ | `rdf:value` | `crm:E82_Actor_Appellation2`|
| _AlphaSortURI_ | `uri` | `crm:E82_Actor_Appellation2`|
| _ConstituentURI_ | `uri` | `crm:E39_Actor1`|
| _Display Name_ | `rdf:value` | `crm:E82_Actor_Appellation1`|
| _NameLabel_ | `rdfs:label` | `crm:E39_Actor1`|
| _PrimaryNameURI_ | `uri` | `crm:E82_Actor_Appellation1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E39_Actor1` | `crm:P1_is_identified_by` | `crm:E82_Actor_Appellation1`|
| `crm:E39_Actor1` | `crm:P1_is_identified_by` | `crm:E82_Actor_Appellation2`|
| `crm:E82_Actor_Appellation1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404670`|
| `crm:E82_Actor_Appellation2` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404672`|
