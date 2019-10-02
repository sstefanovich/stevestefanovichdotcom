Title: Hindsight - WEBSITE_LOAD_CERTIFICATES
Published: 7/30/2019
Tags: [Azure, Hindsight]
---
Many times as developers, it's one missing piece that trips us up. Hours and even days can be wasted. It might be a bug that seems completely obvious after a a bit of [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging), the eternal nemesis that is permissions, or a missing piece of configuration data. In this ongoing series, I'm calling "Hindsight", I'll cover something that tripped me up. If these entries serve only as a painful reference for future me, then I have succeeded. 

# Hindsight: WEBSITE_LOAD_CERTIFICATES
In today's installment, we have the tale of your humble narrator attempting to simply load a private certificate for use as a secret in an Azure Function. The scenario is an Azure Function in Tenant A attempting to add a list item to SharePoint Online hosted in Tenant B. Let's Review:

- Certificate uploaded to Private Keys, SSL section of Platform Settings for the Function (try finding that in a hurry) in Tenant A? Check
- Application registered in Azure AD in Tenant B? Check
- Certificate uploaded to Certificates & secrets in application registration in Tenant B? Check 
- Code loading certificate and working locally? Double check, it always works locally

Much head scratching ensues. A co-worker is finally consulted and after another round of head scratching, the aha! Did you set [WEBSITE_LOAD_CERTIFICATES](https://docs.microsoft.com/en-us/azure/app-service/app-service-web-ssl-cert-load) in the configuration of the function in Tenant A? No, no I did not but I will next time!