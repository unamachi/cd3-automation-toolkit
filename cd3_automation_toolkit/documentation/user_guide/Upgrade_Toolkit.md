# Steps to Upgrade Your Toolkit (For Existing Customers):

## Upgrade to Release v10.1 from v10
1. Follow the steps in [Launch Docker Container](/cd3_automation_toolkit/documentation/user_guide/Launch_Docker_container.md) to build new image with latest code and launch the container by specifying same path for <directory_in_local_system_where_the_files_must_be_generated> to keep using same outdir.
2. Copy the contents(.tf files and modules directory) from /cd3user/oci_tools/cd3_automation_toolkit/user-scripts/terraform to /cd3user/tenancies/<customer_name>/terraform_files/<region_dir>
3. Changes to the CD3 excel sheet templates include correction of the dropdowns for all tabs, few changes in Policies tab wrt policy statements. So existing customers can keep using the v10 templates.
4. If an existing customer wants to shift to seperate outdir structure for each resource, they must launch a new container and execute createTenancy.py with using outdir with 'outdir_structure_file' parameter set and then run export of the tenanncy into this new outdir using Non Greenfield workflow.

## Upgrade to Release v10 from v9.2.1
1. Follow the steps in [Launch Docker Container](/cd3_automation_toolkit/documentation/user_guide/Launch_Docker_container.md) to build new image with latest code and launch the container by specifying same path for <directory_in_local_system_where_the_files_must_be_generated> to keep using same outdir.
2. Use new excel sheet templates to use OKE and SCH.
3. For existing services, user can continue using existing outdir.

<br><br>
<div align='center'>

| <a href="/cd3_automation_toolkit/documentation/user_guide/FAQ.md">:arrow_backward: Prev</a> | <a href="/README.md#table-of-contents-bookmark">Next :arrow_forward:</a> |
| :---- | -------: |