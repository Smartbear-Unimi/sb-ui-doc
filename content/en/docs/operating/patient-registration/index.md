---
title: "Patient Registration"
description: ""
lead: ""
date: 2023-03-11T12:29:01+01:00
lastmod: 2023-03-11T12:29:01+01:00
draft: false
images: []
menu:
  docs:
    parent: "operating"
    identifier: "patient-registration"
weight: 140
toc: true
mermaid: true
---

## Patient creation

```mermaid
graph TD;
    Start(PATIENT <br>CREATION)-->
    ClickPlusMed(1. Click on **+PATIENT** in the Patients page <br> up to the corner to open the Create Patient form);
    ClickPlusMed--See sec-->FillData(2. Fill the following data <br> to complete the form)
    FillData-->Pilot(2.1 **Pilot:** Click on it and <br> select a value  from the menu)
    Pilot-->SbEmail(2.2 **SB Email:** Click on it and type the patient's <br>  assigned email address  to set up the devices kit)
    SbEmail-->DateOf(2.3 **Date of participant consent:** <br> Click on it and select a date from the calendar)
    DateOf--Figure 1-->Phone(2.4 **Enter a phone number:** <br> Click on it and type the patient's mobile number. <br> The country is detected via the browser. )
    Phone-->UserCCM(2.5 **Username of CCM:** <br> Click on  it and if the CCM  is registered <br> in the platform select the patient's name.)
    UserCCM-->NotRegistered{Is the CCM <br> registered in the platform?}
    NotRegistered--No-->External(**Email of ExternalCCM:** Click on the label and type <br> an email  address which has to receive notifications.)
    NotRegistered--Yes-->MoreCCM{Is the patient managed <br> by more than on CCM?}
	
	
	MoreCCM--Yes-->IfAddDelete{Add or Delete <br> a CCM?}
    IfAddDelete--Add-->AddCCM(**+ button:** Click on it and select the name <br>if a patient is managed by more than one CCM.)
    IfAddDelete--Delete-->DelCCM(**- button:** Click on it to delete a CCM.)

	MoreCCM--No-->IsCompleted
    

	External-->IfAddDelete
	IfAddDelete--No-->IsCompleted{Is the form completed <br> correctly?}

	IsCompleted--Yes-->Create(**CREATE PATIENT:** Click on it to save data)
	IsCompleted--No-->ToCancel{Do you want to cancel it?}
	
	ToCancel--Yes-->Cancel(**CANCEL:** Click on it to discard data.)
	ToCancel--No-->FillData

linkStyle default interpolate basis
```

Click on +PATIENT in the Patients page at the upper right corner (see sec. ) to open the Create patient form.

<figure id="image040" >
<img src="Patient registration images/image040.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image041" class="centered-figure">
<img src="Patient registration images/image041.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>
Fill these data to complete the form:

•	Click on Pilot, (e.g. “Testing”) then select a value from the menu. The Organization field is filled automatically 

<figure id="image042" >
<img src="Patient registration images/image042.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image043" >
<img src="Patient registration images/image043.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

•	Click on SB Email and type the email address that has been assigned to the patient to set up the devices kit 

<figure id="image044" >
<img src="Patient registration images/image044.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image045" >
<img src="Patient registration images/image045.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

•	Click on Date of participant consent and select a date from the calendar 

<figure id="image046" >
<img src="Patient registration images/image046.png" alt="Patient">
<figcaption style="text-align:center"> </figcaption>
</figure>

<figure id="image047" >
<img src="Patient registration images/image047.png" alt="Patient">
<figcaption style="text-align:center">Figure 1. </figcaption>
</figure>

•	Click on Enter a phone number and type the patient’s mobile number. The country is detected via the browser

<figure id="image048" >
<img src="Patient registration images/image048.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image049" >
<img src="Patient registration images/image049.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

•	Click on Username of CCM if the CCM is registered in the platform select his/her name from the menu. If a patient is managed by more than one CCM, click on the + button and select the name if available. To delete a CCM, click on the – button 

<figure id="image050" >
<img src="Patient registration images/image050.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image051" >
<img src="Patient registration images/image051.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

• If a patient is managed by more than one CCM, click on the + button and type the email address. To delete an External CCM, click on the - button.

<figure id="image052" >
<img src="Patient registration images/image052.png" alt="Patient">
<figcaption style="text-align:center"> </figcaption>
</figure>

<figure id="image053" >
<img src="Patient registration images/image053.png" alt="Patient">
<figcaption style="text-align:center"> </figcaption>
</figure>

•	If the CCM is not registered in the platform, click on External CCM, click on the label Email of External CCM and type the email address of the External CCM has to receive the notifications. 

<figure id="image054" >
<img src="Patient registration images/image054.png" alt="Patient">
<figcaption style="text-align:center"> </figcaption>
</figure>

<figure id="image055" >
<img src="Patient registration images/image055.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

```mermaid
graph TD;
    Start(OVERVIEW)--If you want insert and modify<br> data to be collected from the patient <br> follow these instructions:-->Edit(1.**EDIT:** Click on it to fill the Overview Tab.)
    
    Edit-->SbId(**SmartBear ID:** It is filled automatically. )
    SbId-->Bday(**Birthday Date:** It is in the YYYY-MM format. <br> Click on it and select the birth date from the calendar.)
    Bday-->AgeG(**Age Group:** It is filled automatically.)
    AgeG-->Email(**Email:** It is filled automatically.)
    Email-->IsCompleted{Is the form <br> completed correctly? <br> --See Figure 60--}

	IsCompleted--Yes-->Save(**SAVE:** <br>Click on it to save data.)
	IsCompleted--No-->Cancel(**CANCEL:** <br> Click on it to discard data.)
linkStyle default interpolate basis
```

If you have completed the form correctly click on CREATE PATIENT to save the data, otherwise, click on CANCEL to discard them .

<figure id="image056" >
<img src="Patient registration images/image056.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

After the patient is created, the patient’s record is generated, which includes the Overview (see section Overview) and Demographics tabs (see section Demographics).

<figure id="image057" >
<img src="Patient registration images/image057.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>


## Overview {#overview}
To fill the Overview tab, click on EDIT.

<figure id="image058" >
<img src="Patient registration images/image058.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

The Overview tab  allows the user to insert and modify the following data to be collected from the patient:

•	SmartBear ID. It contains the patient’s ID and is filled automatically.
•	Birthday Date. It is in the YYYY-MM format. Click on the Birthday Date and select the date from the calendar
•	Age Group. It is filled automatically
•	Email. It is filled automatically.

<figure id="image059" >
<img src="Patient registration images/image059.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image060" >
<img src="Patient registration images/image060.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

If you have completed the form correctly click on SAVE to save the data, otherwise click on CANCEL to discard them (see Figure 60).

<figure id="image061" >
<img src="Patient registration images/image061.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>


## Demographics

```mermaid
graph TD;
	Start(DEMOGRAPHICS)--If you want insert and modify<br> data to be collected from the patient <br> follow these instructions:-->First(1. **DEMOGRAPHICS:** <br>Click on it to open Demographics tab.)
	First-->BGender(**Biological Gender:** Click on it and select <br> one of the several genders from the menu.)
    BGender-->EduLevel(**Education level:** Click on it and select <br> one education level from the menu.)
    EduLevel-->LivSituation(**Living situation:** Click on it and select one of the <br> description  of the patient's living place from the menu.)
    LivSituation-->SRef(**Source of referral:** Click on Source of Referral and select a person <br> or a medium, that referred the patient to SMART BEAR, from the menu.)
    SRef--Medium -- e.g. social media -->Et(**Ethnicity:** Click on it and select ethnic groups from the menu.)
    Et--Ethnicity required to perform some analytics-->AddDem(In **Additional demographics data:**)
	AddDem-->AtHome(If necessary, tick **Uses stairs at home**.)
	AddDem-->FamSit(**Family situation:** Click on it and select <br> **Lives Alone** or **Lives with family** from the menu.)
	FamSit-->TypeAcc(**Type of accomodation:** Click on it and select a value <br> about patient's living situation from the menu)
	TypeAcc-->IsCompleted{Is the form <br> completed correctly? <br> --See Figure 60--}

	IsCompleted--Yes-->Save(**SAVE:** <br>Click on it to save data.)
	IsCompleted--No-->Cancel(**CANCEL:** <br>Click on it to discard data.)
	IsCompleted
linkStyle default interpolate basis
```


<figure id="Pic_44" >
<img src="images/Pic_44.png" alt="Patient">
<figcaption style="text-align:center">Figure 12.</figcaption>

Click on the DEMOGRAPHICS to open the Demographics tab.  

<figure id="image062" >
<img src="Patient registration images/image062.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image063" >
<img src="Patient registration images/image063.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

To fill the tab, click on EDIT. In Demographics the user is allowed to insert and modify the following data to be collected from the patient:

•	Biological Gender. It can be either a binary non-binary gender. The patient can also choose to NOT disclose this information. Click on Biological Gender and select a value from the menu.
•	Education level. Click on Education Level and select a value from the menu
•	Living situation. It provides a description of the patient’s living place (e.g. an apartment with access to an elevator). Click on Living Situation and select a value from the menu 
•	Source of referral. It is the person or medium (e.g. social media) that referred the patient to SMART BEAR. Click on Source of Referral and select a value from the menu
•	Ethnicity. This information is required to perform some analytics, and refers to large ethnic groups (e.g. caucasian, african). Click on Ethnicity and select a value from the menu
•	If necessary, tick Uses stairs at home
•	Family situation. This information refers to the presence of a family. Click on Lives with and select a value from the menu
•	Type of accommodation. This information consists of further details with regards to the living situations. Click on Type of Accommodation and select a value from the menu.

<figure id="image064" >
<img src="Patient registration images/image064.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image065" >
<img src="Patient registration images/image065.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image066" >
<img src="Patient registration images/image066.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image067" >
<img src="Patient registration images/image067.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image068" >
<img src="Patient registration images/image068.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image069" >
<img src="Patient registration images/image069.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

<figure id="image070" >
<img src="Patient registration images/image070.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>

If you have completed the tab correctly, click on the SAVE button to save the data, otherwise click on the CANCEL button to discard them.

<figure id="image071" >
<img src="Patient registration images/image071.png" alt="Patient">
<figcaption style="text-align:center"></figcaption>
</figure>




