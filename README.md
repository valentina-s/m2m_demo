# OOI Machine to Machine (M2M) Demo
Basic instructions for using the OOI M2M Web Services. See ipython notebooks for examples using python's requests module. 

## Getting Started
* Create a user account on [ooinet.oceanobservatories.org](https://www.ooinet.oceanobservatories.org) or use the CILogon button with an academic or Google account.
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

## Running the Notebooks
* create a python virtual environment and start the notebook from inside
```
conda create -n m2m_demo python=2.7 anaconda

source activate m2m_demo

pip install xarray==0.9.0

pip install netcdf-python

pip install thredds-crawler

jupyter notebook

source deactivate
```

(The latest `xarray` gives an error, seems a known issue which was fixed in future versions, but for now downgrading to 0.9.0 https://github.com/pydata/xarray/issues/1775)

## Additional Resources
* Data Team QC Database http://ooi.visualocean.net
* Data Portal https://ooinet.oceanobservatories.org
* Sampling Strategy http://oceanobservatories.org/observation-and-sampling-approach  
* Data Product Specifications http://oceanobservatories.org/technical-data-package  
* Data Product Algorithms https://github.com/oceanobservatories/ion-functions/tree/master/ion_functions/data  

## Example Applications Built on Top of M2M Web Services

* Command line toolbox for large scale requests https://github.com/kerfoot/uframe-m2m
* Toolbox to plot data realtime https://github.com/ooi-data-review/ooi-realtime-plotting
