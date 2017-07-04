# OOI Machine to Machine (M2M) Basics
Basic instructions for using the OOI M2M Web Services. See ipython notebook for examples using python's requests module. 

## Getting Started
* Create a user account on [ooinet.oceanobservatories.org](https://www.ooinet.oceanobservatories.org)
* Log in
* Navigate to the drop down menu screen in the top-right corner menu
* Click on the "User Profile" element of the drop down.
* Copy and save the following data from the user profile: API Username and API Token.  The API Username is similar to “OOIAPI-QTULEV9STCAS55”.  The API Token is similar to “YXP2Q2W4SOP”.

## Tools to access OOI M2M Web Services

### python requests 
`requests.get('https://ooinet.oceanobservatories.org/api/m2m/...', auth=(API USERNAME, API TOKEN))`

### curl 
`curl –k https://API USERNAME:API TOKEN@ooinet.oceanobservatories.org/api/m2m/...`

### httpie 
`http --auth API USERNAME:API TOKEN https://ooinet.oceanobservatories.org/api/m2m/...`

## Additional Resources
* Data Team QC Database http://ooi.visualocean.net/instruments/view/RS03CCAL-MJ03F-05-BOTPTA301#streams  
* Data Portal https://ooinet.oceanobservatories.org/data_access/?search=botpta301  
* Sampling Strategy http://oceanobservatories.org/observation-and-sampling-approach  
* Data Product Specifications http://oceanobservatories.org/technical-data-package  
* Data Product Algorithms https://github.com/ooici/ion-functions/tree/master/ion_functions/data  

## Example Applications Built on Top of M2M Web Services

* Command line toolbox for large scale requests https://github.com/kerfoot/uframe-m2m
* Toolbox to plot data realtime https://github.com/ooi-data-review/ooi-realtime-plotting
