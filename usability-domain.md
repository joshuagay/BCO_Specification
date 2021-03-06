_This document is part of the [BioCompute Object specification](bco-specification.md)_

## 2.2 Usability Domain "usability_domain"

This section defines the fields of the `usability_domain` part of the [BCO](bco-domains.md) structure.

This field provides a space for the author to define the usability domain of the BCO. It is an array of free text values that can accept template language to indicate valeus from the [external_references](https://github.com/biocompute-objects/BCO_Specification/blob/master/external-references.md). This field is to aid in search-ability and provide a specific **scientific use case** and a description of the function of the object. The usability domain along with keywords can help determine when and how the BCO can be used. It is recomended that a novel use of the BCO could result in the creation of a new entry with a new usability domain. The template takes the form of:
* `(SNP)[SO:0000694]` 

where ($term) and [$identifier] are an entry in the `external_references` section.


```json
    "usability_domain": [

        "Identify baseline single nucleotide polymorphisms (SNPs)[SO:0000694], (insertions)[SO:0000667], and (deletions)[SO:0000045] that correlate with reduced (ledipasvir)[pubchem.compound:67505836] antiviral drug efficacy in (Hepatitis C virus subtype 1)[taxonomy:31646]", 

        "Identify treatment emergent amino acid (substitutions)[SO:1000002] that correlate with antiviral drug treatment failure", 

        "Determine whether the treatment emergent amino acid (substitutions)[SO:1000002] identified correlate with treatment failure involving other drugs against the same virus", 

        "GitHub CWL example: https://github.com/mr-c/hive-cwl-examples/blob/master/workflow/hive-viral-mutation-detection.cwl#L20"]
]
```
