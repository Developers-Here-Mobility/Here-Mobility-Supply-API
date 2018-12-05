marketplace/public/grpc/supply_handler/v1/supply_handler_rides_service.proto-REST
=================================================================================
**Version:** version not set

### /dispatch.rides.v1/offer_requests
---
##### ***POST***
**Summary:** Request ride offers from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1GetSimpleRideOffersRequest](#v1getsimplerideoffersrequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1SimpleRideOffers](#v1simplerideoffers) |

### /dispatch.rides.v1/rides
---
##### ***POST***
**Summary:** Create a ride with the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CreateSimpleRideRequest](#v1createsimpleriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1CreateSimpleRideResponse](#v1createsimplerideresponse) |

### /dispatch.rides.v1/rides/{ride_id}/demander_cancel
---
##### ***POST***
**Summary:** Update the supplier that the demander has cancelled the ride.

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1DemanderCancelRideRequest](#v1demandercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1DemanderCancelRideResponse](#v1demandercancelrideresponse) |

### /dispatch.rides.v1/rides/{ride_id}/status
---
##### ***GET***
**Summary:** Request the latest status of the ride from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| supplier_id | query | Marketplace generated supplier id. | No | string |
| environment_type | query | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1SupplierRideStatus](#v1supplierridestatus) |

### /supply.rides.v1/rides/{ride_id}/eta_update
---
##### ***POST***
**Summary:** Update the marketplace that estimated time to arrival to the origin and and to destination has changed
Recommended to update only when there is a major change (1 minute at least)

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideEtaUpdate](#v1rideetaupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/location_update
---
##### ***POST***
**Summary:** Update the marketplace that the vehicle location has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideLocationUpdate](#v1ridelocationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/pickup_and_destination_update
---
##### ***POST***
**Summary:** Update the marketplace that the meeting pickup and destination points changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RidePickupAndDestinationUpdate](#v1ridepickupanddestinationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/price_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride price has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RidePriceUpdate](#v1ridepriceupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/requested_pickup_time_update
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideRequestedPickupTimeUpdate](#v1riderequestedpickuptimeupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/status_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride status changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1SupplierRideStatusUpdate](#v1supplierridestatusupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/supplier_cancel
---
##### ***POST***
**Summary:** Update the marketplace that the assigned supplier has cancelled the ride

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1SupplierCancelRideRequest](#v1suppliercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/vehicle_and_driver_update
---
##### ***POST***
**Summary:** Update the marketplace that the assigned vehicle and driver have changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideVehicleAndDriverUpdate](#v1ridevehicleanddriverupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### Models
---

### DemanderCancelRideRequestPassengerCancelReasonCategory  

- UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVER_NO_SHOW: Driver did not show up.
 - PRICE_CHANGED: Ride price changed.
 - ETA_CHANGED: Ride ETA changed.
 - UNSUITABLE_VEHICLE: Ride vehicle is not suitable.
 - DRIVER_BEHAVED_INAPPROPRIATELY: Driver behaved inappropriately.
 - CHANGED_MY_PLANS: Passenger changed plans.
 - OTHER_PASSENGER_CANCEL_REASON_CATEGORY: Other.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| DemanderCancelRideRequestPassengerCancelReasonCategory | string | - UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVER_NO_SHOW: Driver did not show up.
 - PRICE_CHANGED: Ride price changed.
 - ETA_CHANGED: Ride ETA changed.
 - UNSUITABLE_VEHICLE: Ride vehicle is not suitable.
 - DRIVER_BEHAVED_INAPPROPRIATELY: Driver behaved inappropriately.
 - CHANGED_MY_PLANS: Passenger changed plans.
 - OTHER_PASSENGER_CANCEL_REASON_CATEGORY: Other. |  |

### SupplierCancelRideRequestSupplierCancelReasonCategory  

- UNKNOWN_SUPPLIER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVERS_UNAVAILABLE: No available drivers for ride.
 - PASSENGER_NO_SHOW: Passenger did not show up for the ride.
 - PASSENGER_REQUESTED_TO_CANCEL: Passenger requested to cancel the ride.
 - VEHICLE_MALFUNCTION: Vehicle mulfunction.
 - HEAVY_TRAFFIC: Heavy traffic.
 - OTHER_SUPPLIER_CANCEL_REASON_CATEGORY: Other cancellation cetegory.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| SupplierCancelRideRequestSupplierCancelReasonCategory | string | - UNKNOWN_SUPPLIER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVERS_UNAVAILABLE: No available drivers for ride.
 - PASSENGER_NO_SHOW: Passenger did not show up for the ride.
 - PASSENGER_REQUESTED_TO_CANCEL: Passenger requested to cancel the ride.
 - VEHICLE_MALFUNCTION: Vehicle mulfunction.
 - HEAVY_TRAFFIC: Heavy traffic.
 - OTHER_SUPPLIER_CANCEL_REASON_CATEGORY: Other cancellation cetegory. |  |

### VehicleVehicleType  

 - UNKNOWN: Default value - unknown vehicle type.
 - STANDARD: Standard vehicle.
 - LIMO: Limousine.
 - VAN: Van.
 - OTHER: Other known type - not specified.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| VehicleVehicleType | string |  - UNKNOWN: Default value - unknown vehicle type.
 - STANDARD: Standard vehicle.
 - LIMO: Limousine.
 - VAN: Van.
 - OTHER: Other known type - not specified. |  |

### commonv1Location  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| point | [v1Point](#v1point) | geographic coordinates (latitude, longtitude). | No |
| address | [v1Address](#v1address) | description, state and zip code are optional, rest are mandatory. | No |
| place | [v1Place](#v1place) | Optional. Place information of the location. | No |
| free_text | string | Street address in a free text format. | No |

### protobufUInt32Value  

Wrapper message for `uint32`.

The JSON representation for `UInt32Value` is JSON number.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| value | long | The uint32 value. | No |

### v1Address  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| country | string | Localized country name. | No |
| country_code | string | ISO 3166-alpha-3 country code. | No |
| state | string | State (first subdivision level below the country, if relevant). | No |
| county | string | County (second subdivision level below the country, if relevant). | No |
| city | string | City/town. | No |
| district | string | District (subdivision level below the city). | No |
| sub_district | string | Sub-district (subdivision level below the district; e.g. commonly used in IND). | No |
| street | string | Street name. | No |
| house_number | string | House number; depending on regional characteristics, can also be house name. | No |
| postal_code | string | Postal code (zipcode). | No |
| building_name | string | Building name; e.g. commonly used in HKG. | No |
| line | [ string ] | Formatted address lines. | No |

### v1CreateSimpleRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace if of the supplier for which we want to create the ride. | No |
| ride_id | string | Marketplace generated ride id which will be used to identify this ride. | No |
| ride_details | [v1SimpleRideDetails](#v1simpleridedetails) | Details of the ride creation request. | No |
| demander_id | string | additional fields for reporting and GDPR functionality. | No |
| demander_user_id | string |  | No |
| demander_product_id | string |  | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1CreateSimpleRideResponse  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| accepted_and_looking_for_driver | boolean (boolean) | Return true if ride was accepted and supplier is looking for a driver, or false if the ride is rejected. This call should return quickly and not wait for human confirmation. | No |
| pickup_eta | [v1UnixTime](#v1unixtime) | Estimated time of arrival to pickup. | No |
| booking_estimated_price | [v1Price](#v1price) | Estimated price. | No |

### v1DemanderCancelRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| cancel_reason | string | Cancellation reason. | No |
| cancel_reason_category | [DemanderCancelRideRequestPassengerCancelReasonCategory](#demandercancelriderequestpassengercancelreasoncategory) | Cancellation reason category. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1DemanderCancelRideResponse  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| cancel_accepted | boolean (boolean) | true if cancellation went through, false it if ride cannot be cancelled. TBD: cancel and pay fee. | No |
| cancel_reason | string | in case cancellation failed, a textual reason explaining the cause. | No |

### v1DriverDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| driver_id | string | Mandatory. Unique Id of the driver in the dispatcher system. | No |
| name | string | Mandatory. Full name of the driver, in English. | No |
| phone | string | Mandatory. Phone number though which the driver is reachable. | No |
| picture_url | string | URL of a driver photo. | No |
| driving_license_id | string | Mandatory in some jurisdictions. License id of the driver. | No |

### v1Empty  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1Empty | object |  |  |

### v1EnvironmentType  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1EnvironmentType | string |  |  |

### v1GetSimpleRideOffersRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| request_id | string | Unique request id generated by the marketplace. | No |
| supplier_id | string | Marketplace ID of the supplier from which we want offers. | No |
| pickup | [commonv1Location](#commonv1location) | Origin of the ride (pickup location). | No |
| destination | [commonv1Location](#commonv1location) | Destination of the ride (dropoff location). | No |
| constraints | [v1SimpleRideBookingConstraints](#v1simpleridebookingconstraints) | Constraints represent the requested ride parameters. | No |
| pickup_time | [v1UnixTime](#v1unixtime) | Pickup time. | No |
| passenger_note | string | Free-text comments by the passenger. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1PassengerDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | Full name of the passenger. | No |
| phone_number | string | Phone number in full international format. | No |
| photo_url | string | Optional URL. | No |

### v1PaymentFlow  

- OFFLINE_PAYMENT: Offline payment flow is used.
 - ONLINE_PAYMENT: Online payment flow is used.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1PaymentFlow | string | - OFFLINE_PAYMENT: Offline payment flow is used.
 - ONLINE_PAYMENT: Online payment flow is used. |  |

### v1Place  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The place name. | No |
| category | string | The place category (e.g.: Airport, Restaurant, Park, etc.). | No |

### v1Point  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| lat | double | Latitude. | No |
| lng | double | Latitude. | No |

### v1Price  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| fixed | string (uint64) | Amount in cents. Fixed price means a price which the supplier commits to in advance. | No |
| lower_bound | string (uint64) | Amount in cents. Lower bound of an estimated price. | No |
| upper_bound | string (uint64) | Amount in cents. Lower bound of an estimated price. | No |
| currency | string | ISO 4217 code. | No |

### v1RideEtaUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| eta_to_pickup | [v1UnixTime](#v1unixtime) | Updated estimated time (in epoch) until pickup.
NOTE: DEPRECATED soon - please use eta_to_pickup_seconds. | No |
| eta_to_destination | [v1UnixTime](#v1unixtime) | Updated estimated time (in epoch) until destination.
NOTE: DEPRECATED soon - please use eta_to_destination_seconds. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1RideLocationUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| current_location | [v1Point](#v1point) | Updated location of the vehicle. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1RidePickupAndDestinationUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| pickup | [commonv1Location](#commonv1location) | Updated pickup location. | No |
| destination | [commonv1Location](#commonv1location) | Updated destination location. | No |
| eta_to_pickup | [v1UnixTime](#v1unixtime) | Updated estimated time (in epoch) of arrival to pickup, time since epoch.
NOTE: This field will be deprecated soon, please use eta_to_pickup_seconds instead. | No |
| eta_to_destination | [v1UnixTime](#v1unixtime) | Updated estimated time (in epoch) of arrival to destination.
NOTE: This field will be deprecated soon, please use eta_to_destination_seconds instead. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |

### v1RidePriceUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| booking_estimated_price | [v1Price](#v1price) | Updated estimated price. | No |
| actual_price | [v1Price](#v1price) | Updated actual price of the ride. | No |
| is_final_price | boolean (boolean) | Marks the price as a final price. This price will be charged after the ride is completed. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1RideRequestedPickupTimeUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| prebook_pickup_time | [v1UnixTime](#v1unixtime) | New requested pickup time form the supplier. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1RideVehicleAndDriverUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| vehicle | [v1Vehicle](#v1vehicle) | Updated vehicle. | No |
| driver | [v1DriverDetails](#v1driverdetails) | Updated driver. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1SimpleRideBookingConstraints  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| passengers_no | long | Number of passengers. | No |
| suitcases_no | long | Number of suitcases. | No |

### v1SimpleRideDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| pickup | [commonv1Location](#commonv1location) | Origin of the ride. | No |
| destination | [commonv1Location](#commonv1location) | Destination of the ride. | No |
| constraints | [v1SimpleRideBookingConstraints](#v1simpleridebookingconstraints) | Special requests of the client. | No |
| passenger_details | [v1PassengerDetails](#v1passengerdetails) | Details of the passenger. | No |
| pickup_time | [v1UnixTime](#v1unixtime) | Requested pickuo time. | No |
| passenger_note | string | Free-text comments by the passenger. | No |
| dispatcher_offer_id | string | Supplier generated unique offer ID. See SimpleRideOffer. | No |
| payment_flow | [v1PaymentFlow](#v1paymentflow) | The ride's payment flow. | No |

### v1SimpleRideOffer  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| dispatcher_offer_id | string | Supplier generated unique offer ID. Relevant only for selectable offers. | No |
| pickup_eta | [v1UnixTime](#v1unixtime) | Estimated pickup time in epoch.
NOTE: This field will be deprecated soon. please use pickup_eta_seconds instead. | No |
| dropoff_eta | [v1UnixTime](#v1unixtime) | Estimated dropoff time in epoch.
NOTE: This field will be deprecated soon. please use estimated_ride_duration_seconds instead. | No |
| booking_estimated_price | [v1Price](#v1price) | Estimated price. | No |
| pickup_eta_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| estimated_ride_duration_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |

### v1SimpleRideOffers  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| request_id | string | Set to the request_id received in the original GetSimpleRideOffersRequest. | No |
| is_selectable | boolean (boolean) | An offer is selectable if during ride creation, demander can ask for this specific offer to be used to create the ride. | No |
| offers | [ [v1SimpleRideOffer](#v1simplerideoffer) ] | A set of offers. | No |
| supplier | [v1Supplier](#v1supplier) | Details of the supplier. Given for aggregate suppliers. | No |

### v1Supplier  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | A unique supplier ID. | No |
| english_name | string | The name of the supplier, in English. | No |
| local_name | string | Optional. The name of the supplier in the local language. | No |
| logo_url | string | Optional. A URL pointing to a logo image for the supplier. | No |
| phone_number | string | The supplier’s telephone number. | No |
| website_url | string | URL of the supplier’s website. | No |

### v1SupplierCancelRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| cancel_reason | string | Cancellation reason. | No |
| cancel_reason_category | [SupplierCancelRideRequestSupplierCancelReasonCategory](#suppliercancelriderequestsuppliercancelreasoncategory) | Cancellation reason category. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1SupplierRideStatus  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| status_code | [v1SupplierRideStatusRideStatus](#v1supplierridestatusridestatus) | Current status of te ride. | No |
| status_information | string | Additional information regarding the current state. | No |

### v1SupplierRideStatusRideStatus  

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and drive to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1SupplierRideStatusRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and drive to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander). |  |

### v1SupplierRideStatusUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| status_code | [v1SupplierRideStatusUpdateRideStatus](#v1supplierridestatusupdateridestatus) | Current status of te ride. | No |
| status_information | string | Additional information regarding the current state. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [v1EnvironmentType](#v1environmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### v1SupplierRideStatusUpdateRideStatus  

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and drive to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1SupplierRideStatusUpdateRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and drive to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander). |  |

### v1UnixTime  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| seconds_since_epoch | string (uint64) | Seconds since epoch UTC. | No |

### v1Vehicle  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| license_plate_number | string | The vehicle’s license plate number. | No |
| vehicle_type | [VehicleVehicleType](#vehiclevehicletype) | The vehicle type (standard, limo, van). | No |
| make | string | The vehicle make. | No |
| model | string | The vehicle model. | No |
| color | string | The vehicle color. | No |
