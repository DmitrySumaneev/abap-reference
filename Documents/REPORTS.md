# Reports

## Purpose

This section describes features of reports from ABAP perspective.

## Disclaimer

In this section the terms *"Report"* and *"Program"* are used as synonims.

## Contents

- [How to](#how-to)
  - [How to get the name of the current report](#how-to-get-the-name-of-the-current-report)
  - [How to get a list of report variants](#how-to-get-a-list-of-reports-variants)
  - [How to call a report from another report](#how-to-call-a-report-from-another-report)
  - [How to launch editor for a program](#how-to-launch-editor-for-a-program)

## How to

### How to get the name of the current report

Use global variable *sy-cprog*:

```ABAP
    report_name = sy-cprog.
```

### How to get a list of report's variants

Use:

```ABAP
    CALL FUNCTION 'RS_VARIANT_CATALOG'.
```

### How to call a report from another report

Use:

```ABAP
    SUBMIT some_report
      WITH parameter_1 = value_1
      WITH select_options_1 IN range_1.
```

If you want to return to the calling program after the called program finishes execution, use the addition *AND RETURN*:

```ABAP
    SUBMIT some_other_report
      WITH parameter_1 = value_1
      WITH select_options_1 IN range_1
      AND RETURN.
```

### How to launch editor for a program

Use statement:

```ABAP
    EDITOR-CALL FOR REPORT prog [DISPLAY-MODE]
```

With addition *DISPLAY-MODE* the editor launches in display mode.
