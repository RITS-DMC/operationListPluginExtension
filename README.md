To begin, we need to clone projects:

- operationListExtensionProvider
- util

1. Clone the Repository:-
 - Clone the repository  inside your plugin project and path for the cloned Repositoryshould be like:- yourPlugin/webapp/operationListExtensionProvider.
 - Open and Identify data-name in your plugin’s index.html file. 
 - Identify the value of the data-name attribute (e.g., rits.custom.plugin.operationlistpluginextension). 
 This will be used in the upcoming search-and-replace operations

2. Search and Replace in the Cloned Folder :-
- Right click on the cloned folder operationlistpluginextensionExtensionProvider. 
- Select "Find in Folder". - Perform the following search-and-replace operations:
  Replace 1:
 - Use this in the Search field: rits.custom.plugin.operationlistpluginextension 
 - Use this in the replace field: with your namespace from the index.html file
 - Click "Replace All Icon". 
  Replace 2: 
 - Use this in the Search field: rits/custom/plugin/operationlistpluginextension 
 - Convert your data-name (e.g., rits.custom.plugin.operationlistpluginextension) to a folder path by replacing dots (.) with slashes (/)(e.g., rits/custom/plugin/operationlistpluginextension). 
 - Use this in the replace field: with your namespace from the index.html file - Click "Replace All Icon".

3. Update component.json :-
- Open the file: yourPlugin/webapp/designer/component.json 
- Inside the extensions list, add an entry for the plugin with the following structure: after the components: rits/custom/plugin/operationlistpluginextension:

  <img width="1123" height="291" alt="image" src="https://github.com/user-attachments/assets/bcbe6fe0-fc86-4928-ade2-9f417ab87bad" />

**Important Note: After pasting the above JSON:
      i. Ensure provider matches the correct plugin path. It should be: <data-name with slashes>/operationListExtensionProvider/ExtensionProvider. 
      For example, if your data-name is rits.custom.plugin.operationlistpluginextension, then it becomes:rits/custom/plugin/operationlistpluginextension/operationListExtensionProvider/ExtensionProvider.
      ii. Ensure pods and plants are updated based on your actual deployment targets. Replace "pod1", "pod2" and "plant1", "plant2" with real values.**
  
Navigate to: dmc-coreplugin-extension > plugins > webapp > utils and repeat the same setup process for this utils project as well
  
4. Build and Deploy Your Plugin :-
- Build your plugin project using your standard build process. 
- Deploy it to your target environment.

5. Verify the Result 
- Navigate to the relevant section in your app. 
- Verify that the extension is functioning correctly and is visible for the specified pods and plants defined in the component.json file.
