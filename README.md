# poc-jmeter

**Step1:** Download and extract jmeter from [Jmeter](https://jmeter.apache.org/download_jmeter.cgi).

**Step2:** And then we are ready to use jmeter recording.

## For GUI use:

**Step3:** Open jmeter from bin folder, click on file then open and open the jmx file. after opening click the start button to run the test. You can check the result in ***View Results Tree*** listener.

**Step4:** For loadtest, to increase the number of user, click on "Thread Group" and change the ***Number of Threads*** to your desired number of load users.

## Run script from GUI:

**Step5:** Click on ***Clear all*** button to clear previous test result and run again to check the test for your desired number of users.

## Run script from CLI:
**Step1:**
Create the log file in .jtl format. Make sure the location where you are creating the log should be empty.

### Syntax:

`<jmeter bin location>/jmeter.sh -n -t <path to your jmx file> -l <path to the .jtl file>`

### Example:
` jmeter -n -t tests/abc.jmx -l tests/log.jtl`


**Step2:**
Generate the html file from the .jtl file.

### Syntax:
`<jmeter bin location>/jmeter <path to the .jtl file> -o <path to the .html file>`

### Example:
`jmeter -g tests/log.jtl -o tests/results`

***(The results folder needs to be empty)***

For detailed documentation visit [fortefit](https://fortefit.atlassian.net/wiki/spaces/PD/pages/2408579106/Jmeter+Beginning)