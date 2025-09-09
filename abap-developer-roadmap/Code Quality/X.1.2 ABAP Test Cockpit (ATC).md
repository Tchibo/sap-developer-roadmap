#Intermediate 
The ATC enforces standards by ensuring compliance with policies such as coding conventions and best practices and by serving as an automated quality gate for transports. It centrally checks the objects contained in a transport against quality, performance, and security rules and can block the release or import in the event of critical findings. This enables early detection of errors and target-system incompatibilities, reduces risks and rework.

While it may be tempting to enable as many ATC rules as possible, doing so noticeably increases the runtime of transport checks and can impede throughput. Therefore, transport checks should focus on the most important aspects—those that are high-risk and difficult to change later. These include security and performance checks as well as global naming and API conflicts. A practical example is global variable names or identifiers that may already be used elsewhere and could later lead to conflicts or side effects.

> [!todo] Because ATC rules not enforced when transporting copies
> Clarify that running the ATC check manually ahead of transport release is important as ATC rules are not checked when transport of copies are deployed to the quality assurance system

It is recommended to manually run the ATC check variant before releasing the transport to reduce the number of issues at release time.

> [!todo] Refer to ATC practice at Tchibo
> Mention that all priority 1 and 2 findings needs to be fixed for a transport to be releaseable for transport to QA. Mention that an ATC person on call needs to approve/ reject exemption requests.

# Resources
#website [Central Quality Checking with the ATC | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/ba879a6e2ea04d9bb94c7ccd7cdac446/3f1a866ced26445cbfb8e1f896f86dfb.html?locale=en-US)
#website [Configuring ATC in a Consolidation System | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/ba879a6e2ea04d9bb94c7ccd7cdac446/73473fd593fc417ba7a6367423f1e535.html?locale=en-US)
#Article [Getting Started with the ABAP Test Cockpit for Dev... - SAP Community](https://community.sap.com/t5/application-development-and-automation-blog-posts/getting-started-with-the-abap-test-cockpit-for-developers/ba-p/13232141)
