---
title: "Patient flowchart"
description: "Exclusion Criteria for enrollement"
lead: ""
date: 2023-03-11T12:29:14+01:00
lastmod: 2023-03-11T12:29:14+01:00
draft: true
images: []
menu:
  docs:
    parent: "operating"
    identifier: "exclusion-criteria"
weight: 150
toc: true
mermaid: true
---

<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
<style>
#flowchart {
  display: none;
}
</style>
<script>
function toggleFlowchart() {
  var x = document.getElementById("flowchart");
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
</script>
</head>
<body>
<button onclick="toggleFlowchart()">Recruitment Process Flowchart</button>

<div id="flowchart" style="display: none;">

## PROFILING PROCESS
**Patient profiling & Risk of exclusion**

```mermaid  
graph TB



%% Change the color of the link 
AStep1<==>Link1<==>ProfilingAStep1 
AStep3<==>Link2<==>ProfilingAStep5
AStep5<==>Link3<==>ProfilingAStep2
AStep6<==>Link4<==>ProfilingAStep6
AStep7<==>Link5<==>ProfilingAStep7
AStep8<==>Link6<==>ProfilingAStep8

Link1((=))
Link2((=))
Link3((=))
Link4((=))
Link5((=))
Link6((=))



subgraph Patient Profiling
ProfilingAStep1((Step 1: <br>Exclusion Criteria))
ProfilingBStep1a(Profiling Click on <br>Exclusion criteria)

ProfilingAStep1-->ProfilingBStep1a
ProfilingBStep1a--Step1a<br>Insert <br>Dexterity-->ProfilingGStep1a
ProfilingBStep1a--Step1b<br>Insert <br>MoCA-->ProfilingGStep1b
ProfilingBStep1a--Step1c<br>Insert <br>MoCA-->ProfilingGStep1c

ProfilingGStep1a{Profiling Dexterity <br> Score < 4?}
ProfilingGStep1b{Profiling MoCA <br> Score > 18?}
ProfilingGStep1c{Profiling MoCA <br> Score > 26?}

ProfilingGStep1a--YES-->ProfilingYesStep1a(Do MoCA <br>questionnaire)
ProfilingGStep1a--NO-->ProfilingNoStep1a(Risk of<br> exclusion)

ProfilingNoStep1a-->Exclude1aa(Exclude)
ProfilingNoStep1a-->NoExclude1aa(Go Ahead)

ProfilingGStep1b--YES-->ProfilingYesStep1b(Assess <br>Cognitive <br>Disorders)
ProfilingGStep1b--NO-->ProfilingNoStep1b(Risk of<br> exclusion)

ProfilingNoStep1b-->Exclude1bb(Exclude)
ProfilingNoStep1b-->NoExclude1bb(Go Ahead)

ProfilingGStep1c--YES-->ProfilingNoActionStep1c(No action)
ProfilingGStep1c--NO-->ProfilingActStep1c(Activate Cognitive <br> Disorders tab,<br> then go to step 8)

Exclude1aa-->ProfilingAStep2
NoExclude1aa-->ProfilingAStep2
Exclude1bb-->ProfilingAStep2
NoExclude1bb-->ProfilingAStep2

ProfilingYesStep1a-->ProfilingAStep2
ProfilingYesStep1b-->ProfilingAStep2
ProfilingNoActionStep1c-->ProfilingAStep2
ProfilingActStep1c-->ProfilingAStep2

ProfilingAStep2((Step 2:<br>Medical History))
ProfilingAStep2-->ProfilingBStep2(Click on Medical History<br>then on<br>General Information)

ProfilingGStep2{TRUE?} 


ProfilingBStep2--Check<br>Substance abuse-->ProfilingGStep2
ProfilingBStep2--Check<br>Brain injury-->ProfilingGStep2
ProfilingBStep2--Check<br>Hearing Loss-->ProfilingGStep2
ProfilingBStep2--Check<br>Uses Hearing Aids-->ProfilingGStep2
ProfilingBStep2--Check<br>Cognitive Issue-->ProfilingGStep2
ProfilingBStep2--Check<br>Weight Loss-->ProfilingGStep2
ProfilingBStep2--Check<br>Depression/Anxiety<br> Disorder-->ProfilingGStep2

ProfilingGStep2-->ProfilingYesStep2(YES)
ProfilingGStep2-->ProfilingNoStep2(NO)

ProfilingYesStep2--Substance abuse<br>Brain injury<br>-->ProfilingRiskStep2(Risk of<br>exclusion)
ProfilingYesStep2--Hearing Loss-->ProfilingHearingLoss(Activate <br>Hearing Loss tab)
ProfilingYesStep2--Uses <br> Hearing Aids-->ProfilingHearingAids(Dectivate <br>Hearing Loss tab)
ProfilingYesStep2--Cognitive<br>Issue-->ProfilingCognitiveIssue(Activate <br> Cognitive Disorders tab<br>Go to step 8)
ProfilingYesStep2--Weight Loss-->ProfilingWeightLoss(Activate Frailty tab,<br> Go to Step 9)
ProfilingYesStep2--Depression Disorder <br> Anxiety Disorder-->ProfilingDisorders(Activete <br> Mental Disorder tab<br> Go to step 7)

ProfilingNoStep2-->ProfilingNoActStep2(No action)

ProfilingNoActStep2-->ProfilingAStep3((Step 3: <br> Life Habits))

ProfilingRiskStep2-->RiskExclude2(Exclude)
ProfilingRiskStep2-->RiskNoExclude2(Go Ahead)
RiskExclude2-->ProfilingAStep3
RiskNoExclude2-->ProfilingAStep3

ProfilingHearingLoss-->ProfilingAStep3
ProfilingHearingAids-->ProfilingAStep3
ProfilingCognitiveIssue-->ProfilingAStep3
ProfilingWeightLoss-->ProfilingAStep3
ProfilingDisorders-->ProfilingAStep3

ProfilingAStep3-->ProfilingBStep3(Click on Medical History <br> then on Life Habits)
ProfilingBStep3--Insert Habits-->ProfilingCStep3{Falls>0?}
ProfilingCStep3--YES-->ProfilingYesStep3(Activate <br> Balance Disorders tab)
ProfilingCStep3--NO-->ProfilingNoStep3(No action)

ProfilingYesStep3-->ProfilingAStep5
ProfilingNoStep3-->ProfilingAStep5

ProfilingAStep5((Step 5: <br>General <br>Questionnaires))
ProfilingAStep5-->ProfilingBStep5(Click on<br>Medical History <br> then on Questionnaries)
ProfilingBStep5--Insert GDS-->ProfilingGDSStep5{GDS>=12?}
ProfilingBStep5--Insert IADL-->ProfilingIADLStep5{IADL<=2}

ProfilingRiskStep5a(Risk of<br>exclusion)
ProfilingRiskStep5b(Risk of<br>exclusion)
ProfilingRiskStep5a-->RiskExclude5a(Exclude)
ProfilingRiskStep5b-->RiskExclude5b(Exclude)
ProfilingRiskStep5a-->RiskNoExclude5a(Go Ahead)
ProfilingRiskStep5b-->RiskNoExclude5b(Go Ahead)


ProfilingNoActStep5a(No action<br>Go to step 9)
ProfilingNoActStep5b(No action<br>Go to step 9)

ProfilingGDSStep5--YES-->ProfilingRiskStep5a
ProfilingIADLStep5--YES-->ProfilingRiskStep5b
ProfilingGDSStep5--NO-->ProfilingNoActStep5a
ProfilingIADLStep5--NO-->ProfilingNoActStep5b

RiskExclude5a-->ProfilingAStep6
RiskNoExclude5a-->ProfilingAStep6
RiskExclude5b-->ProfilingAStep6
RiskNoExclude5b-->ProfilingAStep6
ProfilingNoActStep5a-->ProfilingAStep6
ProfilingNoActStep5b-->ProfilingAStep6

ProfilingAStep6((Step 6:<br>Mental Disorders))
ProfilingAStep6-->ProfilingBStep6(Click on Mental Disorders<br>then on Questionnaires)
ProfilingBStep6--Insert GDS-->ProfilingCStep6{GDS>=12?}
ProfilingCStep6--YES-->ProfilingYesStep6(Risk of<br>exclusion)
ProfilingCStep6--NO-->ProfilingNoStep6(No action<br>Go to step 9)

ProfilingYesStep6-->RiskExclude6(Exclude)
ProfilingYesStep6-->RiskNoExclude6(Go Ahead)

RiskExclude6-->ProfilingAStep7
RiskNoExclude6-->ProfilingAStep7
ProfilingNoStep6-->ProfilingAStep7

ProfilingAStep7((Step 7:<br>Cognitive Disorders))
ProfilingAStep7-->ProfilingBStep7(Click on Cognitive Disorders<br> then on Questionnaires)
ProfilingBStep7--Insert GDS-->ProfilingCStep7{GDS>=12?}
ProfilingCStep7--YES-->ProfilingYesStep7(Risk of<br>exclusion)
ProfilingCStep7--NO-->ProfilingNoStep7(No action<br>Go to step 9)

ProfilingYesStep7-->RiskExclude7(Exclude)
ProfilingYesStep7-->RiskNoExclude7(Go Ahead)

RiskExclude7-->ProfilingAStep8
RiskNoExclude7-->ProfilingAStep8
ProfilingNoStep7-->ProfilingAStep8

ProfilingAStep8((Step 8:<br>Frailty))
ProfilingAStep8-->ProfilingBStep8(Click on Frailty<br>then on Questionnaires)
ProfilingBStep8--Insert EFS-->ProfilingCStep8a{0<=EFS<=5?}
ProfilingBStep8--Insert EFS-->ProfilingCStep8b{12<=EFS<=17?}

ProfilingCStep8a--YES-->ProfilingYesStep8a(Deactivate<br>Frailty tab)
ProfilingCStep8a--NO-->ProfilingNoStep8a(Go to Step 8b)
ProfilingCStep8b--YES-->ProfilingYesStep8b(Risk of<br>exclusion)
ProfilingCStep8b--NO-->ProfilingNoStep8b(No action <br>Go to step 9)

ProfilingYesStep8b-->RiskExclusion8b(Exclude)
ProfilingYesStep8b-->RiskNoExclusion8b(Go Ahead)

RiskExclusion8b-->ProfilingAStep9
RiskNoExclusion8b-->ProfilingAStep9

ProfilingYesStep8a-->ProfilingAStep9
ProfilingNoStep8a-->ProfilingAStep9
ProfilingNoStep8b-->ProfilingAStep9

ProfilingAStep9((Step 9:<br>Patient Profiling))
ProfilingAStep9-->ProfilingBStep9(Click on Assessments<br>then on <br> Modify a Patient's profile)

ProfilingCStep9{TRUE?}

ProfilingBStep9--Hearing<br>Loss-->ProfilingCStep9
ProfilingBStep9--Balance<br>Disorders-->ProfilingCStep9
ProfilingBStep9--Cardiovascular-->ProfilingCStep9
ProfilingBStep9--Mental<br>Disorders-->ProfilingCStep9
ProfilingBStep9--Cognitive<br>Disorders-->ProfilingCStep9
ProfilingBStep9--Frailty-->ProfilingCStep9
ProfilingBStep9--Back Pain-->ProfilingCStep9

ProfilingCStep9--->ProfilingYesStep9(YES)
ProfilingCStep9--->ProfilingNoStep9(NO)

ProfilingYesStep9--Hearing Loss<br>Balance Disorders<br>Mental Disorders<br>Cognitive Disorders<br>Frailty<br>Back Pain-->ProfilingNoActStep9(No action)
ProfilingYesStep9--Cardiovascular-->ProfilingActStep9(Activate <br>Cardiovascular tab)
ProfilingNoStep9---->ProfilingDisStep9(Disable tab)

%% set linkStyle
linkStyle default interpolate linear

style ProfilingAStep1 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep2 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep3 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep5 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep6 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep7 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep8 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style ProfilingAStep9 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;

end
```

</div>

</body> </html>
