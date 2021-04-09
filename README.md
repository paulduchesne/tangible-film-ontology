# Tangible Film Ontology
##### v0.1 // 2021-04-10 // Paul Duchesne

This ontology was created for film archives with the intention of focusing only on information which can be derived from primary film sources,
ignoring the fact that film institutions often preserve large collections of related documentation.

This concentration on verifiable physical characteristics would assist with interoperability, by favouring reasoning and inference over interpretation.

##### DATA MODEL

#### Work

A discrete instance of artistic expression.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Work|
| tfo:workType  | Type of work as defined by the FIAF Cataloguing Manual (controlled vocabulary from FIAF). | tfo:Monographic |
| tfo:hasVariant | Variant of work. | http://example_archive.org/variant/8589 |
| tfo:hasManifestation | Manifestation of work or variant. | http://example_archive.org/manifestation/2439 |

#### Variant
An altered instance of a work.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:Variant|
| tfo:variantType  | Type of variant as defined by the FIAF Cataloguing Manual (controlled vocabulary from FIAF). | tfo:Subtitled |
| tfo:hasManifestation | Manifestation of work or variant.| http://example_archive.org/manifestaion/5436 |

#### Manifestation
A uniform state in which a work or variant is available.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Manifestation|
|tfo:hasImageStream|An image stream within a manifestation.| _:blankNode |
|tfo:hasAudioStream|An audio stream within a manifestation. | _:blankNode |
|tfo:hasSubtitleStream|A subtitle stream within a manifestation.| _:blankNode |
|tfo:hasTitle| Title featured in manifestation.| _:blankNode |
|tfo:hasCredit| Credit featured in manifestation.| _:blankNode |
|tfo:hasEvent| Event pertaining to manifestation. | _:blankNode |
| tfo:hasItem | Item of manifestation. | http://example_archive.org/item/1856 |

#### Image Stream
A track of visual data.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:ImageStream|
| tfo:hasPolarity | Polarity of image stream (Positive or Negative). | tfo:Positive|
| tfo:hasColour | Colour of image stream (Colour or Black And White). | tfo:BlackAndWhite|
| tfo:hasRatio | Aspect ratio of an image stream, represented as a ratio to 1. | "1.37"^^xsd:float|
| tfo:hasFrame | Frame of an image stream. | http://example_archive.org/frame/5171 |

#### Polarity Type
Polarity of image stream.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:PolarityType|

#### Colour Type
Colour of image stream.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:ColourType|

#### Frame
A single image from an image stream. 
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Frame|

#### Audio Stream
A track of auditory data.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:AudioStream|
| tfo:hasLanguage | Language of title or audio/subtitle stream (controlled vocabulary from ISO 639-1). | tfo:French |
| tfo:hasChannels | Number of audio channels present in stream. | "1"^^xsd:integer |

#### Subtitle Stream
A track of text data.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:SubtitleStream|
| tfo:hasLanguage | Language of title or audio/subtitle stream (controlled vocabulary from ISO 639-1). | tfo:English |
| tfo:subtitleVisibility | Ability to invoke or suppress subtitle stream (Optional or Mandatory). | tfo:Optional |

#### Subtitle Visibility Type
Visibility of subtitle stream.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:SubtitleVisibilityType|

#### Title
A name by which the manifestation is identified.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Title|
| tfo:hasTitleType | Type of title (controlled vocabulary of Proper or Devised).| tfo:Proper |
| tfo:hasLanguage | Language of title or audio/subtitle stream (controlled vocabulary from ISO 639-1). | tfo:French |
| tfo:hasTitleString | Literal string of the title. | "LE TEMPESTAIRE" |

#### Credit
A recognised contribution by an agent to a manifestation.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:Credit|
| tfo:hasCreditType | Type of credit as defined by the FIAF Glossary of Filmographic Terms (controlled vocabulary from FIAF). | tfo:Director|
| tfo:hasCreditString | Literal string of the credit. | "Un film de JEAN EPSTEIN"|
| tfo:hasAgent | Agent referenced by the credit, or involved in event.| http://example_archive.org/agent/3791 |

#### Event
An "event" as an action related to the creation, acquisition or modification of a "manifestation" or "item".
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Event|
| tfo:eventType | Type of event (vocabulary to be decided). | tfo:Printed|
| tfo:eventPlace | Place of event (vocabulary to be decided). | tfo:Chalon-sur-Saône, France |
| tfo:eventTime | Time of event.| "1949-04-20"^^xsd:date |
| tfo:hasAgent | Agent referenced by the credit, or involved in event. | http://example_archive.org/agent/7722 |

#### Agent
An action related to the creation, acquisition or modification of a manifestion or item.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Agent|
| tfo:agentType| Controlled vocabulary (Person or Organisation) | tfo:Person|
| tfo:firstName| First name of person. | "Jean"^^xsd:string|
| tfo:lastName| Last name of person. | "Epstein"^^xsd:string|
| tfo:organisationName| Name of organisation. | "Kodak"^^xsd:string|

#### Item
A specific physical instance of a manifestation.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class.| tfo:Item|
| tfo:hasObject | Object of item. | http://example_archive.org/object/7723 |

#### Object
A discrete physical component of a item.
| Property | Description | Example |
| ---- | ---- | ---- |
| rdf:type | An instance of this class. | tfo:Object|
|tfo:hasWidth| Width of object | "35mm"^^xsd:string |
|tfo:hasLength| Length of object | "1300m"^^xsd:string |


