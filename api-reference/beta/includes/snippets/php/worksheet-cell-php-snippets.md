---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);


$result = $graphServiceClient->drivesById('drive-id')->itemsById('driveItem-id')->workbook()->worksheetsById('workbookWorksheet-id')->cell(row={row},column={column})()->get();


```