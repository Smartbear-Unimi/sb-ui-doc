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

To search a patient in the Patient page the user can:
1.	Click on the < (left) and > (right) buttons in the lower right corner in the tab. (see Figure )
2.	Type the patient id in the search bar on top of the tab. (see Figure ).

{{< alert icon="👉" context="info" text="Typing the id in the search box is much faster !" />}}

In each row of the Patients tab the user can click on the following buttons (see Figure ):

•	SHOW. It opens the Patient tab (see sec. ) where the following buttons appear on the left:
o	OVERVIEW which opens Overview page (see sec. )
o	DEMOGRAPHICS which opens the Demographics page (see sec. )
o	DEVICES MANAGEMENT which opens the Devices page (see sec. )
o	ID MANAGEMENT which opens the ID Management page, where the patient IDs are recorded that are assigned in the HOLOBalance and Smart4Health projects (see sec. ).
•	EDIT. It opens the Modify Patient form (see Figure ), where the user can modify the status of a patient in a project. For example, the status: ACTIVE means the patient has been accepted, the status: WITHDRAWN means the patient has chosen to leave the SMART BEAR. (see sec. )


## Patient editing

To change the status of a patient after a dropout, follow the steps below:

1.	Click on EDIT in the Patient’s page, (see Figure ) to open the Modify patient tab (see Figure )
2.	Click on Recruitment status (see Figure ), select a value from the menu (in this case WITHDRAWN) (see Figure ).
3.	Click on withdraw date (see Figure ), select a date from the calendar (see Figure ). 

When the edit is done, click on MODIFY PATIENT (see Figure ) to save the data, otherwise click on CANCEL to discard them.

The other available options for status are the following:
•	PENDING. In this case the patient has not concluded the Baseline Assessment or has not been accepted yet
•	ACCEPTED
•	RISK OF EXCLUSION. In this case the exclusion is recommended, generally because the Medical History or the questionnaire scores highlight some issue. 


## Device Management

Click on DEVICE MANAGEMENT (see Figure ) to open the Devices tab (see Figure ). Data concerning the devices and their status are saved here. A record can be generated for all the devices, and data include the following attributes: Unique Identifier (a unique number that is assigned to a device), Category (for example Smartphone, Smartwatch etc.) and Status (Active, Inactive or Suspended). 

The tab also features the following buttons (see ):

•	+DEVICE. It opens the Assign Device form that is meant for assigning a device to a patient
•	EDIT. It opens the Modify Device form that is meant for the user to modify a device 
•	DELETE. It deletes a device


Follow the steps below to assign a device:

1.	Click on +DEVICE to open Assign Device form (see Figure ). 
2.	Click the Unique ID and type the device ID 
3.	Click on the Status (see Figure ), and select a value from the menu (see Figure 189)
4.	Click on Category type (select Figure ), and select a value from the menu (see Figure )
5.	Click on the Number and type the number 
6.	Click on CREATE DEVICE to save the data, otherwise click on the CANCEL button to discard them (see Figure ).


To modify a device, click on EDIT (see Figure ) to open the Modify Device form. Click on MODIFY DEVICE to save the changes (see Figure ), otherwise click on CANCEL to discard the modifications.

## External Id Management

Click on ID MANAGEMENT (see Figure 195) to open the ID Management tab (see Figure ). The IDs are saved here that are assigned to a patient in the context of the synergies with other projects, e.g. HOLOBalance and (only for the PoP) Smart4Health. Each record of the External ID tab has the following attributes: Unique Identifier, i.e. the ID, the Scope (HOLOBalance, Smart4Health and HA vendor) and the status (Active, Inactive, Suspended).

The following buttons are featured (see Figure ):

•	+EXTERNAL ID. It opens the Create External ID form that allows the user to assign an External ID
•	EDIT. It opens the Modify External ID form that allows the user to modify an External ID
•	DELETE. It deletes an External ID


In order to create an External ID, follow the steps below:

1.	Click on +EXTERNAL ID (see Figure ) to open the Create External ID (see Figure ). 
2.	Click on Unique External ID field and type the Unique External ID 
3.	Click on Status and select a value from the menu (Active, Inactive, Suspended) (see Figure )
4.	Click on Project and select a value from the menu (Holobalance, Smart4health, HA vendor) (see Figure )
5.	Click on CREATE IDENTITY to save the data, otherwise click on CANCEL button to discard them (see Figure ).


To modify an ID, click on EDIT and the Modify External ID form appears that is shown in Figure . Click on UPDATE IDENTITY to save the edit or on the CANCEL button to discard it.

## Clinical Data

Click on the CLINICAL DATA button in a patient’s record and 3 tabs appear (see Figure ):
•	GENERAL, which shows data from the SMART BEAR cloud (see Figure )
•	SMART4HEALTH. Click on SMART4HEALTH to open the Smart4Health which shows data from Smart4Health (see Figure )
•	HOLOBALANCE. Click on HOLOBALANCE to open the HOLOBalance tab, which shows data from HOLOBalance (see Figure ).

## Interventions Management

The Interventions are personalized messages that are delivered to a patient, according to the recorded value of his/her clinical data, and target specific comorbidities. The interventions are triggered based on thresholds, which are set by hand. The work is ongoing on Machine Learning algorithms that will suggest values to adjust the thresholds, based on the pattern a data time series has been following during the monitoring.
Click on INTERVENTIONS (see Figure ) to open the Intervention tab (see Figure ). All the interventions are shown as a record in the tab, and can be deleted. Rule-based Interventions can be created and managed for a patient in the case of CVDs. The parameters of an Intervention for CVDs are the following:

•	Systolic BP Optimal Range
•	Systolic BP Extreme Range
•	Systolic BP Threshold
•	Diastolic BP Optimal Range
•	Diastolic BP Extreme Range
•	Diastolic BP Threshold
