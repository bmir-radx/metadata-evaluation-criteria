---
title: Metadata Evaluation Criteria
has_toc: true
---

# Metadata Evaluation Criteria

## Completeness
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">

### Overall Completeness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: The percentage of all fields that contain a non-empty value.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A metadata template with 10 fields, where 3 fields are empty, would have an overall completeness of 70% (7/10).

### Required Fields Completeness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: The percentage of required fields that contain a non-empty value.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A metadata template with 10 fields, 4 of which are required. If all 4 required fields are filled, the required fields completeness is 100% (4/4).


### Recommended Fields Completeness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: The percentage of recommended fields that contain a non-empty value.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A metadata template with 10 fields, 4 of which are recommended. If 3 recommended fields are filled, the recommended fields completeness is 75% (3/4).


### Optional Fields Completeness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: The percentage of optional fields that contain a non-empty value.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A metadata template with 10 fields, 2 of which are optional. If 1 optional field is filled, the optional fields completeness is 50% (1/2).


## Consistency
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">

### Associated Metadata Consistency

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Metadata fields that are logically related should be internally consistent.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: In the RADx Data Hub, the fields `Estimated Cohort Size` and `Cohort Size Range` should reflect the same cohort size. Similarly, `Full Name` should be consistent with `Given Name` and `Family Name`.


### Overlapped Metadata Consistency

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Metadata fields containing overlapping information should be aligned in meaning and value.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: In the RADx Data Hub, if the `Acknowledgment Statement` mentions a supporting NIH institution or center, it should align with the `NIH Institute/Center` field in the same study metadata instance.


### Cross-instance Metadata Consistency

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Common fields shared between study-level and data file-level metadata should have consistent values.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: If both the study-level and data file-level metadata include the `Study Name`, the value should be identical in both instances.


## Accuracy
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">

### External Reference Accuracy

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Validates that metadata fields referencing external systems (e.g., NIH RePORTER, funding sources) accurately reflect the information found in those authoritative sources.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: Cross-checked against NIH RePORTER using provided `NIH Grant or Contract Number(s)` information to ensure alignment of `NIH Institute/Center` and `Funding Opportunity Announcement (FOA) Number` metadata.


### Linked Resource Accuracy

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Ensures that URLs provided in metadata resolve to the correct and intended external resource, accurately representing the associated study or content.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: Verified that `ClinicalTrials.gov URLs` point to the corresponding study.


## Validity
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">


### File Format Validity

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Validates that the uploaded file is a well-formed and syntactically correct JSON file.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A file that includes an unexpected trailing comma or unmatched brackets will fail this check.


### Schema Validity

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Verifies that the JSON structure aligns with the defined CEDAR template.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A JSON file missing required fields like `fileName` or `fileType` will not conform to the schema.


### Value Constraint Validity

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Ensures that metadata conforms to the constraints specified in the CEDAR template, such as allowed controlled terms, formats, data types, and required patterns.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A field like `Subjects`, constrained to controlled terms from an ontology (e.g., MeSH), must use valid concept labels such as *COVID-19*. Free-text variations like *covid-19* are not accepted, as they do not match the standardized ontology term.


## Accessibility
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">


### Link Accessibility

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Evaluates whether all link-type fields are accessible and resolve to valid, publicly reachable web pages.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: Fields such as `Study Website URL`, `ClinicalTrials.gov URL`, `Publication URLs`, `Funding Opportunity Announcement (FOA) URL`, and `RAPIDS Link` are tested to ensure they are not broken and point to the intended resources.


## Uniqueness
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">


### Metadata Instance Uniqueness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Ensures that each metadata instance is uniquely identifiable and not duplicated within the dataset or metadata repository.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: Two instances with the same combination of `Study ID`, `Data File Name`, and `Version` would violate uniqueness. Each metadata instance should have a distinct identifier or a unique combination of key fields to prevent duplication.


## Linguistic Quality
<hr style="border: none; border-top: 1px solid #ccc; margin-top: 0.2em; margin-bottom: 1.5em;">


### Text Formatting Consistency

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Evaluates the consistency and cleanliness of text formatting.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: The presence of unnecessary spaces, inconsistent use of line breaks, or other visual irregularities that affect readability.


### Grammatical Correctness

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Ensures that text adheres to proper grammatical rules, improving clarity, professionalism, and readability.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A sentence like `"The study include data from 2020"` should be corrected to `"The study includes data from 2020"`.


### Spelling Accuracy

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Detects and corrects spelling errors to maintain lexical precision and avoid ambiguity.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A value like `"diabtes"` should be corrected to `"diabetes"`.


### Punctuation Accuracy

<span style="background-color: #cce4f6; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #003c66;">Description</span>: Identifies missing or incorrect punctuation marks to ensure sentence completeness and proper structure.

<span style="background-color: #bde5c8; padding: 2px 6px; border-radius: 4px; font-weight: bold; color: #1e4620;">Example</span>: A sentence like `"This study investigates heart disease"` may require a period: `"This study investigates heart disease."`
