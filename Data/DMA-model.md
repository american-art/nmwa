# Dallas Museum of Art - LOD - UPDATED.csv

## Add Column

## Add Node/Literal
#### Literal Node: `http://vocab.getty.edu/aat/300179869`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300026687`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/30008091`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404670`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300266036`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`


## PyTransforms
#### _ObjectURI_
From column: _ObjectID_
``` python
return "object/"+getValue("ObjectID")
```

#### _ClassificationAssignmentURI_
From column: _ObjectURI_
``` python
return getValue("ObjectURI")+"/classification_assignment"
```

#### _Classification_
From column: _ClassificationAssignmentURI_
``` python
return UM.uri_from_fields("thesauri/classification/",getValue("ClassificationObject"))
```

#### _CreditURI_
From column: _Copyright_
``` python
return getValue("ObjectURI")+"/credit"
```

#### _CopyrightURI_
From column: _ClassificationObject_
``` python
return getValue("ObjectURI")+"/copyright"
```

#### _ProductionURI_
From column: _DataDateStamp_
``` python
if getValue("DateBegin")!="0":
    return getValue("ObjectURI")+"/production"
else:
    return ""
```

#### _DateURI_
From column: _ProductionURI_
``` python
if getValue("ProductionURI"):
    return getValue("ProductionURI")+"/date"
else:
    return ""
```

#### _ObjectNumberLabel_
From column: _ObjectNumber_
``` python
return getValue("ObjectNumber")
```

#### _ObjectNumberURI_
From column: _ObjectOwned_
``` python
return getValue("ObjectURI")+"/object_number"
```

#### _MaterialURI_
From column: _ResourceURL_
``` python
return UM.uri_from_fields("thesauri/material/",getValue("Medium"))
```

#### _DescriptionURI_
From column: _ObjectNumberLabel_
``` python
if getValue("PublicDescription"):
    return getValue("ObjectURI")+"/description"
else:
    return ""
```

#### _DimensionURI_
From column: _Medium_
``` python
if getValue("DimensionsDisplayText"):
    return getValue("ObjectURI")+"/dimension"
else:
    return ""
```

#### _Role_
From column: _Role_
``` python
return getValue("Role")
```

#### _TitleURI_
From column: _Role_
``` python
return UM.uri_from_fields("thesauri/title/",getValue("Title"))
```

#### _TitleLabel_
From column: _Title_
``` python
return getValue("Title")
```

#### _ImageURLClean_
From column: _ImageURL_
``` python
if getValue("ImageURL"):
    return getValue("ImageURL")
else:
    return ""
```

#### _ObjectUrlURI_
From column: _PublicDescription_
``` python
if getValue("ResourceURL"):
    return getValue("ResourceURL")
else:
    return ""
```

#### _ArtistURI_
From column: _Role_
``` python
if getValue("Role") in ['Artist','Author','Engraver']:
    return "constituent/"+SM.fingerprint_string(getValue(("DisplayName")))
else:
    return ""
```

#### _SubjectURI_
From column: _Role_
``` python
if getValue("Role")=="Depicted individual":
    return "constituent/"+SM.fingerprint_string(getValue("DisplayName"))
else:
    return ""
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _ArtistURI_ | `crm:P14_carried_out_by` | `crm:E12_Production1`|
| _Classification_ | `uri` | `crm:E55_Type1`|
| _ClassificationAssignmentURI_ | `uri` | `crm:E17_Type_Assignment1`|
| _ClassificationObject_ | `rdfs:label` | `crm:E55_Type1`|
| _Copyright_ | `crm:P3_has_note` | `crm:E30_Right1`|
| _CopyrightURI_ | `uri` | `crm:E30_Right1`|
| _CreditLine_ | `rdf:value` | `crm:E33_Linguistic_Object1`|
| _CreditURI_ | `uri` | `crm:E33_Linguistic_Object1`|
| _DateBegin_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _DateEnd_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _DateURI_ | `uri` | `crm:E52_Time-Span1`|
| _Dated_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _DescriptionURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _DimensionURI_ | `uri` | `crm:E33_Linguistic_Object3`|
| _DimensionsDisplayText_ | `rdf:value` | `crm:E33_Linguistic_Object3`|
| _ImageURLClean_ | `uri` | `crm:E38_Image1`|
| _MaterialURI_ | `uri` | `crm:E57_Material1`|
| _Medium_ | `skos:prefLabel` | `crm:E57_Material1`|
| _ObjectNumber_ | `rdf:value` | `crm:E42_Identifier1`|
| _ObjectNumberLabel_ | `rdfs:label` | `crm:E42_Identifier1`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ObjectUrlURI_ | `uri` | `foaf:Document1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _PublicDescription_ | `rdf:value` | `crm:E33_Linguistic_Object2`|
| _ResourceURL_ | `rdfs:label` | `foaf:Document1`|
| _SubjectURI_ | `crm:P62_depicts` | `crm:E22_Man-Made_Object1`|
| _Title_ | `rdf:value` | `crm:E35_Title1`|
| _TitleLabel_ | `rdfs:label` | `crm:E22_Man-Made_Object1`|
| _TitleURI_ | `uri` | `crm:E35_Title1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E12_Production1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E17_Type_Assignment1` | `crm:P42_assigned` | `crm:E55_Type1`|
| `crm:E17_Type_Assignment1` | `crm:P21_had_general_purpose` | `xsd:http://vocab.getty.edu/aat/300179869`|
| `crm:E22_Man-Made_Object1` | `crm:P108i_was_produced_by` | `crm:E12_Production1`|
| `crm:E22_Man-Made_Object1` | `crm:P41i_was_classified_by` | `crm:E17_Type_Assignment1`|
| `crm:E22_Man-Made_Object1` | `crm:P104_is_subject_to` | `crm:E30_Right1`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object1`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object2`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object3`|
| `crm:E22_Man-Made_Object1` | `crm:P102_has_title` | `crm:E35_Title1`|
| `crm:E22_Man-Made_Object1` | `crm:P138i_has_representation` | `crm:E38_Image1`|
| `crm:E22_Man-Made_Object1` | `crm:P48_has_preferred_identifier` | `crm:E42_Identifier1`|
| `crm:E22_Man-Made_Object1` | `crm:P45_consists_of` | `crm:E57_Material1`|
| `crm:E22_Man-Made_Object1` | `foaf:homepage` | `foaf:Document1`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type1`|
| `crm:E33_Linguistic_Object1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300026687`|
| `crm:E33_Linguistic_Object2` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404670`|
| `crm:E33_Linguistic_Object2` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/30008091`|
| `crm:E33_Linguistic_Object3` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300266036`|
| `crm:E35_Title1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404670`|
