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