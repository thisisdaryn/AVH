# AVH: Acute Viral Hepatitis Case Reporting (in DHIS2)

2026-10-06


This DHIS2 event program aims to support case reporting and surveillance
of acute viral hepatitis.

It is designed to cover the full life cycle of a case from initial
notification through to final classification, supporting data entry at
each stage: clinical assessment, specimen collection, exposure and
risk-factor investigation, hospitalization and outcome, and
disease-specific final classification.

It is intended to be compliant with all available WHO surveillance
standards for viral hepatitis and to facilitate reporting compliant with
the reporting requirements for each hepatitis type.

# Background

Five known hepatitis viruses - A, B, C, D, and E (HAV, HBV, HCV, HDV and
HEV) are collectively responsible for an estimated 1.46 million deaths
per year globally (World Health Organization 2016). The acute illnesses
caused by these viruses are clinically indistinguishable at the point of
first contact.

## Source documents

This document and the AVH Event program itself are based on several
source documents. (See references section for more detailed
information.)

(World Health Organization 2016) is the main guiding document for
surveillance of viral hepatitis. (World Health Organization 2018a) and
(World Health Organization 2018b) are surveillance standards for
Hepatitis A and Hepatitis B respectively (and can be considered to be
summaries of relevant information from (World Health Organization
2016)).

The data capture form provided by the event program is largely intended
to replicate the template reporting form provided in (World Health
Organization 2019).

Some language used in this document and in the event program is taken
verbatim from these source documents.

## The hepatitis viruses

**Hepatitis A (HAV)** is transmitted through the fecal-oral route,
including through personal contact, water, and food. A serological assay
(IgM anti-HAV) is available to diagnose recent infection. There is a
vaccine available. WHO standards allow for case confirmation via
laboratory confirmation or an epidemiological link to a laboratory
confirmed case.

**Hepatitis B (HBV)** is transmitted through exposure to blood and body
fluids, including perinatal, percutaneous and sexual. Hepatitis B
infections among children often lead to chronic disease. Acute Hepatitis
B among adults is usually self-limiting. A serological assay (IgM
anti-HBc) is available to diagnose recent infection. There is a vaccine
available and recommended for all newborns. WHO standards allow only for
case classification via laboratory confirmation.

**Hepatitis C (HCV)** is mostly transmitted via exposure to infected
blood. Chronic infections can lead to hepatocellular carcinoma (HCC) and
cirrhosis. New HCV infections uncommonly cause acute hepatitis.
Serological assays for HCV (total anti-HCV) does not distinguish between
new, chronic, and resolved. Distinguishing resolved infection from
chronic infection requires either HCV core antigen testing or nucleic
acid testing (NAT) to detect HCV RNA. No vaccine is available yet. WHO
standards allow only for case classification via laboratory
confirmation.

**Hepatitis D (HDV)** is a bloodborne, incomplete virus that needs HBV
to replicate. Infection can be prevented through Hepatitis B
vaccination. (This event program offers no components specific to
Hepatitis D currently.)

**Hepatitis E (HEV)** is transmitted through the fecal-oral route,
mostly through fecally contaminated water. Hepatitis E often occurs as
large waterborne outbreaks. Person-to-person transmission is uncommon. A
serological test (IgM anti-HEV) is available to diagnose recent
infection. The WHO has not recommended a vaccine for widespread use. WHO
standards allow for case confirmation via laboratory confirmation or an
epidemiological link to a laboratory confirmed case.

## Laboratory testing for hepatitis viruses

The table below lists some of the available laboratory tests for
detecting hepatitis viruses.

<div id="tbl-hep-labs">

Table 1: Laboratory tests for hepatitis viruses

<div class="cell-output-display">

| Test | Description |
|:---|:---|
| Alanine aminotransferase (ALT) | Tests for elevated levels of ALT in blood which would indicate liver damage. The results are given in IU/L (international units per liter). |
| Anti-HAV IgM | Detects IgM antibodies to the Hepatitis A virus |
| Anti-HBc IgM | Detects IgM antibodies against Hepatitis B core antigen, a component of the Hep B virus |
| HBsAg | Detects the presence of the Hepatitis B surface antigen |
| Anti-HCV | Detects any antibodies against the Hepatitis C virus |
| HCV RNA | Detects the RNA of the Hepatitis C virus (to confirm an active infection) |
| HDV testing | Detects antibodies to the hepatitis D virus |
| Anti-HEV IgM | Detects IgM antibodies against the Hepatitis C virus |

</div>

</div>

## Laboratory confirmation criteria

WHO guidance specifies certain allowable biomarker profiles appropriate
for laboratory-confirmed case classifications for each hepatitis virus.

<div id="tbl-hep-labconfprofiles">

Table 2: WHO criteria for laboratory confirmation of acute hepatitis

<div class="cell-output-display">

| Virus | Lab-confirmation criteria for Acute Hepatitis |
|:---|:---|
| HAV | Someone who meets the presumptive case definition and is positive for IgM anti-HAV |
| HBV | ELISA testing for immunoglobulin M antibodies to core antigen of hepatitis B (anti-HBC IgM) |
| HCV | 1\. HCV-RNA positive and anti-HCV negative or 2. HCV-RNA positive in persons previously negative or 3. Occurrence with clinical acute hepatitis with a test positive for anti-HCV after exclusion of hepatitis A, B, and E. |
| HDV | Someone who meets the presumptive case definition and is positive for IgM anti-HEV |

</div>

</div>

# Installing the Event Program

Successful installation of the AVH event program should involve the
following steps:

1.  Importing the event program metadata
    (`AVH_metadata_dependencies_complete_program.json`) via the
    `Import/Export` app
2.  Making the event program available for data entry at specified
    organisation units (using the `Maintenance` or `Metadata Management`
    apps)
3.  Creating users if necessary
4.  Adding admin users to the `AVH Level 1` user group
5.  Adding data entry users to the `AVH Level 2` user group
6.  Assigning the `AVH Capture User` (or a comparable role) to data
    entry users if necessary

# AVH Technical details

## Data Elements

The program contains **103 data elements** organised into **12
sections**. The table below lists all fields in section order with
relevant details.

Value types are: `DATE`, `TEXT` (free text or option set), `BOOLEAN`
(Yes/No checkbox), `INTEGER_ZERO_OR_POSITIVE` (non-negative whole
number), `COORDINATE` (latitude/longitude), `MULTI_TEXT` (multi-select
option set).

<div id="tbl-data-elements">

Table 3: All AVH event program data elements by section

<div class="cell-output-display">

<table class="table table-striped table-hover table-condensed cell"
data-quarto-postprocess="true"
style="font-size: 11px; margin-left: auto; margin-right: auto;">
<thead>
<tr>
<th data-quarto-table-cell-role="th"
style="text-align: left; font-weight: bold;">Form name</th>
<th data-quarto-table-cell-role="th"
style="text-align: left; font-weight: bold;">code</th>
<th data-quarto-table-cell-role="th"
style="text-align: left; font-weight: bold;">id</th>
<th data-quarto-table-cell-role="th"
style="text-align: left; font-weight: bold;">valueType</th>
<th data-quarto-table-cell-role="th"
style="text-align: left; font-weight: bold;">Option Set</th>
</tr>
</thead>
<tbody>
<tr data-grouplength="14">
<td colspan="5" style="border-bottom: 1px solid"><strong>Patient
Information</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Unique Identifier</td>
<td style="text-align: left;">AVH_RECORDID</td>
<td style="text-align: left;">W2pkAFEn3z5</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">First Name</td>
<td style="text-align: left;">AVH_FIRSTNAME</td>
<td style="text-align: left;">BS9UYJQTFjm</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Last Name</td>
<td style="text-align: left;">AVH_LASTNAME</td>
<td style="text-align: left;">dLEG62Hkd9G</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Birth</td>
<td style="text-align: left;">AVH_DOB</td>
<td style="text-align: left;">KpLMcNfAQLK</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Age in Years</td>
<td style="text-align: left;">AVH_AGEYEARS</td>
<td style="text-align: left;">iQPtDu7W7ea</td>
<td style="text-align: left;">INTEGER_ZERO_OR_POSITIVE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Age in Months</td>
<td style="text-align: left;">AVH_AGEMONTHS</td>
<td style="text-align: left;">w4e4pxskC1I</td>
<td style="text-align: left;">INTEGER</td>
<td style="text-align: left;">AVH - Age in Months</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Sex</td>
<td style="text-align: left;">AVH_SEX</td>
<td style="text-align: left;">Qg84iqh4gVJ</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Sex</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Phone Number</td>
<td style="text-align: left;">AVH_PHONE</td>
<td style="text-align: left;">qGFq562dfOB</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Address 1</td>
<td style="text-align: left;">AVH_ADDRESS1</td>
<td style="text-align: left;">JTBJahe84S5</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Address 2</td>
<td style="text-align: left;">AVH_ADDRESS2</td>
<td style="text-align: left;">tx57Y3c5wnR</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Address 3</td>
<td style="text-align: left;">AVH_ADDRESS3</td>
<td style="text-align: left;">j77p3kZZl4A</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Address 4</td>
<td style="text-align: left;">AVH_ADDRESS4</td>
<td style="text-align: left;">VZprkYSgy3c</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Location</td>
<td style="text-align: left;">AVH_LOCATION</td>
<td style="text-align: left;">oobQmzvr3e9</td>
<td style="text-align: left;">COORDINATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Visit</td>
<td style="text-align: left;">AVH_DATEOFVISIT</td>
<td style="text-align: left;">bh4qlL9qcgM</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr data-grouplength="11">
<td colspan="5" style="border-bottom: 1px solid"><strong>Clinical
Presentation</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Onset</td>
<td style="text-align: left;">AVH_DATEONSET</td>
<td style="text-align: left;">RU8VVQmxBe8</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Fever</td>
<td style="text-align: left;">AVH_SXFEVER</td>
<td style="text-align: left;">GtQAuzSsJim</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Malaise</td>
<td style="text-align: left;">AVH_SXMALAISE</td>
<td style="text-align: left;">zJ1atsnBYLM</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Fatigue</td>
<td style="text-align: left;">AVH_SXFATIGUE</td>
<td style="text-align: left;">YVkQfsGQONv</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Anorexia</td>
<td style="text-align: left;">AVH_SXANOREXIA</td>
<td style="text-align: left;">bcpEN2XeDA4</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Nausea</td>
<td style="text-align: left;">AVH_SXNAUSEA</td>
<td style="text-align: left;">Sa5W3X4gXBo</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Jaundice</td>
<td style="text-align: left;">AVH_SXJAUNDICE</td>
<td style="text-align: left;">hDiZDQHJMu8</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Dark Urine</td>
<td style="text-align: left;">AVH_SXDARKURINE</td>
<td style="text-align: left;">JC5kV3ECqWp</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Right Upper Quadrant Tenderness</td>
<td style="text-align: left;">AVH_SXRUQPAIN</td>
<td style="text-align: left;">Tsprvu5Ifij</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Encephalopathy</td>
<td style="text-align: left;">AVH_ENCEPHALOPATHY</td>
<td style="text-align: left;">DAdn1Ay5XL8</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Encephalopathy Grade</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Acute Liver Failure?</td>
<td style="text-align: left;">AVH_ACUTELIVERFAIL</td>
<td style="text-align: left;">tWy2591AIVV</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr data-grouplength="5">
<td colspan="5" style="border-bottom: 1px solid"><strong>Hospitalization
and Outcome</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hospitalized?</td>
<td style="text-align: left;">AVH_HOSPITALIZED</td>
<td style="text-align: left;">wAvuQg2kvAS</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Hospitalization</td>
<td style="text-align: left;">AVH_HOSPDATE</td>
<td style="text-align: left;">uquhXz3G0aQ</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Discharge Date</td>
<td style="text-align: left;">AVH_DISCHARGEDATE</td>
<td style="text-align: left;">CWdnrJi7sC4</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Outcome</td>
<td style="text-align: left;">AVH_OUTCOME</td>
<td style="text-align: left;">JaJAfo16hD8</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Outcome</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Death</td>
<td style="text-align: left;">AVH_DATEDEATH</td>
<td style="text-align: left;">A1EEpDJjym6</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr data-grouplength="20">
<td colspan="5" style="border-bottom: 1px solid"><strong>Laboratory and
Biomarkers</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Specimen Collected?</td>
<td style="text-align: left;">AVH_SPECIMEN</td>
<td style="text-align: left;">iNIb6zLKQbf</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Specimen Type</td>
<td style="text-align: left;">AVH_SPECTYPE</td>
<td style="text-align: left;">DuvW4yrW81A</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Specimen Type</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Specimen Collection</td>
<td style="text-align: left;">AVH_DATESPEC</td>
<td style="text-align: left;">PeX9PcWb8pm</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date Specimen Sent to Laboratory</td>
<td style="text-align: left;">AVH_DATESPECSENT</td>
<td style="text-align: left;">DSqXxkMM9VT</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date Specimen Received at Laboratory</td>
<td style="text-align: left;">AVH_DATESPECRECV</td>
<td style="text-align: left;">KR69yz8TmeL</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">ALT Result (IU/L)</td>
<td style="text-align: left;">AVH_ALTRESULT</td>
<td style="text-align: left;">ZhYKYcwIBQx</td>
<td style="text-align: left;">NUMBER</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Anti-HAV IgM</td>
<td style="text-align: left;">AVH_ANTIHAV_IGM 13950-1</td>
<td style="text-align: left;">xO51DTjBlUH</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">IgM Anti-HBc</td>
<td style="text-align: left;">AVH_ANTIHBC_IGM 24113-3</td>
<td style="text-align: left;">ULru2p17fr4</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Total Anti-HBc Result</td>
<td style="text-align: left;">AVH_ANTIHBC_TOTAL</td>
<td style="text-align: left;">ulFnwZqvr4M</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">HBsAg</td>
<td style="text-align: left;">AVH_HBSAG 5196-1</td>
<td style="text-align: left;">AFJWpSEPTFC</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Anti-HCV</td>
<td style="text-align: left;">AVH_ANTIHCV 13955-0</td>
<td style="text-align: left;">xEJHwBVJvwS</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Previous Negative Anti-HCV test</td>
<td style="text-align: left;">AVH_PREV_NEG_ANTIHCV</td>
<td style="text-align: left;">D4GmBrVfpZr</td>
<td style="text-align: left;">BOOLEAN</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of negative Anti-HCV test</td>
<td style="text-align: left;">AVH_DATE_ANTIHCV_NEG</td>
<td style="text-align: left;">Y616snuFKXW</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">HCV RNA presence</td>
<td style="text-align: left;">AVH_HCVRNA 11259-9</td>
<td style="text-align: left;">I8WSlmnVErU</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">HCV RNA viral load</td>
<td style="text-align: left;">AVH_HCVRNA 11011-4</td>
<td style="text-align: left;">pioHuaL05Jo</td>
<td style="text-align: left;">NUMBER</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">HDV Testing</td>
<td style="text-align: left;">AVH_HDVRESULT 40727-0</td>
<td style="text-align: left;">ltaTIircdJs</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Anti-HEV IgM</td>
<td style="text-align: left;">AVH_ANTIHEV_IGM 14212-5</td>
<td style="text-align: left;">sEECvl9dq83</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Lab Result</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">HBV Genotype (if performed)</td>
<td style="text-align: left;">AVH_HBVGENOTYPE 104995-6</td>
<td style="text-align: left;">jjZK8tfphJW</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Result</td>
<td style="text-align: left;">AVH_DATERESULT</td>
<td style="text-align: left;">Ct3LBtKNdN9</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Other Laboratory Findings / Notes</td>
<td style="text-align: left;">AVH_OTHERHEP</td>
<td style="text-align: left;">plJekaACSME</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr data-grouplength="3">
<td colspan="5" style="border-bottom: 1px solid"><strong>Case Linkage
and Source of Infection</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Contact with a Laboratory-Confirmed Case of Viral
Hepatitis?</td>
<td style="text-align: left;">AVH_CONTACTCASE</td>
<td style="text-align: left;">CR74KPONu3O</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Associated Case ID</td>
<td style="text-align: left;">AVH_ASSOCCASEID</td>
<td style="text-align: left;">dwGetDCcdx1</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Source of Infection</td>
<td style="text-align: left;">AVH_SOURCE</td>
<td style="text-align: left;">LJ9YV5cC6ZK</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Source of Infection</td>
</tr>
<tr data-grouplength="5">
<td colspan="5" style="border-bottom: 1px solid"><strong>Case
Classification</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Final Case Classification</td>
<td style="text-align: left;">AVH_FINALCLASS</td>
<td style="text-align: left;">TCCHHNkxx6s</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Final Case Classification</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis A - Final Case Classification</td>
<td style="text-align: left;">AVH_HEPA_FINALCLASS</td>
<td style="text-align: left;">evgJRysqU2Q</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH Hepatitis A/E - Case
Classification</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis B - Final Case Classification</td>
<td style="text-align: left;">AVH_HEPB_FINALCLASS</td>
<td style="text-align: left;">R6HfPQBGxbx</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH Hepatitis B/C - Case
Classification</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis C - Final Case Classification</td>
<td style="text-align: left;">AVH_HEPC_FINALCLASS</td>
<td style="text-align: left;">kl1SXNZ5kUC</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH Hepatitis B/C - Case
Classification</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis E - Final Case Classification</td>
<td style="text-align: left;">AVH_HEPE_FINALCLASS</td>
<td style="text-align: left;">GHA9k0mZMi3</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH Hepatitis A/E - Case
Classification</td>
</tr>
<tr data-grouplength="3">
<td colspan="5" style="border-bottom: 1px solid"><strong>Prior Diagnosis
and Chronic Conditions</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Previously Identified with Chronic HBV
Infection?</td>
<td style="text-align: left;">AVH_PRIORHBV</td>
<td style="text-align: left;">BhIoPj6r0je</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Previously Identified with Chronic HCV
Infection?</td>
<td style="text-align: left;">AVH_PRIORHCV</td>
<td style="text-align: left;">hDStSz8rGIF</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Previous History of Other Chronic Liver
Disease?</td>
<td style="text-align: left;">AVH_PRIORCLD</td>
<td style="text-align: left;">fo9R13KL8bW</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr data-grouplength="14">
<td colspan="5" style="border-bottom: 1px solid"><strong>Vaccination
History</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Vaccinated against Hepatitis A?</td>
<td style="text-align: left;">AVH_VACC_HEPA_GIVEN</td>
<td style="text-align: left;">LLQF3jCIEwv</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Number of Hepatitis A Vaccine Doses Received</td>
<td style="text-align: left;">AVH_VACC_HEPA_DOSES</td>
<td style="text-align: left;">Kyo2XAcuVET</td>
<td style="text-align: left;">INTEGER_ZERO_OR_POSITIVE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis A Vaccine - Date of Dose 1</td>
<td style="text-align: left;">AVH_VACC_HEPA_DATE1</td>
<td style="text-align: left;">iG9Lv3g32Cg</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis A Vaccine - Date of Dose 2</td>
<td style="text-align: left;">AVH_VACC_HEPA_DATE2</td>
<td style="text-align: left;">EYqvNSzPf2v</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Vaccinated against Hepatitis B?</td>
<td style="text-align: left;">AVH_VACC_HEPB_GIVEN</td>
<td style="text-align: left;">IcNepOR6soV</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Number of Hepatitis B Vaccine Doses Received</td>
<td style="text-align: left;">AVH_VACC_HEPB_DOSES</td>
<td style="text-align: left;">t5bcuYdswxB</td>
<td style="text-align: left;">INTEGER_ZERO_OR_POSITIVE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis B Vaccine - Received Birth Dose?</td>
<td style="text-align: left;">AVH_VACC_HEPB_BIRTHDOSE</td>
<td style="text-align: left;">N3yNRpF6Ljo</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis B Vaccine - Date of Dose 1</td>
<td style="text-align: left;">AVH_VACC_HEPB_DATE1</td>
<td style="text-align: left;">sRIkeC8wLtO</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis B Vaccine - Date of Dose 2</td>
<td style="text-align: left;">AVH_VACC_HEPB_DATE2</td>
<td style="text-align: left;">pyKwKsSsb1Q</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Hepatitis B Vaccine - Date of Dose 3</td>
<td style="text-align: left;">AVH_VACC_HEPB_DATE3</td>
<td style="text-align: left;">VF155sXZoMZ</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Vaccinated with Combined Hepatitis A and B
Vaccine?</td>
<td style="text-align: left;">AVH_VACC_HEPAB_GIVEN</td>
<td style="text-align: left;">R1iOg5OPctY</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Number of Combined Hepatitis A and B Vaccine Doses
Received</td>
<td style="text-align: left;">AVH_VACC_HEPAB_DOSES</td>
<td style="text-align: left;">AlmiYI4xHG6</td>
<td style="text-align: left;">INTEGER_ZERO_OR_POSITIVE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Vaccinated against Hepatitis E?</td>
<td style="text-align: left;">AVH_VACC_HEPE_GIVEN</td>
<td style="text-align: left;">V3vZhD9ejW9</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Number of Hepatitis E Vaccine Doses Received</td>
<td style="text-align: left;">AVH_VACC_HEPE_DOSES</td>
<td style="text-align: left;">fYzaqIhDxRV</td>
<td style="text-align: left;">INTEGER_ZERO_OR_POSITIVE</td>
<td style="text-align: left;"></td>
</tr>
<tr data-grouplength="4">
<td colspan="5" style="border-bottom: 1px solid"><strong>Patient Risk
Characteristics</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Health-care Worker Exposed to Blood through Patient
Care?</td>
<td style="text-align: left;">AVH_RISK_HCW</td>
<td style="text-align: left;">eO0D6StPAhi</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Man Who Has Sex with Other Men?</td>
<td style="text-align: left;">AVH_RISK_MSM</td>
<td style="text-align: left;">yDxQ8VS8IAL</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Undergoes Haemodialysis?</td>
<td style="text-align: left;">AVH_RISK_HAEMODIALYSIS</td>
<td style="text-align: left;">rcSxnCC8p2x</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Injecting Drug Use?</td>
<td style="text-align: left;">AVH_RISK_IDU</td>
<td style="text-align: left;">h820DfQnPOM</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr data-grouplength="7">
<td colspan="5" style="border-bottom: 1px solid"><strong>Exposure
History — 2 to 6 Weeks Before Onset</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Involved in a Reported, Identified Outbreak?</td>
<td style="text-align: left;">AVH_EXP_OUTBREAK</td>
<td style="text-align: left;">Y5Mar2jiIqZ</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Contact with Patient(s) with the Same
Symptoms?</td>
<td style="text-align: left;">AVH_EXP_CONTACTSYMPTOMS</td>
<td style="text-align: left;">LublqdiVAHh</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Ate Raw, Uncooked Shellfish (e.g. Oysters)?</td>
<td style="text-align: left;">AVH_EXP_SHELLFISH</td>
<td style="text-align: left;">o8NcUY63QHt</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Ate Raw, Uncooked Pork, Boar Meat or Venison?</td>
<td style="text-align: left;">AVH_EXP_PORK</td>
<td style="text-align: left;">FT6Ce5fuMje</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Drank Water from a Well or Other Unsafe
Source?</td>
<td style="text-align: left;">AVH_EXP_WATER</td>
<td style="text-align: left;">sDGMBgYSh2P</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Child or Staff Member in a Day-care Centre?</td>
<td style="text-align: left;">AVH_EXP_DAYCARE</td>
<td style="text-align: left;">Av0DzAUguBu</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Travelled to an Area Highly Endemic for Hepatitis A
/ Hepatitis E?</td>
<td style="text-align: left;">AVH_EXP_TRAVEL</td>
<td style="text-align: left;">ffBgVVxZiJd</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr data-grouplength="10">
<td colspan="5" style="border-bottom: 1px solid"><strong>Exposure
History — 1 to 6 Months Before Onset</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Received Injections Given for Therapeutic
Purposes?</td>
<td style="text-align: left;">AVH_EXP_INJECTIONS</td>
<td style="text-align: left;">gKGnjQEo2gw</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Admitted to Hospital?</td>
<td style="text-align: left;">AVH_EXP_HOSPITALADM</td>
<td style="text-align: left;">X0NNRPJbM7Q</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Underwent a Surgical Procedure?</td>
<td style="text-align: left;">AVH_EXP_SURGERY</td>
<td style="text-align: left;">al3jKQzejVO</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Received a Blood Transfusion?</td>
<td style="text-align: left;">AVH_EXP_TRANSFUSION</td>
<td style="text-align: left;">tUuX8KMf4dj</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Received Dental Care?</td>
<td style="text-align: left;">AVH_EXP_DENTAL</td>
<td style="text-align: left;">MCArnWGhwBh</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Underwent Endoscopy?</td>
<td style="text-align: left;">AVH_EXP_ENDOSCOPY</td>
<td style="text-align: left;">Mdant8nXiWq</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Underwent Tattooing or Body Piercing?</td>
<td style="text-align: left;">AVH_EXP_TATTOO</td>
<td style="text-align: left;">ToGJ1QZwez3</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Underwent Shaving by a Barber?</td>
<td style="text-align: left;">AVH_EXP_BARBER</td>
<td style="text-align: left;">KzTOAshzb9u</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Unprotected Sex with an Occasional Partner?</td>
<td style="text-align: left;">AVH_EXP_SEX</td>
<td style="text-align: left;">gpBLzHfz3tV</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Household Contact with Someone with Hepatitis B /
C?</td>
<td style="text-align: left;">AVH_EXP_HOUSEHOLD</td>
<td style="text-align: left;">m5XwwU90P0j</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;">AVH - Yes / No / Unknown</td>
</tr>
<tr data-grouplength="4">
<td colspan="5"
style="border-bottom: 1px solid"><strong>Reporting</strong></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Reporting</td>
<td style="text-align: left;">AVH_DATEREPORT</td>
<td style="text-align: left;">bu7g1TPvYji</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Reporting Facility</td>
<td style="text-align: left;">AVH_REPFACILITY</td>
<td style="text-align: left;">CNa5fbqn1jJ</td>
<td style="text-align: left;">TEXT</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Notification to Public Health</td>
<td style="text-align: left;">AVH_DATENOTIF</td>
<td style="text-align: left;">pAOYNDeh15F</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left; padding-left: 2em;"
data-indentlevel="1">Date of Investigation</td>
<td style="text-align: left;">AVH_DATEINVESTIG</td>
<td style="text-align: left;">aNwpKAlQQfH</td>
<td style="text-align: left;">DATE</td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>

</div>

</div>

### Data Elements for laboratory test results

The data elements for include LOINC(Regenstrief Institute)
classification codes in their names/codes as well as in metadata
attributes. The table below lists all the data elements included in the
metadata JSON file along with the corresponding *Common Long Name* in
the LOINC classification database.

(Note that two of data elements in the table are not included by default
in the AVH data capture form. DHIS2 instance administrators can include
these data elements - or create others - to more accurately reflect the
laboratory tests used, if necessary.)

<div id="tbl-loinc-codes">

Table 4: Laboratory-confirmation criteria for acute hepatitis hepatitis

<div class="cell-output-display">

| Data Element | Form Name | LOINC Common Long Name | Note |
|:---|:---|:---|:---|
| AVH_ANTIHAV_IGM 13950-1 | Anti-HAV IgM | Hepatitis A virus IgM Ab \[Presence\] in Serum or Plasma by Immunoassay |  |
| AVH_ANTIHBC_IGM 24113-3 | IgM Anti-HBc | Hepatitis B virus core IgM Ab \[Presence\] in Serum or Plasma by Immunoassay |  |
| AVH_HBSAG 5196-1 | HBsAg | Hepatitis B virus surface Ag \[Presence\] in Serum or Plasma by Immunoassay |  |
| AVH_ANTIHCV 13955-0 | Anti-HCV | Hepatitis C virus Ab \[Presence\] in Serum or Plasma by Immunoassay |  |
| AVH_ANTIHCV 16128-1 | Anti-HCV | Hepatitis C virus Ab \[Presence\] in Serum | Not included in default data capture form |
| AVH_HCVRNA 11259-9 | HCV RNA presence | Hepatitis C virus RNA \[Presence\] in Serum or Plasma by NAA with probe detection |  |
| AVH_HCVRNA 11011-4 | HCV RNA viral load | Hepatitis C virus RNA \[Units/volume\] (viral load) in Serum or Plasma by NAA with probe detection |  |
| AVH_HDVRESULT 40727-0 | HDV Testing | Hepatitis D virus Ab \[Presence\] in Serum by Immunoassay |  |
| AVH_ANTIHEV_IGM 14212-5 | Anti-HEV IgM | Hepatitis E virus IgM Ab \[Presence\] in Serum |  |
| AVH_ANTIHEV_IGM 83128-9 | Anti-HEV IgM | Hepatitis E virus IgM Ab \[Presence\] in Serum or Plasma by Immunoassay | Not included in default data capture form |
| AVH_HBVGENOTYPE 104995-6 | HBV Genotype (if performed) | Hepatitis B virus genotype \[Identifier\] in Serum or Plasma by Sequencing |  |

</div>

</div>

------------------------------------------------------------------------

## Option Sets

The program uses **11 option sets** which are described below.

DHIS2 admins may choose to edit the metadata to have pre-existing/other
option sets at their discretion.

<div id="tbl-option-sets">

Table 5: Option sets used by the AVH event program

<div class="cell-output-display">

| Option set | id | options |
|:---|:---|:---|
| AVH - Age in Months | GMbJmTPSIAo | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 |
| AVH - Encephalopathy Grade | CLrZ3aWZkSB | No encephalopathy, Grade I, Grade II, Grade III, Grade IV |
| AVH - Final Case Classification | w2wMqZcUDIh | Hepatitis A — Laboratory-confirmed, Hepatitis A — Epidemiologically linked, Hepatitis B — Laboratory-confirmed, Hepatitis C — Laboratory-confirmed, Hepatitis E — Laboratory-confirmed, Hepatitis E — Epidemiologically linked, Non-viral cause identified, Unknown / undetermined |
| AVH - Lab Result | vT4kOPP8lv8 | Positive, Negative, Indeterminate or Equivocal, Not done, Pending, Unknown |
| AVH - Outcome | ztnzxkdtA3H | Alive — Discharged, Alive — Transferred, Died (institutional), Died (community), Unknown |
| AVH - Sex | jroZR2T9JiK | Male, Female |
| AVH - Source of Infection | p4l2G02E7CA | Endemic — local transmission with no imported link, Imported — infection acquired in another country, Import-related — locally acquired from an imported case, Unknown — source not identified |
| AVH - Specimen Type | vrjn9Wvgfyg | Serum, Whole blood, Plasma, Other |
| AVH - Yes / No / Unknown | hR50RixhlE7 | Yes, No, Unknown |
| AVH Hepatitis A/E - Case Classification | LCvADiBniCG | Laboratory-confirmed, Epidemiologically linked, Discarded |
| AVH Hepatitis B/C - Case Classification | RbkKR94kMQI | Laboratory-confirmed, Discarded |

</div>

</div>

## Users Groups and User Roles

### User Groups

The event program metadata creates **2 User groups**.

<div id="tbl-user-groups">

Table 6: User groups associated with the AVH event program

<div class="cell-output-display">

| User group | id | Description |
|:---|:---|:---|
| AVH Level 1 | YRf53KKIFEi | Acute Viral Hepatitis surveillance — Admin users. |
| AVH Level 2 | ZPuPYP20gP1 | Acute Viral Hepatitis surveillance — Data entry personnel. |

</div>

</div>

<div id="tbl-user-groups-privileges">

Table 7: Metadata and Data privileges of user groups

<div class="cell-output-display">

| Objects | AVH Level 1 | AVH Level 2 |
|:---|:---|:---|
| Data Elements | Metadata read+write | Metadata read only |
| Option sets | Metadata read+write | Metadata read only |
| Program | Metadata read+write, Data read+write | Metadata read only, Data read+write |
| Program stage | Metadata read+write, Data read+write | Metadata read only, Data read+write |

</div>

</div>

### User Roles

The program metadata creates **1 User role**.

`AVH Capture User` user role provides users access to the
`Browser Cache Cleaner`, `Capture`, and `Dashboard apps`. If the event
program is being installed to an instance of DHIS2 that already has a
role of comparable functionality, administrators can choose to use the
pre-existing user role for accounts being used to carry out data entry.

## Program Rules

The event program metadata includes **43 Program Rules**. These rules
collectively serve to streamline data capture, enforce consistency
between related data inputs, and to ensure that mandatory data fields
are captured before an event is marked as `Complete`.

The table below gives descriptions of each of the Program Rules.

<div id="tbl-program-rules">

Table 8: AVH Program Rules

<div class="cell-output-display">

| Rule | Description |
|:---|:---|
| Always hide AVH_HEPA_FINALCLASS | Hides Hepatitis A final classification. This value is set by a program rule based on the overall final case classification. |
| Always hide AVH_HEPB_FINALCLASS | Hides Hepatitis B final classification. This value is set by a program rule based on the overall final case classification. |
| Always hide AVH_HEPC_FINALCLASS | Hides Hepatitis C final classification. This value is set by a program rule based on the overall final case classification. |
| Always hide AVH_HEPE_FINALCLASS | Hides Hepatitis E final classification. This value is set by a program rule based on the overall final case classification. |
| Assign Event Date to Date of Visit and Hide Field | Hides the Date of Visit field and sets its value to the event date. This avoids duplication in the data entry form while allowing the Date of Visit field to be used in downstream queries and visualizations. |
| Classification: Hepatitis A — Epidemiologically linked | If the final case classification is Hepatitis A - Epidemiologically linked then: 1) Set Hep A case classification to EpiLinked 2) Set Hep B, Hep C, and Hep E case classifications to Discarded |
| Classification: Hepatitis A — Laboratory-confirmed | If the final case classification is Hep A - Lab-confirmed then: 1) Set Hep A case classification to LabConfirmed 2) Set Hep B, Hep C, and Hep E case classifications to Discarded |
| Classification: Hepatitis B — Laboratory-confirmed | If the final case classification is Hepatitis B - Lab-confirmed then: 1) Set Hep B case classification to Lab confirmed 2) Set Hep A, Hep C, and Hep E case classifications to Discarded |
| Classification: Hepatitis C — Laboratory-confirmed | If the final case classification is Hepatitis C - Lab-confirmed then: 1) Set Hep C case classification to Lab confirmed 2) Set Hep A, Hep B, and Hep E case classifications to Discarded |
| Classification: Hepatitis E — Epidemiologically linked | If the final case classification is Hep E - Epidemiologically linked then: 1) Set Hep E case classification to EpiLinked 2) Set Hep A, Hep B, and Hep C case classifcations to Discarded |
| Classification: Hepatitis E — Laboratory-confirmed | If the final case classification is Hep E - Lab confirmed then: 1) Set Hep E case classification to Lab confirmed 2) Set Hep A, Hep B, and Hep C case classifications to Discarded |
| Classification: Non-viral — set ABCE to Discarded | If the final overall case classication is Nonviral then set Hep A, Hep B, Hep C, and Hep E classifications to Discarded |
| Completion: Anti-HAV IgM required for Hepatitis A lab-confirmed classification | Ensuring that the test result is recorded for a Hep A lab-confirmed classification. |
| Completion: Anti-HEV IgM required for Hepatitis E lab-confirmed classification | Ensuring that the test result is recorded for a Hep E lab-confirmed classification. |
| Completion: At least one age field required | Ensuring that at least one of the fields in the form that allows for determining patient's age is completed. |
| Completion: Date of Onset Required | Ensuring that a date of symptom onset is recorded. |
| Completion: Final Case Classification Required | Case cannot be marked as complete without a final case classification. |
| Completion: HCV RNA required for Hepatitis C lab-confirmed classification | Ensuring that the test result is recorded for a Hep C lab-confirmed classification. |
| Completion: IgM anti-HBc required for Hepatitis B lab-confirmed classification | Ensuring that the test result is recorded for a Hep B lab-confirmed classification. |
| Completion: Sex Required | Ensuring that the patient's sex is recorded. |
| Completion: Specimen Collected is required | Ensuring that specimen collection (Yes/No/Unknown) is documented. |
| Completion: Unique Identifier Required | Ensures that a Patient Identifier is recorded |
| Completion: Valid biomarker profile needed for Hepatitis C lab-confirmed | Ensures that one of the valid biomarker profile is recorded to accompany a hepatitis C lab-confirmed case classification. |
| Error: Anti-HAV IgM must be Positive for Hepatitis A lab-confirmed | Ensuring that the appropriate laboratory test is recorded to substantiate a Hepatitis A lab-confirmed case classification. |
| Error: Anti-HEV IgM must be Positive for Hepatitis E lab-confirmed | Ensuring that the appropriate laboratory test is recorded to substantiate a Hepatitis E lab-confirmed case classification. |
| Error: Contact with confirmed case required for epi-linked classification | Ensuring that contact with a confirmed case is recorded consistent with epi-linked case classification (Hep A or Hep E). |
| Error: IgM anti-HBc must be Positive for Hepatitis B lab-confirmed | Ensuring that the appropriate laboratory test is recorded to substantiate a Hepatitis B lab-confirmed case classification. |
| Error: Onset date after visit date | Ensuring that the date of symptom onset is not later than the date of the visit. |
| Error: Specimen required for lab-confirmed classification | Ensuring that a collected specimen is recorded consistent with a lab-confirmed case classification. |
| Hide Age in Months when DOB entered or Age Years \> 0 | Hides the Age in Months field if DOB or Age in Years \>= 1 are recorded. |
| Hide Associated Case ID when No Contact with Case | Hide field for associated case ID when there's no contact with a confirmed case. |
| Hide Combined Hepatitis A+B Vaccination Details when Not Vaccinated | Hide field for details when the patient was not vaccinated with Hep A+B vaccine. |
| Hide Date of Death when Outcome is not Death | Hide date of death field when the outcome is not death. |
| Hide HBV Genotype unless HBsAg Positive | Hide field for HBV Genotype unless HBsAg test result is Positive. |
| Hide HCV RNA unless Anti-HCV Positive | Hide HCV RNA details unless Anti-HCV is Positive |
| Hide Hepatitis A Vaccination Details when Not Vaccinated | Hide fields for details when the patient was not vaccinated with Hep A vaccine. |
| Hide Hepatitis B Vaccination Details when Not Vaccinated | Hide fields for details when the patient was not vaccinated with Hep B vaccine. |
| Hide Hepatitis E Vaccination Details when Not Vaccinated | Hide field for details when the patient was not vaccinated with Hep E vaccine. |
| Hide Hospitalization and Discharge Dates when Not Hospitalized | Hide fields for details of hospitalization when patient was not hospitalized. |
| Hide Laboratory Fields when No Specimen Collected | Hide fields for laboratory tests when no collected specimen is recorded. |
| Info: Enter DOB or age | Reminds user to enter patient's DOB or age. |
| Note: Final Case Classification Requirements | Show reminder of final case classification criteria. |
| Reminder: Record All Laboratory Tests Performed | Show reminder to enter all available test results. |

</div>

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-LOINC" class="csl-entry">

Regenstrief Institute. *LOINC - LOINC Is the International Standard
for Identifying Health Observations, Measurements, and Documents.*
<a href="https://loinc.org/" class="uri">Https://loinc.org/</a>.

</div>

<div id="ref-who2016technicalhep" class="csl-entry">

World Health Organization. 2016. *Technical Considerations and Case
Definitions to Improve Surveillance for Viral Hepatitis: Technical
Report*. World Health Organization.

</div>

<div id="ref-who2018VPDHepA" class="csl-entry">

World Health Organization. 2018a. *Hepatitis a: Vaccine Preventable
Diseases Surveillance Standards.* World Health Organization.

</div>

<div id="ref-who2018VPDHepB" class="csl-entry">

World Health Organization. 2018b. *Hepatitis a: Vaccine Preventable
Diseases Surveillance Standards.* World Health Organization.

</div>

<div id="ref-who2019SOPHep" class="csl-entry">

World Health Organization. 2019. *Web Annex 1. Standard Operating
Procedures (SOPs) for Enhanced Reporting of Cases of Acute Hepatitis.
In: Consolidated Strategic Information Guidelines for Viral Hepatitis
Planning and Tracking Progress Towards Elimination.* World Health
Organization.

</div>

</div>
