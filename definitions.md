## Definitions
### BannerAddRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|bannerImageUrl||false|string||
|campaignUuid||false|string||


### BannerDetailResponse
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|bannerImageUrl||false|string||
|migrationLink||false|string||


### CampaignCreateRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|campaignEndDate||false|LocalDate||
|campaignStartDate||false|LocalDate||
|couponCode||false|string||
|giverUuid||false|string||
|productId||false|string||
|takerUuid||false|string||


### CampaignMetric
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|count||false|integer (int64)||
|status||false|enum (READY, ACCESSED, MIGRATED, EXISTING_USER)||
|statusGiver||false|enum (DELETED, EXISTS, NEW, NOT_CHECKED, PENDING)||
|statusTaker||false|enum (DELETED, EXISTS, NEW, NOT_CHECKED, PENDING)||


### CampaignSearchRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|couponCode||false|string||
|fromDate||false|LocalDate||
|giverUuid||false|string||
|onlyActive||false|boolean||
|page||false|integer (int32)||
|pageSize||false|integer (int32)||
|productId||false|string||
|sortDescending||false|boolean||
|sortOrder||false|string array||
|takerUuid||false|string||
|toDate||false|LocalDate||


### CampaignUpdateRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|campaignActive||false|boolean||
|campaignEndDate||false|LocalDate||


### CustomerCreateRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|addressFirstLine||false|string||
|email||false|string||
|firstName||false|string||
|lastName||false|string||
|phoneNumber||false|string||
|postCode||false|string||


### EventSearchRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|campaignUuid||false|string||
|emailAddress||false|string||
|excludeCustomerEvents||false|boolean||
|merchantUuid||false|string||
|page||false|integer (int32)||
|pageSize||false|integer (int32)||
|sortDescending||false|boolean||
|sortOrder||false|string array||


### FullMerchant
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|details||false|MerchantAdminResource||
|merchant||false|Merchant||


### IndexValuePair
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|index||false|integer (int64)||
|value||false|string||


### Map«string,List«Map«string,object»»»
### Map«string,Map«string,object»»
### Map«string,object»
### Map«string,string»
### Merchant
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|active||false|boolean||
|id||false|integer (int64)||
|policyUrl||false|string||
|shopImageUrl||false|string||
|shopName||false|string||
|shopUrl||false|string||
|status||false|enum (ACTIVE, UNINSTALLED, NOT_CONFIGURED, DELETED)||
|termsAndConditionsUrl||false|string||
|uuid||false|string||


### MerchantAdminOptionsRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|address1||false|string||
|address2||false|string||
|businessModel||false|string||
|country||false|IndexValuePair||
|newsletterCustomers||false|integer (int64)||
|phone||false|string||
|postCode||false|string||
|registeredCustomers||false|integer (int64)||
|state||false|string||


### MerchantAdminResource
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|fees||false|object||
|industries||false|Map«string,object» array||
|locations||false|Map«string,object» array||
|options||false|object||
|platform||false|object||
|relationships||false|object||
|roles||false|string array||


### MerchantAdminSaveRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|fees||false|object||
|industries||false|Map«string,object» array||
|locations||false|Map«string,object» array||
|options||false|MerchantAdminOptionsRequest||
|platform||false|object||
|relationships||false|object||
|roles||false|string array||
|uuid||false|string||


### MerchantAdminSearchRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|ages||false|string array||
|genders||false|string array||
|industries||false|string array||
|locations||false|string array||
|roles||false|string array||
|shopNameHint||false|string||


### MerchantCreateRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|apiBaseUrl||false|string||
|pluginVersion||false|string||
|policyUrl||false|string||
|shopImageUrl||false|string||
|shopName||false|string||
|shopUrl||false|string||
|termsAndConditionsUrl||false|string||


### MerchantPluginRegisterRequest
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|apiBaseUrl||false|string||
|apiKey||false|string||
|pluginVersion||false|string||


### Page«FullMerchant»
|Name|Description|Required|Schema|Default|
|----|----|----|----|----|
|content||false|FullMerchant array||
|first||false|boolean||
|last||false|boolean||
|number||false|integer (int32)||
|numberOfElements||false|integer (int32)||
|size||false|integer (int32)||
|sort||false|Sort||
|totalElements||false|integer (int64)||
|totalPages||false|integer (int32)||


