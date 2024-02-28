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

## Overview flowchart



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




## Demographics flowchart

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












