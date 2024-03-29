# Introduction
In this step, you will setup two SAP Build Work Zone, standard edition Services in two different regions, which can be from the same or different hyperscalers.

SAP Build Work Zone, standard edition service enables organizations to establish a central point of access to SAP (e.g. SAP S/4HANA), custom-built, and third-party applications and extensions, both on the cloud and on-premise.

# Setup SAP BTP Build Work Zone, standard edition Service
1.  If you haven't used SAP Build Work Zone, standard edition Service yet, please go to the SAP Discovery Center Mission [Establish a central entry point with SAP Build Work Zone, standard edition service](https://discovery-center.cloud.sap/missiondetail/3283/3378).

2.  Go to your [SAP BTP Cockpit](https://cockpit.us10.hana.ondemand.com/) and make sure that you have two subaccounts in your global account. In this case, we have both of them on Azure - one in West Europe (Australia(Sydney), AP20), one in West US (WA, US20). If you don't have them yet, click on **New Subaccount** in order to create a new subaccount.
    
    ![New subaccount](./images/01.png)
   
   > NOTE: If you already have two subaccounts in regions where the SAP Build Work Zone, standard edition Service is available, you don't necessarily need to create separate accounts for this tutorial. You can simply reuse the existing ones if you want.

3. Provide the necessary details for the new SAP BTP subaccount. 

   - Provide a subaccount name. 
   - Optional: Provide a description. 
   - Select Provider **Azure**. 
   - Select Australia(Sydney) or another region, where the SAP Build Work Zone, standard edition service is available. The [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/launchpad-service?region=all&tab=service_plan) shows the available regions.  
   - Enter a Subdomain for your subaccount. This subdomain becomes part of the URL for accessing applications that you subscribe to from this subaccount.
   - Optional: If your subaccount is to be used for productive purposes, select the **Used for production** option.

   ![Subaccount details](./images/02.png)

4. **Save** your changes.
   
   **A new tile appears on the global account page with the subaccount details.**
5. Open the Sub Account and navigate to **Overview** > **Cloud Foundry Environment**.

6. Click **Create Space**, enter the required information and click **Create**.
    ![Subaccount details](./images/space.png)

7. Make sure that you have two subaccounts in regions where the Build Work Zone, standard edition service is available. If you don't have two subaccounts for the SAP Build Work Zone, standard edition service yet, create another subaccount as explained in Steps 3-6.

8. In the navigation area of the global account, choose Entitlements > Entity Assignments and select the subaccounts in which you want to set up SAP Build Work Zone, standard edition service. 
   ![Entity Assignments-Sub account Selection](./images/03.png)

9. Go to **Configure Entitlements** followed by **Add Service Plans** for the first subaccount.
   ![Entity Assignments-Add Service Plan](./images/04.png)

10. Add the following entitlements: 

    - Build Work Zone, standard edition service (Service Plan: standard (Application))
    - Custom Domain service (Service Plan: custom_domains, standard (Application))

11. Click on **Save** to save the changes.
    
12.   **Repeat steps 8-11 for the second subaccount.**

13.   Go to **Subaccounts** and navigate to the first subaccount for SAP Build Work Zone, standard edition service.

14.   In the navigation area of the subaccount, choose **Services > Service Marketplace** and search for **Build Work Zone, standard edition Service**. Choose **Create** on the overview page.
      ![Adding Build Work Zone, standard edition Service](./images/05.png)

15.   In the **New Instance or Subscription** dialog box, select an available **Plan** and finish with **Create**. Wait for the subscription to complete successfully.

16.    In the navigation area of the subaccount, choose **Security > Role Collections** and search for **Launchpad_Admin**. 
      ![Launchpad Role](./images/06.png)

17. Click on the Role Collection itself and **Edit**.

    ![Launchpad role collection edit](./images/07.png) 
    
18. Enter the email address for your SAP BTP user in the **User** section and **Save** your changes. Make sure that your user appears in the User section after you have saved the changes.

19. Go back (using the browser function, for instance) to the **Instances and Subscriptions** page. Select the **Launchpad Service** Subscription and choose **Go to Application** to launch the Build Work Zone, standard edition service.

    ![Go to Build Work Zone, standard edition Service](./images/08.png) 

20. You now have the access to Build Work Zone, standard edition Site Manager.

    ![Build Work Zone, standard edition Service](./images/09.png)

21.   **Repeat steps 13-19 for the second subaccount**.

---

You have successfully configured two SAP BTP subaccounts and subscribed to the SAP Build Work Zone, standard edition Service in each of the subaccounts.

Congratulations!