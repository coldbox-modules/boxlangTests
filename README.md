# Workflow to trigger Boxlang tests in Coldbox Modules

This workflow trigger snapshot workflow to run Boxlang tests, download test results and publish them as check run in this repository. Scenarios:

### Boxlang tests with success conclusion
If Boxlang tests are success, job has triggered tests will finish with success and publish tests results as a success check run. Test results file are uploaded as artifacts

### Boxlang tests with failure conclusion
When Boxlang tests fail, job has triggered will finish with failure and publish tests results as failed check run. Test results file are uploaded as artifacts

### Boxlang test with errors (due Boxlang engine or any other event)
When Boxlang tests has errors, job has triggered will finish with failure and check run is not generated, also logs from Boxlang tests job is retrieve to upload as artifact

>[!NOTE]
> Currently only ColdBox Modules with workflow file name `snapshot.yml` are triggered. Others will be added.
