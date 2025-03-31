# Marketing Cloud Automation Inventory

Have you ever found yourself sifting through countless automations and activities trying to locate where a particular Data Extension is used within Salesforce Marketing Cloud? 
This solution can streamline this process, enabling you to efficiently pinpoint automations by keywords and manage them effectively. You can use it for migrating/updating process for example.
This package includes all essential components, such as Data Extensions, a Polyfill, an Automation, and a Script Activity.

## Package Components:
### Data Extensions:
- DE_AUTOMATION_INVENTORY
- DE_AUTOMATION_INVENTORY_ERROR_LOG

### Polyfill:
- CS_POLYFILL_HELPERS

### Automation:
- AUT_AUTOMATION_INVENTORY

### Script Activity:
- SC_AUTOMATION_INVENTORY

## Deployment Steps:
### Import the Package:
1. Donwload the JSON file in this repository.
2. Using Marketing Cloud menu, navigate to **Platform**, then **Package Manager**.
3. Click **Deployment**.
4. Under the Deployment tab, hit **Deploy**.
5. Click **Upload**, select the JSON file that you downloaded from this repository, click **Done**, **Next**, verify if all items are being created and click **Deploy**.
6. Wait until it is complete and hit **Done**.

### Validate Installation:
- Check that all components listed are correctly installed in their respective sections.
- They have been created in respective studios under Automation Inventory folder.

## Updating Script Variables:
### Access the Script Activity:
- In Automation Studio, locate the SC_AUTOMATION_INVENTORY script activity within the installed automation.
- Edit the script activity to view the SSJS code.

### Modify Variables:
- Update the variable definitions at the top of the script:
  - `includeOnlyActiveAuto`: Set to true or false to filter active or all automations.
  - `targetValues`: Update this array to include keywords relevant to the automations you wish to track.
  - `businessUnitName`: Configure it according to your BU Name.
- Save changes to ensure the script runs with the updated settings.

### Test the Configuration:
- Execute the script activity manually to ensure it performs as expected with the updated variables.
- Check the DE_AUTOMATION_INVENTORY and DE_AUTOMATION_INVENTORY_ERROR_LOG Data Extensions for outputs and errors, respectively.
