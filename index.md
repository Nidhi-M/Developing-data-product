---
title       : BMI and BMR Calcultor
subtitle    : Developing Data Products Assignment
author      : Nidhi Mavani  
job         : Software Engineer
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {selfcontained, draft}
knit        : slidify::knit2slides
---



## Requirements

Hi All,  
For this App you may have to know the following     
1. Height (in Cms)  
2. Weight (in Kgs)  
3. Age (in Years)  
4. Gender  

## BMI and BMR  
<b>Body Mass Index(BMI)</b>, is a scale that provides an indication of your overall body composition and fat.   
<b>Basal Metabolic Rate (BMR)</b>, is a measure of the amount of energy your body requires to perform its normal vital functions at rest.  
Your BMI and BMR are related in the sense that a lager body composition is generally associated with a higher BMR  
If you have a BMI that falls outside the normal range, you can use your BMR to accurately determine the number of calories you need to consume each day to either gain or lose weight.
<b> BMR </b> : Kcal/Day 

---
    
## Formulae    

<b> BMI </b>  
BMI = weight(in kgs)/ (height in m ) ^ 2  
<b> BMR </b>   
for men, 
The Revised Harris-Benedict Equation:
W
for men,  
P = 13.397 * weight(kgs) + 4.799 * height(cms) - 5.677 * age + 88.362  
for women,    
P = 9.247 * weight(kgs) + 3.098 * height(cms)- 4.330 * age + 447.593   

Example Data  

```r
weight = 75
height = 172
age = 25
gender ="male"
```

---    
## R code 
<b> BMI </b>    

```r
bmi<-function(weight,height){weight/((height/100)^2)}
bmi(weight,height)
```

```
## [1] 25.35154
```
<b> BMR </b>  

```r
bmrMale<-function(weight,height,age){
  13.397*weight + 4.799*height - 5.677*age + 88.362 }
bmrFemale<-function(weight,height,age){
  9.247*weight+ 3.098*height- 4.330*age + 447.593 }
bmrMale(weight,height,age)
```

```
## [1] 1776.64
```

---
    
## BMI Table
below 18.5   : underweight  
18.5 to 24.9 : normal  
30 to 34.9   : overweight  
35 and above : obese


Eat Healthy , Stay Healthy   

