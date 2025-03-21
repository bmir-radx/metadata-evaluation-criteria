---
title: Metadata Evaluation Criteria
has_toc: true
---

# Metadata Quality Criteria

## Completeness

### Overall Completeness
- **Description**: Percentage of fields with a non-empty value.
- **Notes/Examples**: Calculated for both Study Metadata and Data File Metadata. For instance, a metadata template with a total of 10 fields, where 3 fields have empty values, would have an overall completeness value of 70%.

### Completeness of Required Fields
- **Description**: Percentage of required fields with a non-empty value.
- **Notes/Examples**: The calculation is similar to Overall Completeness but applies exclusively to required fields.

### Completeness of Recommended Fields
- **Description**: Percentage of recommended fields with a non-empty value.
- **Notes/Examples**: The calculation is similar to Overall Completeness but applies exclusively to recommended fields.

### Completeness of Optional Fields
- **Description**: Percentage of optional fields with a non-empty value.
- **Notes/Examples**: The calculation is similar to Overall Completeness but applies exclusively to optional fields.

## Consistency

### Associated Metadata Consistency
- **Description**: Metadata associated with each other should be internally consistent.
- **Notes/Examples**: For example, in the RADx Data Hub, the fields Estimated Cohort Size and Cohort Size Range should align, reflecting the same cohort size. Similarly, Full Name should be consistent with Given Name and Family Name.
