# Instructions

* Please make a copy of this template. **Once you have your own draft, you can delete this section**.
* The following template includes information required in all PagerDuty integration guides.
* Instructions in ***bold italics*** are intended to provide guidance or examples, and should be deleted once you’ve added your content.
* If your integration does not follow the same flow as what we’ve provided below (e.g. steps begin in your tool’s UI as opposed to the PagerDuty UI, etc.), feel free to make the changes you need to reflect the flow of the integration.
----

# PagerDuty + ***[PARTNER-NAME]*** Integration Benefits

***In a bulleted list, describe the benefits of integrating your tool with PagerDuty. Include specific details on how your tool interacts with PagerDuty.
Use our [Datadog guide](https://www.pagerduty.com/docs/guides/datadog-integration-guide/) as an example:***
* ***Notify on-call responders based on alerts sent from Datadog.***
* ***Send enriched event data from Datadog including visualizations of the metric/service-level indicator (SLI) that triggered the event.***
* ***Create high and low urgency incidents based on the severity of the event from the Datadog event payload.***
* ***Incidents and escalations are synchronized across both PagerDuty and Datadog as they update.***
* ***Incidents will automatically resolve in PagerDuty when the metric in Datadog returns to normal with bidirectional synchronization.***

# How it Works
***In this section, write out the basic functionality of the integration with specific details on how events are transformed into PagerDuty incidents. What happens when your tool sends events to PagerDuty (and vice versa, if applicable)?
Use the current Datadog guide as an example:***
* ***Datadog metrics that fall outside of a designated range will send an event to a service in PagerDuty. Events from Datadog will trigger a new incident on the corresponding PagerDuty service, or group as alerts into an existing incident.***
* ***Once the metric has returned to its designated range, a resolve event will be sent to the PagerDuty service to resolve the alert, and associated incident on that service.***

# Requirements
***If there are requirements that user will need prior to completing the integration, list them here.
Use the current Datadog guide as an example:***
* ***PagerDuty integrations require an Admin base role for account authorization. If you do not have this role, please reach out to an Admin or Account Owner within your organization to configure the integration.***

# Integration Walkthrough
## In PagerDuty

***If your integration works with Global Event Routing, you can optionally include the following section:***

***There are two ways to integrate with PagerDuty: via Global Event Routing or on a PagerDuty Service.***
***If you are adding this integration to an existing PagerDuty service, please skip to the Integrating with a PagerDuty Service section of this guide.***

### ***Integrating With Global Event Routing***
***Integrating with Global Event Routing enables you to route events to specific services based on the payload of the event from your tool. If you would like to learn more, please visit our article on Global Event Routing.***
***1. From the Configuration menu, select Event Rules.***
***2. On the Event Rules screen, click on the arrow next to Incoming Event Source to display the Integration key information. Copy your Integration Key. This is the same integration key you will use for any other tool you want to integrate with using event rules. When you have finished setting up the integration in your tool, you will return to this interface to specify how to route events from your tool to services in PagerDuty.***

![](https://pdpartner.s3.amazonaws.com/ig-template-incoming-event-source-key.png)

### Integrating With a PagerDuty Service
1. From the **Configuration** menu, select **Services**.
2. There are two ways to add an integration to a service:
   * **If you are adding your integration to an existing service**: Click the **name** of the service you want to add the integration to. Then, select the **Integrations** tab and click the **New Integration** button.
   * **If you are creating a new service for your integration**: Please read our documentation in section **Configuring Services and Integrations** and follow the steps outlined in the **Create a New Service** section, selecting ***[PARTNER-NAME]*** as the **Integration Type** in step 4. Continue with the In  ***[PARTNER-NAME]***  section (below) once you have finished these steps.
3. Enter an **Integration Name** in the format `monitoring-tool-service-name` (e.g.  ***[PARTNER-NAME]***-Shopping-Cart) and select  ***[PARTNER-NAME]***  from the Integration Type menu.
4. Click the **Add Integration** button to save your new integration. You will be redirected to the Integrations tab for your service.
5. An **Integration Key** will be generated on this screen. Keep this key saved in a safe place, as it will be used when you configure the integration with  ***[PARTNER-NAME]***  in the next section.
![](https://pdpartner.s3.amazonaws.com/ig-template-copy-integration-key.png)

## In ***[PARTNER-NAME]***

***Outline the configuration steps in your tool starting here.***

# How to Uninstall

***Add instructions here on how to uninstall your app (e.g. going to the profile page to revoke access vs. deleting the integration key or extension).***
