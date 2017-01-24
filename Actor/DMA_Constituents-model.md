# Dallas Museum of Art - LOD - UPDATED.csv

## Add Column

## Add Node/Literal
#### Literal Node: `http://vocab.getty.edu/aat/300379842`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404670`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300055147`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`


## PyTransforms
#### _ConstituentURI_
From column: _ConstituentEndDate_
``` python
return "constituent/"+SM.fingerprint_string(getValue("DisplayName"))
```

#### _NameLabel_
From column: _DisplayName_
``` python
return getValue("DisplayName")
```

#### _GenderURI_
From column: _FirstName_
``` python
return getValue("ConstituentURI")+"/gender"
```

#### _NameURI_
From column: _ConstituentURI_
``` python
return getValue("ConstituentURI")+"/name"
```

#### _BirthURI_
From column: _DimensionsDisplayText_
``` python
return getValue("ConstituentURI")+"/birth"
```

#### _BirthYearURI_
From column: _BirthURI_
``` python
return getValue("BirthURI")+"/birth_year"
```

#### _DeathURI_
From column: _CreatorDispOrder_
``` python
return getValue("ConstituentURI")+"/death"
```

#### _DeathYearURI_
From column: _DeathURI_
``` python
return getValue("DeathURI")+"/death_year"
```

#### _NationalityURI_
From column: _BirthDeathDisplayDate_
``` python
return getValue("ConstituentURI")+"/nationality"
```

#### _BirthDateEnd_
From column: _ConstituentBeginDate_
``` python
return getValue("ConstituentBeginDate")
```

#### _DeathDateBegin_
From column: _ConstituentEndDate_
``` python
return getValue("ConstituentEndDate")
```

#### _DeathDisplayDate_
From column: _ConstituentEndDate_
``` python
return getValue("BirthDeathDisplayDate")
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _BeginDateEnd_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _BirthDeathDisplayDate_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _BirthURI_ | `uri` | `crm:E63_Beginning_of_Existence1`|
| _BirthYearURI_ | `uri` | `crm:E52_Time-Span1`|
| _ConstituentBeginDate_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _ConstituentEndDate_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span2`|
| _ConstituentURI_ | `uri` | `crm:E39_Actor1`|
| _DeathDateBegin_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span2`|
| _DeathDisplayDate_ | `rdfs:label` | `crm:E52_Time-Span2`|
| _DeathURI_ | `uri` | `crm:E64_End_of_Existence1`|
| _DeathYearURI_ | `uri` | `crm:E52_Time-Span2`|
| _DisplayName_ | `rdf:value` | `crm:E82_Actor_Appellation1`|
| _Gender_ | `rdfs:label` | `crm:E55_Type1`|
| _GenderURI_ | `uri` | `crm:E55_Type1`|
| _NameLabel_ | `rdfs:label` | `crm:E39_Actor1`|
| _NameURI_ | `uri` | `crm:E82_Actor_Appellation1`|
| _Nationality_ | `rdfs:label` | `crm:E74_Group1`|
| _NationalityURI_ | `uri` | `crm:E74_Group1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E39_Actor1` | `crm:P2_has_type` | `crm:E55_Type1`|
| `crm:E39_Actor1` | `crm:P92i_was_brought_into_existence_by` | `crm:E63_Beginning_of_Existence1`|
| `crm:E39_Actor1` | `crm:P93i_was_taken_out_of_existence_by` | `crm:E64_End_of_Existence1`|
| `crm:E39_Actor1` | `crm:P107i_is_current_or_former_member_of` | `crm:E74_Group1`|
| `crm:E39_Actor1` | `crm:P131_is_identified_by` | `crm:E82_Actor_Appellation1`|
| `crm:E55_Type1` | `skos:broadMatch` | `xsd:http://vocab.getty.edu/aat/300055147`|
| `crm:E63_Beginning_of_Existence1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E64_End_of_Existence1` | `crm:P4_has_time-span` | `crm:E52_Time-Span2`|
| `crm:E74_Group1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300379842`|
| `crm:E82_Actor_Appellation1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404670`|
