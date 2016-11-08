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

#### _DepartmentURI_
From column: _DepartmentURI_
``` python
return "thesauri/department/"+getValue("Department")
```

#### _CultureURI_
From column: _CultureURI_
``` python
if getValue("Culture"):
    return "thesauri/culture/"+getValue("Culture").lower().replace(' ', '_')
else:
    return ""
```

#### _ClassificationURI_
From column: _ClassificationURI_
``` python
if getValue("Classification"):
    return "thesauri/classification/"+getValue("Classification").lower().replace(' ', '_')
else:
    return ""
```

#### _MediaURI_
From column: _MediaURI_
``` python
return getValue("ObjectURI") + "/media"
```

#### _ProductionURI_
From column: _ProductionURI_
``` python
return getValue("ObjectURI") + "/production"
```

#### _DateURI_
From column: _DateURI_
``` python
return getValue("ProductionURI")+"/date"
```

#### _MediumURI_
From column: _MediumURI_
``` python
if getValue("Medium"):
    return "thesauri/medium/"+getValue("Medium").lower().replace(' ', '_')
else:
    return ""
```

#### _DimensionURI_
From column: _DimensionURI_
``` python
return getValue("ObjectURI")+"/dimensions"
```

#### _DescriptionURI_
From column: _DescriptionURI_
``` python
return getValue("ObjectURI")+"/description"
```

#### _AttributionURI_
From column: _AttributionURI_
``` python
return getValue("ObjectURI") + "/attribution"
```

#### _DisplayNameURI_
From column: _DisplayNameURI_
``` python
return getValue("ObjectURI") + "/displayName"
```

#### _PrimaryTitle_
From column: _PrimaryTitle_
``` python
return getValue("Title")
```

#### _PrimaryTitleURI_
From column: _PrimaryTitleURI_
``` python
if getValue("PrimaryTitle"):
    return "thesauri/title/" + getValue("Title").lower().replace(' ', '_')
else:
    return ''
```

#### _PrimaryTitleType_
From column: _PrimaryTitleType_
``` python
if getValue("PrimaryTitle"):
    return "thesauri/title/" + getValue("Title").lower().replace(' ', '_')
else:
    return ''
```

#### _PrimaryTitleTypeURI_
From column: _PrimaryTitleTypeURI_
``` python
if getValue("PrimaryTitle"):
    return "thesauri/title/" + getValue("Title").lower().replace(' ', '_')
else:
    return ''
```

#### _PrimaryTitleTranslationTypeURI_
From column: _PrimaryTitleTranslationTypeURI_
``` python
if getValue("PrimaryTitle"):
    return "Not Translatable"
else:
    return ''
```

#### _PrimaryTitleTransltionType_
From column: _PrimaryTitleTransltionType_
``` python
if getValue("PrimaryTitle"):
    return "thesauri/title/" + getValue("Title").lower().replace(' ', '_')
else:
    return ''
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Attribution_ | `crm:P3_has_note` | `crm:E39_Actor2`|
| _Attribution_ | `crm:P3_has_note` | `crm:E39_Actor2`|
| _AttributionURI_ | `uri` | `crm:E39_Actor2`|
| _AttributionURI_ | `uri` | `crm:E39_Actor2`|
| _BeginDate_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _Classification_ | `rdfs:label` | `crm:E55_Type1`|
| _ClassificationURI_ | `uri` | `crm:E55_Type1`|
| _ConTypeURI_ | `uri` | `crm:E55_Type1`|
| _ConstituentType_ | `rdfs:label` | `crm:E55_Type1`|
| _ConstituentURI_ | `uri` | `crm:E39_Actor1`|
| _Credit_ | `crm:P3_has_note` | `crm:E82_Actor_Appellation1`|
| _Credit_ | `crm:P3_has_note` | `crm:E82_Actor_Appellation1`|
| _CreditURI_ | `uri` | `crm:E82_Actor_Appellation1`|
| _Culture_ | `rdfs:label` | `crm:E55_Type5`|
| _Culture_ | `rdfs:label` | `crm:E55_Type2`|
| _CultureURI_ | `uri` | `crm:E55_Type2`|
| _CultureURI_ | `uri` | `crm:E55_Type5`|
| _DateURI_ | `uri` | `crm:E52_Time-Span1`|
| _DateURI_ | `uri` | `crm:E52_Time-Span1`|
| _DateURI_ | `uri` | `crm:E49_Time_Appellation1`|
| _Dated_ | `rdfs:label` | `crm:E49_Time_Appellation1`|
| _Department_ | `rdfs:label` | `crm:E55_Type4`|
| _Department_ | `rdfs:label` | `crm:E55_Type5`|
| _DepartmentURI_ | `uri` | `crm:E55_Type5`|
| _DepartmentURI_ | `uri` | `crm:E55_Type4`|
| _Description_ | `rdfs:label` | `crm:E18_Physical_Thing1`|
| _Description_ | `rdfs:label` | `crm:E18_Physical_Thing1`|
| _DescriptionURI_ | `uri` | `crm:E18_Physical_Thing1`|
| _DescriptionURI_ | `uri` | `crm:E18_Physical_Thing1`|
| _DimensionURI_ | `uri` | `crm:E54_Dimension1`|
| _DimensionURI_ | `uri` | `crm:E54_Dimension1`|
| _Dimensions_ | `crm:P3_has_note` | `crm:E54_Dimension1`|
| _Dimensions_ | `crm:P3_has_note` | `crm:E54_Dimension1`|
| _Display Name_ | `rdfs:label` | `crm:E82_Actor_Appellation2`|
| _Display Name_ | `rdfs:label` | `crm:E82_Actor_Appellation2`|
| _DisplayDate_ | `crm:P62i_is_depicted_by` | `crm:E52_Time-Span1`|
| _DisplayNameURI_ | `uri` | `crm:E82_Actor_Appellation2`|
| _DisplayNameURI_ | `uri` | `crm:E82_Actor_Appellation1`|
| _DisplayNameURI_ | `uri` | `crm:E82_Actor_Appellation2`|
| _EndDate_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _FirstName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _LastName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _Media_ | `rdfs:label` | `crm:E55_Type4`|
| _MediaURI_ | `uri` | `crm:E55_Type4`|
| _Medium_ | `crm:P3_has_note` | `crm:E55_Type3`|
| _Medium_ | `crm:P3_has_note` | `crm:E55_Type3`|
| _MediumURI_ | `uri` | `crm:E55_Type3`|
| _MediumURI_ | `uri` | `crm:E55_Type3`|
| _MiddleName_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _NameTitle_ | `crm:P102_has_title` | `crm:E82_Actor_Appellation1`|
| _Object Number_ | `rdfs:label` | `crm:E42_Identifier1`|
| _Object Number_ | `rdfs:label` | `crm:E42_Identifier1`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectNumberURI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _PrimaryTitle_ | `rdfs:label` | `crm:E35_Title1`|
| _PrimaryTitleTranslationTypeURI_ | `uri` | `crm:E55_Type6`|
| _PrimaryTitleTranslationTypeURI_ | `uri` | `crm:E55_Type6`|
| _PrimaryTitleTransltionType_ | `rdfs:label` | `crm:E55_Type6`|
| _PrimaryTitleTransltionType_ | `rdfs:label` | `crm:E55_Type6`|
| _PrimaryTitleType_ | `rdfs:label` | `crm:E55_Type2`|
| _PrimaryTitleTypeURI_ | `uri` | `crm:E55_Type2`|
| _PrimaryTitleURI_ | `uri` | `crm:E35_Title1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _Suffix_ | `crm:P106_is_composed_of` | `crm:E82_Actor_Appellation1`|
| _Title_ | `rdfs:label` | `crm:E35_Title1`|
| _TitleURI_ | `uri` | `crm:E35_Title1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E12_Production1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E22_Man-Made_Object1` | `crm:P108i_was_produced_by` | `crm:E12_Production1`|
| `crm:E22_Man-Made_Object1` | `crm:P62_depicts` | `crm:E18_Physical_Thing1`|
| `crm:E22_Man-Made_Object1` | `crm:P102_has_title` | `crm:E35_Title1`|
| `crm:E22_Man-Made_Object1` | `crm:P51_has_former_or_current_owner` | `crm:E39_Actor1`|
| `crm:E22_Man-Made_Object1` | `crm:P94i_was_created_by` | `crm:E39_Actor2`|
| `crm:E22_Man-Made_Object1` | `crm:P48_has_preferred_identifier` | `crm:E42_Identifier1`|
| `crm:E22_Man-Made_Object1` | `crm:P43_has_dimension` | `crm:E54_Dimension1`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type1`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type3`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type4`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type5`|
| `crm:E35_Title1` | `crm:P2_has_type` | `crm:E55_Type2`|
| `crm:E35_Title1` | `crm:P2_has_type` | `crm:E55_Type6`|
| `crm:E39_Actor1` | `crm:P1_is_identified_by` | `crm:E82_Actor_Appellation1`|
| `crm:E39_Actor2` | `crm:P1_is_identified_by` | `crm:E82_Actor_Appellation2`|
