# NMWA_Data.csv

## Add Column

## Add Node/Literal
#### Literal Node: `http://vocab.getty.edu/aat/300404670`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404621`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300026687`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300179869`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300015646`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300080091`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/ulan/500404082`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`


## PyTransforms
#### _ObjectURI_
From column: _ObjectID_
``` python
return "object/"+getValue("ObjectID")
```

#### _ObjectIdURI_
From column: _ObjectID_
``` python
return getValue("ObjectURI")+"/pref_id"
```

#### _ObjectIdLabel_
From column: _ObjectID_
``` python
return getValue("ObjectID")
```

#### _ObjectNumberURI_
From column: _Object Number_
``` python
return getValue("ObjectURI")+"/object_number"
```

#### _ObjectNumberLabel_
From column: _Object Number_
``` python
return getValue("Object Number")
```

#### _CreditURI_
From column: _Credit_
``` python
return getValue("ObjectURI")+"/credit"
```

#### _DepartmentURI_
From column: _Department_
``` python
return UM.uri_from_fields("thesauri/department/",getValue("Department"))
```

#### _ClassificationURI_
From column: _Classification_
``` python
if getValue("Classification"):
    return UM.uri_from_fields("thesauri/classification/",getValue("Classification"))
else:
    return ""
```

#### _ClassificationTypeURI_
From column: _Classification_
``` python
return getValue("ObjectURI")+"/classification"
```

#### _CultureURI_
From column: _Culture_
``` python
if getValue("Culture"):
    return UM.uri_from_fields("thesauri/culture/",getValue("Culture"))
else:
    return ""
```

#### _CultureTypeURI_
From column: _Culture_
``` python
if getValue("Culture"):
    return getValue("ObjectURI")+"/culture_type"
else:
    return ""
```

#### _ActorURI_
From column: _Display Name_
``` python
return "constituent/"+SM.fingerprint_string(getValue("Display Name"))
```

#### _ProductionURI_
From column: _Display Name_
``` python
if getValue("TimeSpanURI") or getValue("ActorURI"):
  return getValue("ObjectURI")+"/production"
else:
  return ""
```

#### _BeginDateValid_
From column: _Begin Date_
``` python
if getValue("Begin Date")!='0': 
    return getValue("Begin Date") + "-01-01"
else:
    return ""
```

#### _TimeSpanURI_
From column: _Dated_
``` python
if getValue("Dated"):
    return getValue("ObjectURI") + "/timespan"
else:
    return ""
```

#### _Begin Date_
From column: _Begin Date_
``` python
return getValue("Begin Date")
```

#### _EndDateValid_
From column: _Begin Date_
``` python
if getValue("Begin Date")!='0': 
    return getValue("Begin Date") + "-12-31"
else:
    return ""
```

#### _DateLabel_
From column: _Begin Date_
``` python
if getValue("BeginDateValid"):
    return getValue("BeginDateValid") + " to " + getValue("EndDateValid")
else:
    return ""
```

#### _TitleURI_
From column: _Title_
``` python
if getValue("Title"):
    return UM.uri_from_fields("thesauri/title/",getValue("Title"))
else:
    return ""
```

#### _TitleLabel_
From column: _Title_
``` python
return getValue("Title")
```

#### _MaterialURI_
From column: _Medium_
``` python
return UM.uri_from_fields("thesauiri/material/",getValue("Medium"))
```

#### _DimensionURI_
From column: _Dimensions_
``` python
return getValue("ObjectURI")+"/dimension"
```

#### _DescriptionURI_
From column: _Description_
``` python
if getValue("Description"):
    return getValue("ObjectURI")+"/description"
else:
    return ""
```

#### _ObjectURL_
From column: _Object Details Web Page/ Link to Object on Website_
``` python
if getValue("Object Details Web Page/ Link to Object on Website") == "None":
    return ""
else:
     return getValue("Object Details Web Page/ Link to Object on Website")
```

#### _ObjectURLLabel_
From column: _ObjectURL_
``` python
return getValue("ObjectURL")
```

#### _ImageURL_
From column: _Image Full Size URL_
``` python
if getValue("Image Full Size URL"):
    return getValue("Image Full Size URL")
else:
    return ""
```

#### _OwnerURI_
From column: _ObjectID_
``` python
return "http://data.wildlifeart.org"
```

#### _OwnerLabel_
From column: _ObjectID_
``` python
return "National Museum of Wildlife Art"
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _ActorURI_ | `uri` | `crm:E39_Actor1`|
| _BeginDateValid_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _Classification_ | `rdfs:label` | `crm:E55_Type2`|
| _ClassificationTypeURI_ | `uri` | `crm:E17_Type_Assignment1`|
| _ClassificationURI_ | `uri` | `crm:E55_Type2`|
| _Credit_ | `rdf:value` | `crm:E33_Linguistic_Object1`|
| _CreditURI_ | `uri` | `crm:E33_Linguistic_Object1`|
| _Culture_ | `rdfs:label` | `crm:E55_Type3`|
| _CultureTypeURI_ | `uri` | `crm:E55_Type3`|
| _CultureURI_ | `uri` | `crm:E17_Type_Assignment2`|
| _Dated_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _Department_ | `rdf:value` | `crm:E55_Type1`|
| _DepartmentURI_ | `uri` | `crm:E55_Type1`|
| _Description_ | `rdf:value` | `crm:E33_Linguistic_Object3`|
| _DescriptionURI_ | `uri` | `crm:E33_Linguistic_Object3`|
| _DimensionURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _Dimensions_ | `rdf:value` | `crm:E33_Linguistic_Object2`|
| _EndDateValid_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _ImageURL_ | `uri` | `crm:E38_Image1`|
| _MaterialURI_ | `uri` | `crm:E57_Material1`|
| _Medium_ | `skos:prefLabel` | `crm:E57_Material1`|
| _Object Number_ | `rdf:value` | `crm:E42_Identifier2`|
| _ObjectID_ | `rdf:value` | `crm:E42_Identifier1`|
| _ObjectIdLabel_ | `rdfs:label` | `crm:E42_Identifier1`|
| _ObjectIdURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectNumberLabel_ | `rdfs:label` | `crm:E42_Identifier2`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier2`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ObjectURL_ | `uri` | `foaf:Document1`|
| _ObjectURLLabel_ | `rdfs:label` | `foaf:Document1`|
| _OwnerLabel_ | `rdfs:label` | `crm:E40_Legal_Body1`|
| _OwnerURI_ | `uri` | `crm:E40_Legal_Body1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _TimeSpanURI_ | `uri` | `crm:E52_Time-Span1`|
| _Title_ | `rdf:value` | `crm:E35_Title1`|
| _TitleLabel_ | `rdfs:label` | `crm:E22_Man-Made_Object1`|
| _TitleURI_ | `uri` | `crm:E35_Title1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E12_Production1` | `crm:P14_carried_out_by` | `crm:E39_Actor1`|
| `crm:E12_Production1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E17_Type_Assignment1` | `crm:P42_assigned` | `crm:E55_Type2`|
| `crm:E17_Type_Assignment1` | `crm:P21_had_general_purpose` | `http://vocab.getty.edu/aat/300179869`|
| `crm:E17_Type_Assignment2` | `crm:P42_assigned` | `crm:E55_Type3`|
| `crm:E17_Type_Assignment2` | `crm:P21_had_general_purpose` | `http://vocab.getty.edu/aat/300015646`|
| `crm:E22_Man-Made_Object1` | `crm:P108i_was_produced_by` | `crm:E12_Production1`|
| `crm:E22_Man-Made_Object1` | `crm:P41i_was_classified_by` | `crm:E17_Type_Assignment1`|
| `crm:E22_Man-Made_Object1` | `crm:P41i_was_classified_by` | `crm:E17_Type_Assignment2`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object1`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object2`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object3`|
| `crm:E22_Man-Made_Object1` | `crm:P102_has_title` | `crm:E35_Title1`|
| `crm:E22_Man-Made_Object1` | `crm:P138i_has_representation` | `crm:E38_Image1`|
| `crm:E22_Man-Made_Object1` | `crm:P52_has_current_owner` | `crm:E40_Legal_Body1`|
| `crm:E22_Man-Made_Object1` | `crm:P1_is_identified_by` | `crm:E42_Identifier1`|
| `crm:E22_Man-Made_Object1` | `crm:P1_is_identified_by` | `crm:E42_Identifier2`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type1`|
| `crm:E22_Man-Made_Object1` | `crm:P45_consists_of` | `crm:E57_Material1`|
| `crm:E22_Man-Made_Object1` | `foaf:homepage` | `foaf:Document1`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type3`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type2`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object1`|
| `crm:E33_Linguistic_Object1` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300026687`|
| `crm:E33_Linguistic_Object3` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300080091`|
| `crm:E33_Linguistic_Object3` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404670`|
| `crm:E35_Title1` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404670`|
| `crm:E40_Legal_Body1` | `skos:exactMatch` | `http://vocab.getty.edu/ulan/500404082`|
| `crm:E42_Identifier1` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404670`|
| `crm:E42_Identifier2` | `crm:P2_has_type` | `http://vocab.getty.edu/aat/300404621`|
