title: "Patient flowchart"
description: "Exclusion Criteria for enrollement"
lead: ""
date: 2023-03-11T12:29:14+01:00
lastmod: 2023-03-11T12:29:14+01:00
draft: false
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

#RISK OF EXCLUSION

```mermaid  
graph TB
subgraph Risk of exclusion
AStep1((Step 1: <br>Exclusion Criteria))
BStep1a(Click on <br>Exclusion criteria)


AStep1-->BStep1a
BStep1a--Step1a<br>Insert <br>Dexterity-->GStep1a
BStep1a--Step1b<br>Insert <br>MoCA-->GStep1b

GStep1a{Dexterity <br> Score < 4?}
GStep1b{MoCA <br> Score > 18?}

GStep1a--YES-->YesStep1a(Do MoCA <br>questionnaire)
GStep1a--NO-->NoStep1a(Risk of<br> exclusion)
NoStep1a-->Exclude1a(Exclude)
NoStep1a-->NoExclude1a(Go Ahead)

Exclude1a-->AStep2
NoExclude1a-->AStep2

GStep1b--YES-->YesStep1b(Assess <br>Cognitive <br>Disorders)
GStep1b--NO-->NoStep1b(Risk of<br> exclusion)
NoStep1b-->Exclude1b(Exclude)
NoStep1b-->NoExclude1b(Go Ahead)

Exclude1b-->AStep2
NoExclude1b-->AStep2

YesStep1a-->AStep2
YesStep1b-->AStep2

AStep2((Step 2))
GStep2{TRUE?}
AStep2--Check <br>Weight Loss<br>and<br>Depression Disorder    -->GStep2

GStep2-->YesStep2(YES)
GStep2-->NoStep2(NO)


YesStep2--Weight Loss-->YesStep2a(Activate Frailty tab<br>                          Go to step 13)
NoStep2-->NoActStep2(No action)

YesStep2--Depression Disorder-->YesStep2b(Activate <br>Mental Disordes tab<br>Go to step 12)

AStep3((Step 3:<br>General<br>Questionnaires))
YesStep2a-->AStep3
YesStep2b-->AStep3
NoActStep2-->AStep3

AStep3-->BStep3(Click on <br>Medical History<br>then on Questionnaires)
BStep3---->GStep3
BStep3---->AStep4((Step 4))-->GStep4
GStep3{GDS >= 12?}
GStep4{IADL <= 2?}

GStep3-->YesStep3(Risk of<br> exclusion)
GStep3-->NoStep3(No action)

YesStep3-->Exclude3(Exclude)
YesStep3-->NoExclude3(Go Ahead)

Exclude3-->AStep5
NoExclude3-->AStep5

GStep4-->YesStep4(Risk of<br> exclusion)
GStep4-->NoStep4(No action)

YesStep4-->Exclude4(Exclude)
YesStep4-->NoExclude4(Go Ahead)

Exclude4-->AStep5
NoExclude4-->AStep5

NoStep3-->AStep5 
NoStep4-->AStep5

AStep5((Step 5:<br>Patient Profiling))
AStep5-->BStep5(Click on Assessments<br>then on<br>Modify a Patient's profile)

GStep5{TRUE?} 


BStep5--Check<br>Hearing Loss-->GStep5
BStep5--Check<br>Balance Disorders-->GStep5
BStep5--Check<br>Cardiovascular-->GStep5
BStep5--Check<br>Mental Disorders-->GStep5
BStep5--Check<br>Cognitive Disorders-->GStep5
BStep5--Check<br>Frailty-->GStep5
BStep5--Check<br>Back Pain-->GStep5

GStep5-->YesStep5(YES)
GStep5-->NoStep5(NO)


YesStep5--Cardivascular-->ActStep5(Activate<br>Cardiovascular tab)
YesStep5--Hearing Loss<br>Balance Disorders<br>Mental Disorders<br>Cognitive Disorders<br>Frailty<br>Back Pain                        -->NoActionStep5(No action)
NoStep5-->DisStep5(Disable tab)

ActStep5-->AStep6
DisStep5-->AStep6
NoActionStep5-->AStep6

AStep6((Step 6:<br>Mental Disorders))
AStep6-->BStep6(Click on <br>Mental Disorders<br> then on Questionnaires)
BStep6--Insert GDS-->CStep6{GDS >= 12?}
CStep6--YES-->YesStep6(Risk of <br> exclusion)
CStep6--NO-->NoStep6(No action)

YesStep6-->Exclude6(Exclude)
YesStep6-->NoExclude6(Go Ahead)

Exclude6-->AStep7
NoExclude6-->AStep7

NoStep6-->AStep7

AStep7((Step 7:<br> Cognitive Disorders<br>Assessment))
AStep7-->BStep7(Click on <br>Cognitive Disorders<br> then on Questionnaires)
BStep7--Insert GDS-->CStep7{GDS >= 12?}
CStep7--YES-->YesStep7(Risk of <br> exclusion)
CStep7--NO-->NoStep7(No action)

YesStep7-->Exclude7(Exclude)
YesStep7-->NoExclude7(Go Ahead)

Exclude7-->AStep8
NoExclude7-->AStep8

NoStep7-->AStep8

AStep8((Step 8: <br>Frailty))
AStep8-->BStep8(Click on Frailty<br>then on Questionnaires)
BStep8--Insert EFS-->CStep8{12<=EFS<=17}
CStep8--YES-->YesStep8(Risk of <br> exclusion)
CStep8--NO-->NoStep8(No action)

YesStep8-->Exclude8(Exclude)
YesStep8-->NoExclude8(Go Ahead)

%% set linkStyle
linkStyle default interpolate linear

style AStep1 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep2 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep3 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep4 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep5 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep6 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep7 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
style AStep8 fill:#255, stroke:#FFFFFF,stroke-width:2px, color:#000000;
end 


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
