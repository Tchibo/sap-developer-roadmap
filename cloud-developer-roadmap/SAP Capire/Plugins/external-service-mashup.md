---
tags:
  - nodejs
  - backend
  - external-services
  - advanced
links:
  - "[[Add external services]]"
  - "[[Plugin]]"
source:
aliases:
  - "@sap/external-service-mashup"
---
After integrating an [[OData]] service from an external system (see [[Add external services|Guide]]), you need to implement a so-called service mashup if one of the imported entities is used as an association. In a service mashup, the default navigation provided by the [[SAP Capire]] framework is adapted so that, whenever an association to an external entity is resolved, the data is retrieved from the connected external service rather than from the local service.

For more information about the supported scenarios and applicable restrictions for service mashups, please refer to the official documentation.

**Example Implementation of a Service Mashup**
```ts
import cds from '@sap/cds';
import MashupHandler from '@sap/external-service-mashup';

import { Books, I_Supplier_VH } from '#cds-models/BookshopService';

export class BookshopService extends cds.ApplicationService {
  private mashupHandler = new MashupHandler();

  async init() {
    this.mashupHandler.init();

    // Initialize the service mashup for the desired remote entity
    this.mashupHandler.init(I_Supplier_VH);

    // Resolve navigation to the external entity whenever the association is requested
    this.on('READ', Books, async (req, next) => {
      const result = await this.mashupHandler.handle(req, next);
      return result;
    });
  }
}
```

> [!Tip] **Credits**
> Special thanks to [martin-kl](https://community.sap.com/t5/user/viewprofilepage/user-id/6532) for [the suggestion](https://community.sap.com/t5/user/viewprofilepage/user-id/6532)für [den Hinweis](https://community.sap.com/t5/technology-q-a/cap-cds-service-to-service-connection-access-to-compositions/qaa-p/14144275/highlight/true#M4918953) regarding the `@sap/external-service-mashup` package, which enables easy and efficient implementation of service mashups.

**Sources**
- [SAP Capire - Mashing up with Remote Services](https://cap.cloud.sap/docs/guides/using-services#mashing-up-with-remote-services)
- [SAP Capire - Handle Mashups with Remote Services](https://cap.cloud.sap/docs/guides/using-services#mashing-up-with-remote-services)