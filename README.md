Hey everyone!
Today, I’ll be walking through a lab focused on STIG (Security Technical Implementation Guides) and SCAP (Security Content Automation Protocol)—two key tools widely used across DoD environments for enforcing security compliance and hardening systems.

These tools are critical for ensuring systems meet NIST and DoD cybersecurity standards, and this lab will demonstrate how to use them in a practical setting. Stay tuned as I break down the setup, scanning process, and how to interpret the results!


## Installation Steps SCAP 

1. To get started, download the SCAP Compliance Checker from the official DoD Cyber Exchange site: https://public.cyber.mil/stigs/scap/. You’ll also need to download the appropriate SCAP benchmark, which serves as the tool's input. For this lab, I will use the Windows 11 SCAP benchmark to assess system compliance.

2. Once the SCAP Compliance Checker is installed and the appropriate benchmark file has been selected, your setup should resemble the following:



![Alt Text](https://github.com/JamahdPerry99/STIG-and-SCAP/blob/23c41a3993f38d3ea0c96edd5d51580b97348d15/SCAP%20once%20its%20installed%20with%20appropriate%20benchmark.png)


3. To begin the scan, click on the "Start Scan" button located in the left-hand menu. After the scan completes, a "View Results" option will become available, allowing you to examine the compliance report in detail.



4. You should now see a summary screen similar to the one below. At the top, you'll find details of the completed scan session along with the directory where the results have been saved (note: this file path is important for future reference). In the bottom-left corner, the Host Name is displayed, while the bottom-right corner shows the available Report Types. You will want to select the Non-Compliance report. 




![Alt Text](https://github.com/JamahdPerry99/STIG-and-SCAP/blob/f2c515394c9b0a7323bb67aaef47fc3bf98260c6/what%20you%20will%20see%20after%20you%20select%20view%20my%20results.png)


5. This is an example of how the compliance report is presented. It includes key sections such as Score, System Information, Content Information, Results, and Detailed Results.

One important aspect to note is the categorization of findings into CAT I, CAT II, and CAT III:

- CAT I indicates high-severity vulnerabilities

- CAT II represents medium-severity issues

- CAT III refers to low-severity findings

Understanding these categories is crucial for prioritizing remediation efforts.


![Alt Text](https://github.com/JamahdPerry99/STIG-and-SCAP/blob/f2c515394c9b0a7323bb67aaef47fc3bf98260c6/Part%20one%20of%20scan%20seeing%20your%20score%20.png)




## Installation Steps STIG


1. To begin, download the STIG Viewer from the official DoD Cyber Exchange: https://public.cyber.mil/stigs/srg-stig-tools/. You’ll also need the appropriate Security Technical Implementation Guide (STIG) file which can be found here: https://public.cyber.mil/stigs/downloads/. For this lab, I will be using the Windows 11 STIG to assess compliance against the applicable security requirements.


2. Once the STIG Viewer is installed, open the application and load the STIG file you downloaded (in this case, the Windows 11 STIG). The interface should now resemble the example shown below.




![Alt Text](https://github.com/JamahdPerry99/STIG-and-SCAP/blob/4a0df5ba8165d800f342d8ea5b8cbd300bacdec5/STIG%20viewer%20after%20download%20and%20STIG%20input.png)




3. In STIG Viewer, navigate to the Main tab and scroll to the bottom section labeled Checklist. Click New to create a new checklist.

- On the left-hand side, click the ➕ icon next to Microsoft Windows 11 to apply the corresponding STIG.

- Next, in the top-right corner, click Import, then select "Import XCCDF or CMRS Results." Locate and select the XCCDF file from the SCAP results directory referenced in Step 4.

- Finally, in the top-right corner, click "Fill Checklist". This will populate the checklist with your SCAP results, making them easier to navigate and interpret within STIG Viewer’s user-friendly interface.


4. When reviewing the results in STIG Viewer, you can filter findings by CAT I, CAT II, and CAT III to prioritize vulnerabilities based on severity.

On the far right-hand side, you’ll see a pie chart that visually summarizes the assessment status:

- Green – Compliant (Not a finding)

- Black – Not Applicable to your system

- Grey – Not Reviewed and requires manual analysis

- Red – Open Vulnerabilities present on the system

Each listed vulnerability includes a description explaining why it is considered a finding and provides detailed mitigation guidance to help you remediate the issue effectively.



![Alt Text](https://github.com/JamahdPerry99/STIG-and-SCAP/blob/8e1706dfb5dc22b6b4bbda35f6552e413eb574b6/STIG%20Viewer%20with%20results.png)


## Summary

STIGs define secure configuration baselines, while SCAP provides a standardized way to automate compliance checks against those baselines. When used together, they streamline the process of identifying, categorizing, and remediating system vulnerabilities. This combination ensures faster, consistent, and more accurate security assessments, especially in government and DoD environments.


