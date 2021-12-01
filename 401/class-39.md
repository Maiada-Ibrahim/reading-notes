ANALYTICS

The Analytics category enables you to collect analytics data for your App
![](https://d1.awsstatic.com/IoT/diagrams/product-page-diagram_AWS-IoT-Anayltics_how-it-works.a5019170e9ea35fbcec683cf4a394d7a5daa6644.png)

## Set up Analytics backend
- mplify add analytics
- amplify push
- Install Amplify Libraries and sync now

- Initialize Amplify Analytics(addPlugin)

- To record an event, create an AnalyticsEvent and call Amplify.Analytics.recordEvent()

- amplify console analytics

## Record events
- flush out to the network every 30 seconds we can change  amplifyconfiguration.json

-we can call it any time with Amplify.Analytics.flushEvents(); 

- call Amplify.Analytics.disable(); for disable
-call  Amplify.Analytics.enable();call for enable

- it's Automatically track sessions by amplify console analytics and select Session Start and Session Stop events to filter on session events

- Custom User Attributes will appear when identifyUser as customProperties and userAttributes that happened because  Pinpoint console makes that data available as part of the criteria for segment creation.

- we can retrieve the escape hatch to access the underlying Amazon Pinpoint client

- Existing Amazon Pinpoint resources can be used with the Amplify Libraries by referencing your Application ID and Region in your amplifyconfiguration.json file