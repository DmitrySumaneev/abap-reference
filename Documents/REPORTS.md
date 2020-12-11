# Reports

## Purpose

This section describes features of working with the reports from ABAP perspective.

## Disclaimer

In this section the terms *"Report"* and *"Program"* are used as synonims.

## Contents

- [How to](#how-to)
  - [How to get a list of report variants](#how-to-get-a-list-of-report-variants)

## How to

### How to get a list of report variants

Use:

```ABAP
    CALL FUNCTION 'RS_VARIANT_CATALOG'.
```

### How to call a report from another report

Use:

```ABAP
    SUBMIT report
      WITH parameter_1 = value_1
      WITH select_options_1 IN range_1.
```

If you want to return to the calling program after the called program finishes execution, use the addition *AND RETURN*:

```ABAP
    SUBMIT report
      WITH parameter_1 = value_1
      WITH select_options_1 IN range_1
      AND RETURN.
```
