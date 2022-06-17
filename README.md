# postman_examples
This project contains an example Postman Mighty Canary Collection and matching Postman environment that you can use to get yourself acquanted with the Mighty Canary APIs.
## Prerequisites
- install Postman from https://postman.com
- From this project, download Mighty_Canary.postman_environment.json and import from the top left banner button *Import*
- do the same for Mighty_Canary.postman_collection.json
## Setup Mighty Canary Environment Variables
In Postman, click on the imported Mighty Canary Environment. Find the API_KEY and put in your Mighty Canary API Token. It can be found by going to a Sentry and copying it from the right banner.

Now we have two paths going forward. Pick you preferred path:
1. **You want to create a sample Sentry and Canary to explore the API** - This is the easiest. You simply find the Postman Collection element - Mighty Canary -> Sentry Requests -> Create Sentry. This will create a new Sentry in your Mighty Canary Application. Go verify that it is present - https://app.mightycanary.com/sentries. Now do the same thing with a Canary. Go to the Postman Collection element - Mighty Canary -> Caanry Requests -> Create Canary. This will create a new Canary in your Mighty Canary Application that is connected to the Sentry just created.
2. **You want to use an existing Sentry and Canary** - Go into Mighty Canary and pick the Sentry you want to use. Copy the API_URL and save it as the Sentry_url Postman Mighty Canary Environment. The last part of the Sentry_url is the Sentry UID. Save this as the evironment variable Sentry_uid. Now copy the Canary embed url and remove **/show** from the end. This is the value of your Canary_url in your Postman Mighty Canary Environment. Finally, the last part of the Canary_url is the Canary UID. Save this as the environment variable Canary_uid.
## Using the Mighty Canary Postman Requests
Now that we are all setup from the above steps, you can use the available examples. Got to the Mighty Canary Collection in Postman and try out the requests:
### Sentry API's
- **Sentry Request->Get Sentry**: returns the json for the configured Sentry above
- **Sentry Request->Make Happy**: changes the configured Sentry to be in state Happy
- **Sentry Request->Make Sad**: changes the configured Sentry to be in state Sad
- **Sentry Request->Make Sick**: changes the configured Sentry to be in state Sick
- **Sentry Request->Create Sentry**: create a new Sentry and configure it as the curent Sentry in use
- **Sentry Request->Delete Sentry**: removes the configured current Sentry from Mighty Canary. Nothing else will work until you configure a new Sentry, and the easiest was to do this is to run the Create Sentry request.
### Canary API's
- **Canary Request->Get Canary**: returns the json for the configured Canary above
- **Canary Request->Make Happy**: changes the configured Canary to be in state Happy
- **Canary Request->Make Sad**: changes the configured Canary to be in state Sad
- **Canary Request->Make Sick**: changes the configured Canary to be in state Sick
- **Canary Request->Create Canary**: create a new Canary and configure it as the curent Canary in use
- **Canary Request->Delete Canary**: removes the configured current Canary from Mighty Canary. Nothing else will work until you configure a new Canary, and the easiest was to do this is to run the Create Canary request.
## Conclusion
Those are the basic elements of the API. You can modify the parameters as discussed in our documentation and try out more advanced ideas such as latest_record_at and row_counts. PR's for improvements are welcome. Happy Canarying!