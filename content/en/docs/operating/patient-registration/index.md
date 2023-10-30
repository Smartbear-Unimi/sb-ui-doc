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

After the patient is created, the patient’s record is generated, which includes the Overview (see section 4.3.2) and Demographics tabs (see section 4.3.3).

<figure id="Pic_32" >
<img src="images/Pic_32.png" alt="Patient">
<figcaption style="text-align:center">Figure 1. </figcaption>
</figure>

<figure id="Pic_33" class="centered-figure">
<img src="images/Pic_33.png" alt="Patient">
<figcaption style="text-align:center">Figure 2. </figcaption>
</figure>



<figure id="Pic_34" >
<img src="images/Pic_34.png" alt="Patient">
<figcaption style="text-align:center">Figure 3. </figcaption>
</figure>



<figure id="Pic_35" >
<img src="images/Pic_35.png" alt="Patient">
<figcaption style="text-align:center">Figure 4. </figcaption>
</figure>



<figure id="Pic_36" >
<img src="images/Pic_36.png" alt="Patient">
<figcaption style="text-align:center">Figure 5. </figcaption>
</figure>


<figure id="Pic_37" >
<img src="images/Pic_37.png" alt="Patient">
<figcaption style="text-align:center">Figure 6. </figcaption>
</figure>



<figure id="Pic_38" class="centered-figure">
<img src="images/Pic_38.png" alt="Patient">
<figcaption style="text-align:center">Figure 7. </figcaption>
</figure>


</figure>

## Overview {#overview}

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


<figure id="Pic_40" >
<img src="images/Pic_40.png" alt="Patient">
<figcaption style="text-align:center">Figure 8.</figcaption>
</figure>




<figure id="Pic_41" >
<img src="images/Pic_41.png" alt="Patient">
<figcaption style="text-align:center">Figure 9. </figcaption>
</figure>

<figure id="Pic_42" >
<img src="images/Pic_42.png" alt="Patient">
<figcaption style="text-align:center">Figure 10. </figcaption>
</figure>




<figure id="Pic_43" >
<img src="images/Pic_43.png" alt="Patient">
<figcaption style="text-align:center">Figure 11. </figcaption>
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
</figure>





<figure id="Pic_45" >
<img src="images/Pic_45.png" alt="Patient">
<figcaption style="text-align:center">Figure 13.</figcaption>
</figure>





<figure id="Pic_46" >
<img src="images/Pic_46.png" alt="Patient">
<figcaption style="text-align:center">Figure 14.</figcaption>
</figure>





<figure id="Pic_47" >
<img src="images/Pic_47.png" alt="Patient">
<figcaption style="text-align:center">Figure 15.</figcaption>
</figure>





<figure id="Pic_48" >
<img src="images/Pic_48.png" alt="Patient">
<figcaption style="text-align:center">Figure 16.</figcaption>
</figure>





<figure id="Pic_49 >
<img src="images/Pic_49.png" alt="Patient">
<figcaption style="text-align:center">Figure 17.</figcaption>
</figure>



<figure id="Pic_50" >
<img src="images/Pic_50.png" alt="Patient">
<figcaption style="text-align:center">Figure 18.</figcaption>
</figure>





<figure id="Pic_51" >
<img src="images/Pic_51.png" alt="Patient">
<figcaption style="text-align:center">Figure 19.</figcaption>
</figure>




<figure id="Pic_52" >
<img src="images/Pic_52.png" alt="Patient">
<figcaption style="text-align:center">Figure 20.</figcaption>
</figure>





<figure id="Pic_53" >
<img src="images/Pic_53.png" alt="Patient">
<figcaption style="text-align:center">Figure 21.</figcaption>
</figure>






