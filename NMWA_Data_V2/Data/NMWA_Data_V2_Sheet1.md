## NMWA_Data_Sheet1

### PyTransforms
#### _ObjectURI_
From column: _ObjectURI_
``` python
return "object/"+getValue("ObjectID")
```

#### _ObjectNumberURI_
From column: _ObjectNumberURI_
``` python
return getValue("ObjectURI")+"/object_number"
```

#### _ObjectNumberType_
From column: _ObjectNumberType_
``` python
return "aat:300404621"
```

#### _CreditURI_
From column: _CreditURI_
``` python
return getValue("ObjectURI")+"/credit"
```

#### _CreditType_
From column: _CreditType_
``` python
return "aat:300026687"
```

#### _ClassificationURI_
From column: _ClassificationURI_
``` python
return getValue("ObjectURI")+"/classification"
```

#### _CultureURI_
From column: _CultureURI_
``` python
if getValue("Culture"):
    return UM.uri_from_fields("thesauri/culture/",getValue("Culture"))
else:
    return ""
```

#### _PrimaryTitle_
From column: _PrimaryTitle_
``` python
return getValue("Title")
```

#### _PrimaryTitleURI_
From column: _PrimaryTitleURI_
``` python
return UM.uri_from_fields("thesauri/title/",getValue("Title"))
```

#### _PrimaryTitleType_
From column: _PrimaryTitleType_
``` python
return "aat:300404012"
```

#### _ProductionURI_
From column: _ProductionURI_
``` python
return getValue("ObjectURI")+"/production"
```

#### _ActorURI_
From column: _ActorURI_
``` python
return getValue("ObjectURI")+"/attribution"
```

#### _TimespanURI_
From column: _TimespanURI_
``` python
return getValue("ObjectURI")+"/timespan"
```

#### _DateValid_
From column: _DateValid_
``` python
if getValue("Dated")!="NA" and getValue("Dated")!="N/A" and getValue("Dated")!="n.d.":
    return getValue("Dated")
else:
    return ""
```

#### _BeginDateValid_
From column: _BeginDateValid_
``` python
if getValue("Begin Date"): 
    return getValue("Begin Date")
else:
    return ""
```

#### _MaterialURI_
From column: _MaterialURI_
``` python
return UM.uri_from_fields("material/",getValue("Medium"))
```

#### _DimensionURI_
From column: _DimensionURI_
``` python
return getValue("ObjectURI")+"/dimension"
```

#### _DescriptionURI_
From column: _DescriptionURI_
``` python
return getValue("ObjectURI")+"/description"
```

#### _ObjectURL1_
From column: _Object Details Web Page/ Link to Object on Website_
``` python
if getValue("Object Details Web Page/ Link to Object on Website") == "None":
    return ""
else:
     return getValue("Object Details Web Page/ Link to Object on Website")
```

#### _ObjectURLLabel_
From column: _ObjectURL1_
``` python
return getValue("ObjectURL1")
```

#### _ObjectNumberValue_
From column: _Object Number_
``` python
return getValue("Object Number")
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _ActorURI_ | `uri` | `crm:E39_Actor1`|
| _Attribution_ | `crm:P3_has_note` | `crm:E39_Actor1`|
| _Attribution_ | `crm:P3_has_note` | `crm:E39_Actor1`|
| _Attribution_ | `crm:P3_has_note` | `crm:E39_Actor2`|
| _AttributionURI_ | `uri` | `crm:E39_Actor2`|
| _BeginDate_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _BeginDateValid_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _Classification_ | `rdfs:label` | `crm:E55_Type3`|
| _ClassificationURI_ | `uri` | `crm:E55_Type3`|
| _ConTypeURI_ | `uri` | `crm:E55_Type1`|
| _ConstituentType_ | `rdfs:label` | `crm:E55_Type1`|
| _ConstituentURI_ | `uri` | `crm:E39_Actor1`|
| _CopyRightURI_ | `uri` | `crm:E30_Right1`|
| _Copyright_ | `crm:P3_has_note` | `crm:E30_Right1`|
| _Credit_ | `rdf:value` | `crm:E33_Linguistic_Object1`|
| _Credit_ | `crm:P3_has_note` | `crm:E82_Actor_Appellation1`|
| _CreditType_ | `crm:P2_has_type` | `crm:E33_Linguistic_Object1`|
| _CreditURI_ | `uri` | `crm:E33_Linguistic_Object1`|
| _Culture_ | `rdfs:label` | `crm:E55_Type4`|
| _Culture_ | `rdfs:label` | `crm:E55_Type2`|
| _CultureURI_ | `uri` | `crm:E55_Type4`|
| _CultureURI_ | `uri` | `crm:E55_Type2`|
| _DateURI_ | `uri` | `crm:E52_Time-Span1`|
| _DateURI_ | `uri` | `crm:E49_Time_Appellation1`|
| _DateValid_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _Dated_ | `rdfs:label` | `crm:E52_Time-Span1`|
| _Dated_ | `rdfs:label` | `crm:E49_Time_Appellation1`|
| _Dated_ | `crm:P3_has_note` | `crm:E52_Time-Span1`|
| _Department_ | `rdfs:label` | `crm:E55_Type6`|
| _Department_ | `rdfs:label` | `crm:E55_Type5`|
| _Department_ | `rdfs:label` | `crm:E55_Type3`|
| _DepartmentURI_ | `uri` | `crm:E55_Type6`|
| _DepartmentURI_ | `uri` | `crm:E55_Type5`|
| _Description_ | `rdf:value` | `crm:E33_Linguistic_Object3`|
| _Description_ | `crm:P3_has_note` | `crm:E33_Linguistic_Object1`|
| _Description_ | `rdfs:label` | `crm:E18_Physical_Thing1`|
| _DescriptionLinguisticObjectURI_ | `uri` | `crm:E33_Linguistic_Object3`|
| _DescriptionType_ | `uri` | `crm:E55_Type7`|
| _DescriptionURI_ | `uri` | `crm:E18_Physical_Thing1`|
| _DescriptionURI_ | `uri` | `crm:E33_Linguistic_Object3`|
| _DescriptionURI_ | `uri` | `crm:E33_Linguistic_Object1`|
| _DimensionLinguisticObjectURI_ | `uri` | `crm:E33_Linguistic_Object4`|
| _DimensionType_ | `uri` | `crm:E55_Type8`|
| _DimensionURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _DimensionURI_ | `uri` | `crm:E54_Dimension1`|
| _Dimensions_ | `rdf:value` | `crm:E33_Linguistic_Object2`|
| _Dimensions_ | `crm:P3_has_note` | `crm:E54_Dimension1`|
| _Display Name_ | `rdfs:label` | `crm:E39_Actor1`|
| _Display Name_ | `rdfs:label` | `crm:E39_Actor1`|
| _Display Name_ | `rdfs:label` | `crm:E82_Actor_Appellation2`|
| _DisplayDate_ | `crm:P62i_is_depicted_by` | `crm:E52_Time-Span1`|
| _DisplayNameURI_ | `uri` | `crm:E82_Actor_Appellation2`|
| _DisplayNameURI_ | `uri` | `crm:E82_Actor_Appellation1`|
| _EndDate_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _FirstName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _Image Full Size URL_ | `uri` | `crm:E38_Image1`|
| _Image Full Size URL_ | `crm:P3_has_note` | `crm:E38_Image1`|
| _ImageLinguisticObjectURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _ImageURI_ | `uri` | `crm:E38_Image1`|
| _Inscribed_ | `crm:P3_has_note` | `crm:E34_Inscription1`|
| _InscriptionURI_ | `uri` | `crm:E34_Inscription1`|
| _LastName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _LinguisticObjectURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _MaterialURI_ | `uri` | `crm:E57_Material1`|
| _MaterialURI_ | `uri` | `crm:E57_Material1`|
| _Media_ | `rdfs:label` | `crm:E55_Type4`|
| _MediaURI_ | `uri` | `crm:E55_Type4`|
| _Medium_ | `skos:prefLabel` | `crm:E57_Material1`|
| _Medium_ | `skos:prefLabel` | `crm:E57_Material1`|
| _Medium_ | `crm:P3_has_note` | `crm:E55_Type3`|
| _MediumURI_ | `uri` | `crm:E55_Type3`|
| _MiddleName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _NameTitle_ | `crm:P102_has_title` | `crm:E82_Actor_Appellation1`|
| _Object Number_ | `rdfs:label` | `crm:E42_Identifier1`|
| _Object Number_ | `rdfs:label` | `crm:E42_Identifier1`|
| _ObjectNumberType_ | `crm:P2_has_type` | `crm:E42_Identifier1`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectNumberValue_ | `rdf:value` | `crm:E42_Identifier1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ObjectURL1_ | `uri` | `foaf:Document1`|
| _ObjectURLLabel_ | `rdfs:label` | `foaf:Document1`|
| _Period_ | `rdfs:label` | `crm:E4_Period1`|
| _PeriodURI_ | `uri` | `crm:E4_Period1`|
| _PrimaryTitle_ | `rdfs:label` | `crm:E35_Title1`|
| _PrimaryTitleTranslationTypeURI_ | `uri` | `crm:E55_Type6`|
| _PrimaryTitleTransltionType_ | `rdfs:label` | `crm:E55_Type6`|
| _PrimaryTitleURI_ | `uri` | `crm:E35_Title1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _Suffix_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _TimespanURI_ | `uri` | `crm:E52_Time-Span1`|
| _Title_ | `rdfs:label` | `crm:E35_Title1`|
| _TitleURI_ | `uri` | `crm:E35_Title1`|
| _URL_ | `crm:P3_has_note` | `crm:E42_Identifier2`|
| _urlURI_ | `uri` | `crm:E42_Identifier2`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E12_Production1` | `crm:P14_carried_out_by` | `crm:E39_Actor1`|
| `crm:E12_Production1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E22_Man-Made_Object1` | `crm:P108i_was_produced_by` | `crm:E12_Production1`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object1`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object2`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object3`|
| `crm:E22_Man-Made_Object1` | `crm:P102_has_title` | `crm:E35_Title1`|
| `crm:E22_Man-Made_Object1` | `crm:P138i_has_representation` | `crm:E38_Image1`|
| `crm:E22_Man-Made_Object1` | `crm:P1_is_identified_by` | `crm:E42_Identifier1`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type3`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type4`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type6`|
| `crm:E22_Man-Made_Object1` | `crm:P45_consists_of` | `crm:E57_Material1`|
| `crm:E22_Man-Made_Object1` | `foaf:homepage` | `foaf:Document1`|
| `crm:E33_Linguistic_Object1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300026687`|
| `crm:E33_Linguistic_Object2` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300266036`|
| `crm:E33_Linguistic_Object3` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300080091`|
| `crm:E35_Title1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300403012`|
| `crm:E42_Identifier1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404621`|
