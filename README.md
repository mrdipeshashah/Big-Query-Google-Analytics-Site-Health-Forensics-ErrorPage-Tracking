This repository contains Big Query code using Google Analytics raw data tracking error page performance, when a user lands on a 404 error page impacting user experience and in turn potenital revenue loss. 

I have developed a looker studio dashboard (https://lookerstudio.google.com/reporting/860ddb8e-f645-4bc3-9a95-e787e6665ad8) that brings the insights to life. 

The steps required:

1. To be able to generate the data to build the dashboard it requires implementing this GTM container > https://github.com/GTMRecipeContainers/Google-Analytics-4-Error-Page-Tracking it will require configuring the triggers + GA4 event tag that works best for the website
2. Google Analytics is connected to Big Query
3. The 2 Big Query codes provided, create and save the views in Big Query
4. Make a copy of the looker studio dashboard and connect it to the saved views

Watch-Outs: 

1. The Error Rate metric coems from the error-rate-view which is used in the scorecard and couple of the charts
2. The calculation for Error Metrics is - SUM(error_sessions)/SUM(total_sessions)
3. Rest of the dashboard is coming from master-view
