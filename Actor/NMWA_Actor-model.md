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

#### Literal Node: `http://vocab.getty.edu/aat/300379842`
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

#### _AppelationURI_
From column: _Display Name_
``` python
return getValue("Display Name")
```

#### _NameURI_
From column: _Display Name_
``` python
return getValue("ConstituentURI")+"/name"
```

#### _AlphaSortURI_
From column: _Alpha Sort_
``` python
return getValue("ConstituentURI")+"/alpha_sort"
```

#### _AlphaSortLabel_
From column: _Alpha Sort_
``` python
return getValue("Alpha Sort")
```

#### _BirthURI_
From column: _Birth Year_
``` python
if getValue("Birth Year") == '':
    return ""
else:
    return getValue("ConstituentURI")+"/birth"
```

#### _BirthYearURI_
From column: _Birth Year_
``` python
if getValue("Birth Year") == '':
    return ""
else:
     return getValue("ConstituentURI")+"/birth_year"
```

#### _BirthYearBegin_
From column: _Birth Year_
``` python
if getValue("Birth Year") == '':
    return ""
elif '/' in getValue("Birth Year"):
    return getValue("Birth Year")
else:
    return  getValue("Birth Year")+"-01-01"
```

#### _BirthYearEnd_
From column: _Birth Year_
``` python
if getValue("Birth Year") == '':
    return ""
elif '/' in getValue("Birth Year"):
    return getValue("Birth Year")
else:
    return  getValue("Birth Year")+"-12-31"
```

#### _DeathURI_
From column: _Death Year _
``` python
if getValue("Death Year ") == '':
    return ""
else:
    return getValue("ConstituentURI")+"/death"
```

#### _DeathYearURI_
From column: _Death Year _
``` python
if getValue("Death Year ") == '':
    return ""
else:
     return getValue("ConstituentURI")+"/death_year"
```

#### _DeathYearBegin_
From column: _Death Year _
``` python
if getValue("Death Year ") == '':
    return ""
elif '/' in getValue("Death Year "):
    return getValue("Death Year ")
else:
    return  getValue("Death Year ")+"-01-01"
```

#### _DeathYearEnd_
From column: _Death Year _
``` python
if getValue("Death Year ") == '':
    return ""
elif '/' in getValue("Death Year "):
    return getValue("Death Year ")
else:
    return  getValue("Death Year ")+"-12-31"
```

#### _NationalityURI_
From column: _Nationality _
``` python
if getValue("Nationality "):
    return UM.uri_from_fields("thesauiri/nationality/",getValue("Nationality "))
else:
    return ""
```

#### _BirthPlaceURI_
From column: _Birth place_
``` python
if getValue("Birth place"):
    return UM.uri_from_fields("thesauiri/location/",getValue("Birth place"))
else:
    return ""
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Alpha Sort_ | `rdf:value` | `crm:E82_Actor_Appellation2`|
| _AlphaSortLabel_ | `rdfs:label` | `crm:E82_Actor_Appellation2`|
| _AlphaSortURI_ | `uri` | `crm:E82_Actor_Appellation2`|
| _AppelationURI_ | `rdfs:label` | `crm:E82_Actor_Appellation1`|
| _Birth Year_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _Birth place_ | `rdfs:label` | `crm:E53_Place1`|
| _BirthPlaceURI_ | `uri` | `crm:E53_Place1`|
| _BirthURI_ | `uri` | `crm:E63_Beginning_of_Existence1`|
| _BirthYearBegin_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _BirthYearEnd_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _BirthYearURI_ | `uri` | `crm:E52_Time-Span1`|
| _ConstituentURI_ | `uri` | `crm:E39_Actor1`|
| _Death Year _ | `rdfs:label` | `crm:E52_Time-Span2`|
| _DeathURI_ | `uri` | `crm:E64_End_of_Existence1`|
| _DeathYearBegin_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span2`|
| _DeathYearEnd_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span2`|
| _DeathYearURI_ | `uri` | `crm:E52_Time-Span2`|
| _Display Name_ | `rdf:value` | `crm:E82_Actor_Appellation1`|
| _NameLabel_ | `rdfs:label` | `crm:E39_Actor1`|
| _NameURI_ | `uri` | `crm:E82_Actor_Appellation1`|
| _Nationality _ | `rdfs:label` | `crm:E74_Group1`|
| _NationalityURI_ | `uri` | `crm:E74_Group1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E39_Actor1` | `crm:P92i_was_brought_into_existence_by` | `crm:E63_Beginning_of_Existence1`|
| `crm:E39_Actor1` | `crm:P93i_was_taken_out_of_existence_by` | `crm:E64_End_of_Existence1`|
| `crm:E39_Actor1` | `crm:P107i_is_current_or_former_member_of` | `crm:E74_Group1`|
| `crm:E39_Actor1` | `crm:P131_is_identified_by` | `crm:E82_Actor_Appellation1`|
| `crm:E39_Actor1` | `crm:P131_is_identified_by` | `crm:E82_Actor_Appellation2`|
| `crm:E63_Beginning_of_Existence1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E63_Beginning_of_Existence1` | `crm:P7_took_place_at` | `crm:E53_Place1`|
| `crm:E64_End_of_Existence1` | `crm:P4_has_time-span` | `crm:E52_Time-Span2`|
| `crm:E74_Group1` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300379842`|
| `crm:E82_Actor_Appellation1` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404670`|
| `crm:E82_Actor_Appellation2` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404672`|
