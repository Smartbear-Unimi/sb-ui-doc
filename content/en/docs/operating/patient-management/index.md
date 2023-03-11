---
title: "Patient Management"
description: "Patient Management operations like Edit/Delete etc."
lead: ""
date: 2023-03-11T12:29:42+01:00
lastmod: 2023-03-11T12:29:42+01:00
draft: false
images: []
menu:
  docs:
    parent: "operating"
    identifier: "patient-management"
weight: 170
toc: true
---

## Search

The user can search a patient in the Patient page either by:

1. Clicking on the < (left) and > (right) buttons that are displayed on the lower right corner in the tab.
(see Figure 209)
2. Typing the patient id in the search bar on top of the tab. (see Figure 210).

{{< alert icon="👉" context="info" text="Typing the id in the search box is much faster !" />}}

In each row of the Patients tab the user can click on the following buttons that are shown in Figure 211, each
redirecting to an element:

- __SHOW__. It redirects to the Patient tab (see sec. 4.5) where the following buttons appear on the left:
  - __OVERVIEW__. It redirects to the Overview page (see sec. 4.3.2)
  - __DEMOGRAPHICS__. It redirects to the Demographics page (see sec. 4.3.3)
  - __DEVICES MANAGEMENT__. It redirects to the Demographics page (see sec. 4.6.2)
  - __ID MANAGEMENT__. It redirects to the ID Management page (see sec. 4.6.3)
- __EDIT__. In order to modify a patient, the user must click on the EDIT button and the Modify Patient
form will appear (see Figure 212). (see sec. 4.6.1). In addition, it is possible to modify the status of
recruitment, e.g ACTIVE or WITHDRAWN.

Click on the __SHOW__ button and the patient file appears. Here with the following activities can be carried out:

- Assign and manage the devices (see sec. 4.6.2)
- ID Management (see sec.4.6.3)
- Manage the Clinical data from: SMART BEAR, Smart4Health and HOLOBalance (see sec. 4.6.4)
- Create and manage the Interventions (see sec. 4.6.5).

## Editing

If a patient withdraws, or the Recruitment status is to update, follow the steps below:

1. Click on the Recruitment status label (see Figure 213). A dropdown menu appears, select a value (in
this case WITHDRAWN) (see Figure 214 and Figure 215)
2. Click on withdraw date, select a date from the calendar (see Figure 216)

When the modification is done, click on __MODIFY PATIENT__ to save the data, otherwise click on CANCEL to
discard them (see Figure 217).

## Device Management

Click on the DEVICE MANAGEMENT button and the Device tab appears (see Figure 218 and Figure 219).
The Device Management tab allows the user to view, insert and modify the devices associated to a patient.
Each device is visualized as record in the tab having the following attributes: Unique Identifier (a unique
number identifying a device), Category (e.g. Smartphone, Smartwatch etc.) and Status (Active, Inactive or
Suspended).

The tab also features the following buttons that are shown in Figure 220:

- __+DEVICE__. It opens the Assign Device form that is meant for assigning a device to a patient
- __EDIT__. It opens the Modify Device form that is meant for the user to modify a device
- __DELETE__. It deletes a device

Follow the steps below to assign a device:

1. Click on +DEVICE. The Assign Device form will appear (see Figure 221). The form labels are shown in
Figure 222
2. Click on the Unique ID label and type the device ID (see Figure 223)
3. Click on the Status label and select a value (Active, Inactive, Suspended) from the dropdown menu that
appears (see Figure 224)
4. Click on the Category type label and select a value from the dropdown menu that appears (see Figure
225)
5. Click on the Number label and type the number (see Figure 226)
6. Click on CREATE DEVICE to save the data, otherwise click on the CANCEL button to discard them (see
Figure 227).

In order to modify a device, the user must click on the EDIT button that is shown in and the Modify Device
form will appear that is shown. Click on the MODIFY DEVICE button to save the changes or on the
CANCEL button to discard the modifications as it is shown in.

## External Id Management

Click on the ID MANAGEMENT button that is shown in Figure 229 and the ID Management tab appears that
is shown in Figure 230 and allows the user to view, insert and modify the IDs that are assigned to a patient in
the context of the synergies with other projects, e.g. HOLOBalance and (only for the PoP) Smart4Health. Each
record of the External ID tab has the following attributes: Unique Identifier, i.e. the ID, the Scope
(HOLOBalance), Smart4Health and HA vendor) and the status (Active, Inactive, Suspended).

The following buttons are featured (see Figure 231):

- __+EXTERNAL ID__. It opens the Create External ID form that allows the user to assign an External ID
- __EDIT__. It opens the Modify External ID form that allows the user to modify an External ID
- __DELETE__. It deletes an External ID

In order to create an External ID, follow the steps below:

1. Click on the +EXTERNAL ID button. The form Create External ID appears (see Figure 232 and
Figure 233). The form labels are shown in Figure 234
2. Click on the Unique External ID field and type the Unique External ID (see Figure 235)
3. Click on the Status field. A dropdown menu appears. Select a value (Active, Inactive, Suspended)
(see Figure 236)
4. Click on the Project field. A dropdown menu appears. Select a value (Holobalance, Smart4health, HA
vendor) (see Figure 237)
5. Click on the CREATE IDENTITY button to save the data, otherwise click on the CANCEL button to
discard them (see Figure 238).

In order to modify an ID, click on the EDIT button and the Modify External ID form appears that is shown in
Figure 239. Click on the UPDATE IDENTITY button to save the modification or on the CANCEL button to
discard the modification as it is shown in Figure 240.

## Clinical Data

Click on the CLINICAL DATA button in a patient’s tab and 3 tabs appear (see Figure 241):

- __GENERAL__. The data are from the SMART BEAR cloud are shown here (see Figure 242)
- __SMART4HEALTH__. Click on the SMART4HEALTH button. The data from the Smart4Health cloud
are shown here if the patient is participating to the synergy with Smart4Health (see Figure 243)
- __HOLOBALANCE__. Click on the HOLOBALANCE button. The data from the HOLOBalance cloud
are shown here if the patient is participating to the synergy with HOLOBalance (see Figure 244).

## Interventions Management

Click on the INTERVENTIONS button in a patient’s tab and the Intervention tab appears (see Figure 245
and Figure 246). All the interventions are shown as a record in the tab, and can be deleted. Rule-based
Interventions can be created and managed for a patient in the case of CVDs. The parameters of an Intervention
for CVDs are the following.:

- Systolic BP Optimal Range
- Systolic BP Extreme Range
- Systolic BP Threshold
- Diastolic BP Optimal Range
- Diastolic BP Extreme Range
- Diastolic BP Threshold

Click on +INTERVENTION for creating a new Intervention (see sec. 4.7).