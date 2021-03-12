# Mule4

Steps to enable secure properties in Mule 4 are as follows:
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

STEP 1 : 

Open Anypoint Studio -> Go to Help -> Select Install New Software 

Click the Add button and it will open a window, provide Name as Anypoint Enterprise Security and provide location as http://security-update-site-1.4.s3.amazonaws.com and press ok.

Go to the work drop-down and check Anypoint Enterprise Security — in the dropdown list. 

Select it and select the Premium checkbox -> click Next — accept the policy and finish.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

STEP 2: 

Add dependency for mule-secure-configuration-property-module

for example : 
<dependency>
  <groupId>com.mulesoft.modules</groupId>
  <artifactId>
      mule-secure-configuration-property-module
  </artifactId>
  <classifier>mule-plugin</classifier>
  <version>1.2.3</version>
</dependency>
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

STEP 3: 

> create .properties or .yaml configuration file for properties.
> add properties and value to properties.
> open property file in mule app property editor by right clicking on property file in project explorer.
> double click on property and select encrypt option to encrypt property.
> select encryption algorithm from list and add encrypt key.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

STEP 4 : 

> use 'secure' place holder to access secure property.
  for example : ${secure::host}
  
   
