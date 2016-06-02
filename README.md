### EMCW---Learning-To-Code

This is a sample app used for my EMC World Presentation

[Launch EMC World HTML5 App from GitHub] (https://htmlpreview.github.io/?https://github.com/brentpiatti/EMCW---Learning-To-Code/blob/master/index.html)

[Launch EMC World HTML5 App from Pivotal Web Services using Cloud Foundry] (http://brentpiatti.cfapps.io/)

### Push to Cloud Foundry

```
cf login -a https://api.run.pivotal.io
cf push emcw-piatti #<--- use your own unique user/app name
```

Scale the application instantly
```
cf scale emcw-piatti -i 2
```

Make code changes to the application and perform a zero downtime application update

```
cf push emcw-piatti-1
cf map-route emcw-piatti-1 cfapps.io -n emcw-piatti
cf scale emcw-piatti-1 -i 2
cf delete emcw-piatti -f
```
