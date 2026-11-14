# FOSSEE-OsdagBridge-Testing-2026
Functional Testing and Structural Verification of OsdagBridge

This repository records the November 2026 FOSSEE screening tests for the OsdagBridge short-span steel girder bridge module. The baseline highway bridge has a 25 m span and a 7.5 m carriageway. The test cases cover geometry limits, material properties, repeated design runs, exported results and the 3D model.

**Status: draft.** Start with the [updated test log](FOSSEE_OsdagBridge_Test_Log_Updated.xlsx) for case IDs and observed outcomes. The [draft testing report](FOSSEE_OsdagBridge_Functional_Testing_Report_DRAFT.pdf) explains the evidence, including the partial results. Numerical comparison across all three consecutive runs and independent structural verification remain open.

## Saved inputs

Open an `.osi` file in OsdagBridge to inspect the saved configuration. The eight distinct inputs are grouped here by test.

| Test | Saved configurations |
| --- | --- |
| Steel grade selection | [E250C](TC02_E250C.osi), [E275A](TC02_E275A.osi), [E350A](TC02_E350A.osi) |
| Custom materials | [Steel, Fy 250 MPa and Fu 410 MPa](custom_steel_250_410.osi), [custom concrete](TC09_Custom_Concrete.osi) |
| Carriageway width | [23.6 m](TC16_Width_23.6m.osi), [4.25 m](TC17_Width_4.25m.osi) |
| CAD visibility | [Pune 3D test](TC21_Pune_3D_CAD_Test.osi) |

## Results and evidence

| Test | Evidence |
| --- | --- |
| TC-04, results export | [Run 3 workbook](TC04_Results_Run3.xlsx) |
| TC-07, design report generation | [OsdagBridge-generated design report](TC07_Design_Report.pdf) |
| TC-08, custom steel | [Material settings](Custom_Steel_Settings.png), [exported sheet](Custom_Steel_Export.png), [original workbook](TC08_Custom_Steel.xlsx) |
| TC-09, custom concrete | [Material settings](Custom_Concrete_Settings.png), [exported sheet](Custom_Concrete_Export.png), [original workbook](TC09_Custom_Concrete.xlsx) |
| TC-10 to TC-13, span limits | [Lower-bound rejection](Span_Lower_Rejection.png), [upper-bound rejection](Span_Upper_Rejection.png), [minimum span](Span_Minimum.png) and [maximum span](Span_Maximum.png) model views |
| TC-14 to TC-17, carriageway width | [Lower-bound rejection](Width_Lower_Rejection.png), [upper-bound warning](Width_Upper_Warning.png), [maximum](Width_Maximum.png) and [minimum](Width_Minimum.png) model views |
| TC-21 to TC-23, CAD visibility | Isolated [girders](CAD_Girders.png), [deck](CAD_Deck.png), [bracing](CAD_Bracing.png) and [barriers](CAD_Barriers.png) |

The draft records differences between the units shown in the material dialogs and the exported sheets. The upstream issue for steel elastic and shear modulus labels is [OsdagBridge #82](https://github.com/Nidhikhare12/OsdagBridge/issues/82). The draft also references [OsdagBridge #66](https://github.com/Nidhikhare12/OsdagBridge/issues/66) for girder dimensions in the generated PDF. Reproducing the PDF comparison with the same saved input remains open.
