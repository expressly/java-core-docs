## Resources
### Banner-controller

Banner Controller

#### redirectBanner
```
GET /v2/banner/request/redirect
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|email|email|true|string||
|QueryParameter|campaignUuid|campaignUuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* */*

#### getBanner
```
GET /v2/banner/{merchantUuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|merchantUuid|merchantUuid|true|string||
|QueryParameter|email|email|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|BannerDetailResponse|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### addBanner
```
POST /v2/banner/create
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|BannerAddRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Campaign-controller

Campaign Controller

#### create
```
POST /admin/campaign/create
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|CampaignCreateRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|CampaignDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### search
```
POST /admin/campaign/search
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|CampaignSearchRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|PageDto«CampaignDto»|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### get
```
GET /admin/campaign/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|CampaignDto|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### addCustomers
```
POST /admin/campaign/{uuid}/customers/add
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|QueryParameter|excludeExisting|excludeExisting|false|boolean||
|FormDataParameter|emails|file|true|file||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|No Content|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* multipart/form-data

##### Produces

* */*

#### getMerchantAdmin
```
GET /admin/campaign/{uuid}/options
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|BodyParameter|request|request|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### addMerchantAdmin
```
POST /admin/campaign/{uuid}/options
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|BodyParameter|request|request|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* */*

#### getCampaignMetrics
```
GET /admin/campaign/{uuid}/customers/metrics
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|CampaignMetric array|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### update
```
POST /admin/campaign/{uuid}/update
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|BodyParameter|request|request|true|CampaignUpdateRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|CampaignDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getCampaignCustomers
```
GET /admin/campaign/{uuid}/customers
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* */*

### Data-controller

Data Controller

#### getStaticAgeData
```
GET /admin/data/age
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getStaticIndustryData
```
GET /admin/data/industry
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getStaticGenderData
```
GET /admin/data/gender
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getStaticPlatformVersionData
```
GET /admin/data/platform/{id}/version
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|id|id|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getStaticLocationData
```
GET /admin/data/location
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getStaticPlatformData
```
GET /admin/data/platform
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Event-log-controller

Event Log Controller

#### search
```
POST /admin/events/search
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|EventSearchRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|PageDto«EventLogDto»|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Merchant-plugin-controller

Merchant Plugin Controller

#### register
```
POST /v2/plugin/merchant
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|MerchantPluginRegisterRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|No Content|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### uninstall
```
DELETE /v2/plugin/merchant/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|204|No Content|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Merchant-portal-controller

Merchant Portal Controller

#### registerAtAdmin
```
POST /v2/merchant
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|MerchantCreateRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getMerchantAdminOptions
```
GET /v2/merchant/{uuid}/options
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|MerchantAdminResource|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### addMerchantAdminOptions
```
POST /v2/merchant/{uuid}/options
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|MerchantAdminSaveRequest||
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### searchMerchantOptions
```
POST /v2/merchant/search
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|request|request|true|MerchantAdminSearchRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Page«FullMerchant»|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getMerchantAdmin
```
GET /v2/merchant/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|QueryParameter|includeConnectionDetails|includeConnectionDetails|false|boolean||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### updateAtAdmin
```
PUT /v2/merchant/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|BodyParameter|request|request|true|MerchantCreateRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### uninstall
```
DELETE /v2/merchant/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|204|No Content|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getPingMerchant
```
GET /v2/merchant/{uuid}/ping
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### getMerchantApiKey
```
GET /v2/merchant/{uuid}/apikey
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Migration-controller

Migration Controller

#### getPopupHtml
```
GET /v2/migration/{uuid}
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* text/html

#### registerSuccessfulMigration
```
POST /v2/migration/{uuid}/success
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||
|QueryParameter|status|status|false|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* */*

#### migrate
```
GET /v2/migration/{uuid}/user
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Ping-controller

Ping Controller

#### dbReadPing
```
GET /admin/ping
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Test-extras-controller

Test Extras Controller

#### createCampaignLive
```
GET /support/campaign/create/live
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|takerUuid|takerUuid|true|string||
|QueryParameter|giverUuid|giverUuid|true|string||
|QueryParameter|couponCode|couponCode|true|string||
|QueryParameter|productId|productId|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### dbReadPing
```
GET /support/db/read/ping
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### returnInvoicesForEmail
```
GET /support/invoices/{campaignCustomerUuid}/get
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|campaignCustomerUuid|campaignCustomerUuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* text/plain

#### createFullCustomer
```
GET /support/create/migration
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* text/html

#### resetTestData
```
POST /support/test/{uuid}/reset
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|merchantUuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### createCustomerLive
```
GET /support/campaign/customer/create/live
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|email|email|true|string||
|QueryParameter|campaignUuid|campaignUuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### simplePing
```
GET /support/ping
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### dbWritePing
```
GET /support/test/merchant
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|merchantUrl|merchantUrl|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### createCustomer
```
GET /support/campaign/customer/create
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|email|email|true|string||
|QueryParameter|firstName|firstName|true|string||
|QueryParameter|campaignUuid|campaignUuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### dbWritePing
```
GET /support/db/write/ping
```

##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### createCampaign
```
GET /support/campaign/create
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|takerUuid|takerUuid|true|string||
|QueryParameter|couponCode|couponCode|true|string||
|QueryParameter|productId|productId|false|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

#### adminPingMerchant
```
GET /support/merchant/{uuid}/ping
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|uuid|uuid|true|string||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

### Xly-controller

Xly Controller

#### addCustomerToXly
```
POST /v2/xly/customer/add
```

##### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|customer|customer|true|CustomerCreateRequest||


##### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|SuccessMessageDto|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


##### Consumes

* application/json

##### Produces

* application/json

