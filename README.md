**Process Scenario**

The ACME company is interested in automating their vendor reporting process. Currently, the team receives monthly reports and merges them to produce a yearly report for each vendor. Below are the steps provided for the manual process.

Access your work items labeled “Generate Yearly Report for Vendor”
Update the work item status as you work through each item
Use the information in the work item to download monthly reports
Combine the monthly reports and upload the yearly report
Retrieve the unique ID
Add unique ID to the comment section of the work item (i.e. Uploaded with ID XYZ)
The ACME team processes around 300 work items per day across 5 team members. The average processing time per item takes ~8 minutes.

**Requirements:**

Create an account in the ACME System (https://acme-test.uipath.com/) - this can be a dummy account and doesn’t need to be tied to a real email address, just take note of your login credentials.
You must use an RPA bot designer (e.g. UiPath Studio, Automation Anywhere). Feel free to sign up for the community edition / trial if you don’t have access to one.
Please time box this assignment to no longer than two hours and provide as robust of a solution as you can within that time frame.
You do not need to complete the whole use case if the time goes over, however, please be prepared to talk through your solution and add placeholders if needed.
Provide or talk through any supporting documentation needed for the process automation.

**Prerequisites**

UiPath version: 22.10.3

Chrome browser latest version must be installed

UiPath Chrome extension must be installed: UiPath Web Automation 22.10 version 22.10.6

Once extension is installed, go to Details, and turn on "Allow in incognito" and "Allow access to file URLs."

Bot user needs full permissions on local Downloads folder.

Latest version of Microsoft Excel.

**In Orchestrator…**

**Folder**

Name: ACME

**Queue**

Name: VendorReporting

Auto Retry: Yes / 1

**Assets**

Refer to assets.xlsx

**Library**

\Packages\ ACME.1.0.1.nupkg

**Process**

\Packages\VendorReporting\_Dispsatcher.1.0.1.nupkg

\Packages\ VendorReporting\_Performer.1.0.1.nupkg

**Run Instructions**

Run VendorReporting\_Dispsatcher to populate queue

Run VendorReporting\_Performer to process each item in the queue

Output from Queue from QA/UAT: VendorReporting-items.csv

**TDDs**

VendorReporting\_Dispatcher\_TDD.docx

VendorReporting\_Performer\_TDD.docx
