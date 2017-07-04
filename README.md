# OOI Machine to Machine (M2M) Basics
Here the basic instructions to get started using the OOI M2M Web Services, along with a collection of python notebooks demonstrating basic m2m queries for OOI BOTPT data.

## Getting Started
* Create a user account on [ooinet.oceanobservatories.org](https://www.ooinet.oceanobservatories.org)
* Log in
* Navigate to the drop down menu screen in the top-right corner menu
* Click on the "User Profile" element of the drop down.
* Copy and save the following data from the user profile: API Username and API Token.  The API Username is similar to “OOIAPI-QTULEV9STCAS55”.  The API Token is similar to “YXP2Q2W4SOP”.

## Basic Examples Accessing the OOI M2M Web Services
### curl 
`curl –k https://API USERNAME:API TOKEN@ooinet.oceanobservatories.org/api/m2m/12576/sensor/inv/toc`

### python requests 
`requests.get('https://ooinet.oceanobservatories.org/api/m2m/12576/sensor/inv/toc', auth=(API USERNAME, API TOKEN))`

### httpie 
`http --auth API USERNAME:API TOKEN https://ooinet.oceanobservatories.org/api/m2m/12576/sensor/inv/toc`
