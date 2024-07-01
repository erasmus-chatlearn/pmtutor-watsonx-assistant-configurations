# Instructions for creating a PMTutor watsonx Assistant
This file provides you with detailed step-by-step instructions to help you create your PMTutor watsonx Assistant. 
Please make sure the prerequisites are met before proceeding the setup.

## Prerequisites
* PMTutor databases (Instructions coming soon!)
* PMTutor webhook instance: You can find the source code at [pmtutor-webhook](https://github.com/erasmus-chatlearn/pmtutor-webhook)
* IBM watsonx Assistant Plus
* IBM IAM user with Operator and Manager access rights to the watsonx service 
* OpenAI API key

## Step 1: Create a new watsonx Assistant
If you have not created any watsonx Assistant before in your IBM subscription, 
the watsonx Assistant view will guide you through creating your first assistant.

![Welcome View: Create](./images/create-watsonx-assistant-first-time-1.png)
*The welcome view for creating your first watsonx Assistant*

![Welcome View: Personalize](./images/create-watsonx-assistant-first-time-2.png)
*Provide required information for personalization&mdash;you can update your settings later*

![Welcome View: Customize](./images/create-watsonx-assistant-first-time-3.png)
*You can upload an avatar set the UI styles for your assistant*

![Welcome View: Preview](./images/create-watsonx-assistant-first-time-4.png)
*Click "Create" button to complete the steps*

![Assistant View](./images/create-watsonx-assistant-first-time-5.png)
*You should see your assistant view after it has been successfully created*

### Creating another watsonx Assistant
You might want to create another assistant later for different purposes. The steps for creating another one is simpler.

You can find the option "Create New +" from the dropdown list in the top menu bar, when
you click on the name of the current assistant.
![Button for creating another assistant](./images/create-another-watsonx-assistant-1.png)
*Find "Create New +" option from the top menu bar*

![Form for creating another assistant](./images/create-another-watsonx-assistant-2.png)
*Fill up the required fields and click on "Create assistant"*

## Step 2: Activate dialog
The screenshots below show how to navigate to Assistant settings to activate dialog.

![Navigate to Assistant settings](./images/activate-dialog-1.png)
*Assistant settings is located in the bottom of the side bar menu*

![Go to Dialog section](./images/activate-dialog-2.png)
*Click on Activate dialog*

![Confirm dialog activation](./images/activate-dialog-3.png)
*Click on another Activate dialog button to confirm the activation"*

## Step 3: Upload dialog skill
Navigate to Dialog view by hovering over the sidebar menu and clicking on Dialog.

![Dialog view](./images/upload-dialog-1.png)
*Click on Upload / Download in Options*

Upload configurations/pm-tutor-v2-dialog-v44.json.
![Upload dialog skill view](./images/upload-dialog-2.png)
*Click "Upload" button*

![Confirm uploading](./images/upload-dialog-3.png)
*Confirm uploading*

## Step 4: Configure webhook settings
The webhook URL is removed from the dialog skill json in this repository. Please use the URL of your webhook instance.

You can find webhook settings from Options in Dialog view.
![Webhook settings](./images/webhook-settings.png)
*Provide the URL of your webhook*

## Step 5: Upload action skill
Navigate to Actions view by hovering over the sidebar menu and clicking on Actions. The screenshots below show the rest
of steps for uploading action skill.

![Actions view](./images/upload-action-1.png)
*Go to Global settings by clicking on the gear icon in the top-right corner*

![Actions > Global settings view](./images/upload-action-2.png)
*Click on Upload/Download from the tabs under the heading Global settings*

![Actions > Global settings > Upload/Download view](./images/upload-action-3.png)
*Upload configurations/pm-tutor-v2-action-v44.json using the Upload section*

![Confirm action skill uploading](./images/upload-action-4.png)
*Confirm action skill uploading*

## Step 6: Create and add OpenAI extension
The screenshots below show how to create and add OpenAI extension to your assistant.

![Navigate to Integrations](./images/create-oai-extension-1.png)
*Hover over the sidebar menu and select Integrations*

![Build a custom extension](./images/create-oai-extension-2.png)
*Go to Extensions section and click "Build custom extension"*

![Custom extension start view](./images/create-oai-extension-3.png)
*Click Next*

![Custom extension basic info](./images/create-oai-extension-4.png)
*Provide a name of your extension*

![Custom extension import API document](./images/create-oai-extension-5.png)
*Select and upload configurations/openai-openapi.json*

![Custom extension review](./images/create-oai-extension-6.png)
*Click Finish*

After successfully creating the extension, you should see the name of your extension in the Extensions section.
Click Add to integrate it to your Draft environment.
![Created extension](./images/create-oai-extension-7.png)

![Confirm the integration](./images/create-oai-extension-8.png)
*Click Add again to confirm the integration*

### Configure custom extension for an assistant environment

![Configure the extension for Draft environment](./images/create-oai-extension-9.png)
*Click Next*

![Provide OpenAI platform API key](./images/create-oai-extension-10.png)
*Copy and paste your OpenAI Platform API key to Token field*

![Review custom extension configuration](./images/create-oai-extension-11.png)
*Click Finish*

After successfully integrating to your Draft environment, you should see your OpenAI platform extension in 
Environments > Draft.
![Draft environment](./images/create-oai-extension-12.png)

You should also integrate the extension to the Live environment by clicking on Live tab in Environments and then "Add" 
in the OpenAI extension.
![Add extension to Live environment](./images/create-oai-extension-13.png)

It will walk you through the previous steps in [configure custom extension](#configure-custom-extension-for-an-assistant-environment).



