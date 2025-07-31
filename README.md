## 📚 Table of Contents

1. [🚀 How to Configure Copado Robotic Testing and Copado CI/CD](#how-to-configure-copado-robotic-testing-and-copado-cicd)  
2. [🖼️ Preview](#preview)  
3. [📦 Prerequisites](#prerequisites)  
4. [🛠️ Step-by-Step Setup](#step-by-step-setup)  
   - [🔐 Step 1: Create a Personal Access Key](#step-1-create-a-personal-access-key)  
   - [🔄 Step 2: Connect CRT to Copado CI/CD](#step-2-connect-crt-to-copado-cicd)  
   - [🔗 Step 3: Link Project](#step-3-link-project)  
5. [🎉 You're Done!](#youre-done)  
6. [⚠️ Troubleshooting](#troubleshooting)

# 🚀 How to Configure Copado Robotic Testing and Copado CI/CD

This guide walks you through setting up the connection between your **Copado CI/CD instance** and **Copado Robotic Testing (CRT)** organization.

---

## 🖼️ Preview

Here’s what we’re going to build:

<div style="border:2px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/copado-robotics-home.png" alt="App Screenshot" style="max-width: 100%;">
</div>

---

## 📦 Prerequisites

Before you begin, make sure you have the following ready:

- ✅ Access to a **Copado CI/CD** org with the **Copado Robotics** package installed.
- ✅ Access to a **Copado Robotic Testing** project with at least one test job configured.
- ✅ A **Personal Access Key** from CRT.

---

## 🛠️ Step-by-Step Setup

### 🔐 Step 1: Create a Personal Access Key

**1.** Go to your **Copado Robotic Testing** project where test jobs are configured.  
**2.** Click on your **profile icon** and select **Personal Access Keys**.  
**3.** Click on **Generate Key**.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Personal-Access-Key.png" alt="Generating Access Key">
</div>

**4.** Provide a **key name**, choose the **expiration (in days)**, and click **Save**.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Generate-Access-Key.png" alt="Generate Key">
</div>

**5.** A pop-up will display your access key. **Copy and store it safely** — it will not be shown again.

> ⚠️ This key is sensitive. Do not share it publicly. The example below is a dummy key for demonstration purposes:

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Key-Example.png" alt="Access Key Example">
</div>

---

### 🔄 Step 2: Connect CRT to Copado CI/CD

**1.** Go back to your **Copado CI/CD** org.  
**2.** In the **App Launcher**, search for **Copado Robotics** and click on it.  
**3.** In the below page click on the **Add Connection** button.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Add-Connection.png" alt="Add-Connection">
</div>

**4.** This will open up this pop-up below, with some fields auto populated, here add your personal access key and click **Next** button.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Add-Connection-1.png" alt="Add-Connection-1">
</div>

**5.** After clicking **Next** button, below pop-up will show a new screen. As per the instructions shown in the pop-up, go to the Named Credentials (automatically created by Copado) and enable the **Allow Callouts** option.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Add-Connection-2.png" alt="Add-Connection-2">
</div>

**6.** After enabling the callout option, come back to the pop-up and click the **Test Connection** button.  
If all the steps mentioned earlier are done correctly, it will show **Connection tested successfully**. Then click on the **Finish-Setup** button.

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Finish-Setup.png" alt="Finish-Setup">
</div>

---

### 🔗 Step 3: Link Project

**1.** Post completion of Step-2:

<div style="border: 3px solid #87ceeb; border-radius: 8px; overflow: hidden; width: fit-content;">
  <img src="Files/Copado-CRT-Setup/Link-Project.png" alt="Link-Project">
</div>

**2.** Click **Link Project** beside the connection record.  
**3.** Select the CRT project from the dropdown and click **Save**.  
**4.** Your CRT project is now linked with your Copado CI/CD org and is ready for automated test execution.

---

## 🎉 You're Done!

You’ve successfully:

- Generated a Personal Access Key  
- Connected Copado CI/CD with Copado Robotic Testing  
- Linked a project for automated testing

You’re now ready to trigger and monitor robotic test runs directly from your CI/CD pipeline!

---

## ⚠️ Troubleshooting

- **Issue:** Test Connection fails.  
  **Solution:** Double-check that the Personal Access Key is correct and not expired. Also verify that the Named Credential's **Allow Callouts** option is enabled.

- **Issue:** CRT project not appearing in dropdown.  
  **Solution:** Make sure your CRT user has access to the project and that the test job is properly configured.

For additional help, refer to Copado documentation or contact your administrator.
