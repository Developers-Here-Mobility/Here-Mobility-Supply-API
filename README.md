# Protocol Documentation
<a name="top"/>

## Table of Contents

- [marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_common.proto](#marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_common.proto)
    - [Address](#supply.common.v1.Address)
    - [DriverDetails](#supply.common.v1.DriverDetails)
    - [Empty](#supply.common.v1.Empty)
    - [Location](#supply.common.v1.Location)
    - [PassengerDetails](#supply.common.v1.PassengerDetails)
    - [Place](#supply.common.v1.Place)
    - [Point](#supply.common.v1.Point)
    - [Price](#supply.common.v1.Price)
    - [Supplier](#supply.common.v1.Supplier)
    - [UnixTime](#supply.common.v1.UnixTime)
    - [Vehicle](#supply.common.v1.Vehicle)

    - [PaymentFlow](#supply.common.v1.PaymentFlow)
    - [Vehicle.VehicleType](#supply.common.v1.Vehicle.VehicleType)




- [marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_messages.proto](#marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_messages.proto)
    - [CreateSimpleRideRequest](#supply.rides.v1.CreateSimpleRideRequest)
    - [CreateSimpleRideResponse](#supply.rides.v1.CreateSimpleRideResponse)
    - [DemanderCancelRideRequest](#supply.rides.v1.DemanderCancelRideRequest)
    - [DemanderCancelRideResponse](#supply.rides.v1.DemanderCancelRideResponse)
    - [GetRideStatusRequest](#supply.rides.v1.GetRideStatusRequest)
    - [GetSimpleRideOffersRequest](#supply.rides.v1.GetSimpleRideOffersRequest)
    - [RideEtaUpdate](#supply.rides.v1.RideEtaUpdate)
    - [RideLocationUpdate](#supply.rides.v1.RideLocationUpdate)
    - [RidePickupAndDestinationUpdate](#supply.rides.v1.RidePickupAndDestinationUpdate)
    - [RidePriceUpdate](#supply.rides.v1.RidePriceUpdate)
    - [RideRequestedPickupTimeUpdate](#supply.rides.v1.RideRequestedPickupTimeUpdate)
    - [RideVehicleAndDriverUpdate](#supply.rides.v1.RideVehicleAndDriverUpdate)
    - [SimpleRideBookingConstraints](#supply.rides.v1.SimpleRideBookingConstraints)
    - [SimpleRideDetails](#supply.rides.v1.SimpleRideDetails)
    - [SimpleRideOffer](#supply.rides.v1.SimpleRideOffer)
    - [SimpleRideOffers](#supply.rides.v1.SimpleRideOffers)
    - [SupplierCancelRideRequest](#supply.rides.v1.SupplierCancelRideRequest)
    - [SupplierRideStatus](#supply.rides.v1.SupplierRideStatus)
    - [SupplierRideStatusUpdate](#supply.rides.v1.SupplierRideStatusUpdate)

    - [DemanderCancelRideRequest.PassengerCancelReasonCategory](#supply.rides.v1.DemanderCancelRideRequest.PassengerCancelReasonCategory)
    - [SupplierCancelRideRequest.SupplierCancelReasonCategory](#supply.rides.v1.SupplierCancelRideRequest.SupplierCancelReasonCategory)
    - [SupplierRideStatus.RideStatus](#supply.rides.v1.SupplierRideStatus.RideStatus)
    - [SupplierRideStatusUpdate.RideStatus](#supply.rides.v1.SupplierRideStatusUpdate.RideStatus)




- [marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_service.proto](#marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_service.proto)



    - [RidesDispatchApi](#supply.rides.v1.RidesDispatchApi)
    - [RidesSupplyApi](#supply.rides.v1.RidesSupplyApi)


- [marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_messages.proto](#marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_messages.proto)





- [marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_service.proto](#marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_service.proto)





- [Scalar Value Types](#scalar-value-types)



<a name="marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_common.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_common.proto



<a name="supply.common.v1.Address"/>

### Address



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| country | [string](#string) |  | Optional. Localized country name. |
| country_code | [string](#string) |  | Optional. ISO 3166-alpha-3 country code. |
| state | [string](#string) |  | Optional. State (first subdivision level below the country, if relevant). |
| county | [string](#string) |  | Optional. County (second subdivision level below the country, if relevant). |
| city | [string](#string) |  | Optional. City/town. |
| district | [string](#string) |  | Optional. District (subdivision level below the city). |
| sub_district | [string](#string) |  | Optional. Sub-district (subdivision level below the district; e.g. commonly used in IND). |
| street | [string](#string) |  | Optional. Street name. |
| house_number | [string](#string) |  | Optional. House number; depending on regional characteristics, can also be house name. |
| postal_code | [string](#string) |  | Optional. Postal code (zipcode). |
| building_name | [string](#string) |  | Optional. Building name; e.g. commonly used in HKG. |
| line | [string](#string) | repeated | Optional. Formatted address lines. |






<a name="supply.common.v1.DriverDetails"/>

### DriverDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| driver_id | [string](#string) |  | Mandatory. Unique ID of the driver in the dispatcher system. |
| name | [string](#string) |  | Mandatory. Full name of the driver, in English. |
| phone | [string](#string) |  | Mandatory. Phone number through which the driver is reachable. |
| picture_url | [string](#string) |  | Optional. URL of the driver&#39;s photo. |
| driving_license_id | [string](#string) |  | Mandatory in some jurisdictions. License ID of the driver. |






<a name="supply.common.v1.Empty"/>

### Empty







<a name="supply.common.v1.Location"/>

### Location



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| point | [Point](#supply.common.v1.Point) |  | Mandatory. Geographic coordinates (latitude, longtitude). |
| address | [Address](#supply.common.v1.Address) |  | Optional. |
| place | [Place](#supply.common.v1.Place) |  | Optional. Place information of the location. |
| free_text | [string](#string) |  | Optional. Street address in a free text format. |






<a name="supply.common.v1.PassengerDetails"/>

### PassengerDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Mandatory. Full name of the passenger. |
| phone_number | [string](#string) |  | Mandatory. Phone number in full international format. |
| photo_url | [string](#string) |  | Optional. URL. |






<a name="supply.common.v1.Place"/>

### Place



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Optional. The place&#39;s name. |
| category | [string](#string) |  | Optional. The place&#39;s category (e.g.: Airport, Restaurant, Park, etc.). |






<a name="supply.common.v1.Point"/>

### Point



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lat | [double](#double) |  | Mandatory. Latitude. |
| lng | [double](#double) |  | Mandatory. Longtitude. |






<a name="supply.common.v1.Price"/>

### Price



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| fixed | [uint64](#uint64) |  | Optional. Amount in cents. Fixed price means a price which the supplier commits to in advance. |
| lower_bound | [uint64](#uint64) |  | Optional. Amount in cents. Lower bound of an estimated price. |
| upper_bound | [uint64](#uint64) |  | Optional. Amount in cents. Upper bound of an estimated price. |
| currency | [string](#string) |  | Optional. ISO 4217 code. |






<a name="supply.common.v1.Supplier"/>

### Supplier
Ride supplier details (for aggregated suppliers only)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Optional. A unique supplier ID. |
| english_name | [string](#string) |  | Mandatory. The name of the supplier, in English. |
| local_name | [string](#string) |  | Optional. The name of the supplier in the local language. |
| logo_url | [string](#string) |  | Optional. A URL pointing to a logo image of the supplier. |
| phone_number | [string](#string) |  | Mandatory. The supplier’s telephone number. |
| website_url | [string](#string) |  | Optional. URL of the supplier’s website. |






<a name="supply.common.v1.UnixTime"/>

### UnixTime



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| seconds_since_epoch | [uint64](#uint64) |  | Seconds since epoch UTC. |






<a name="supply.common.v1.Vehicle"/>

### Vehicle
Vehicle details


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| license_plate_number | [string](#string) |  | Optional. The vehicle’s license plate number. |
| vehicle_type | [Vehicle.VehicleType](#supply.common.v1.Vehicle.VehicleType) |  | Optional. The vehicle&#39;s type (standard, limo, van). |
| make | [string](#string) |  | Optional. The vehicle&#39;s make. |
| model | [string](#string) |  | Optional. The vehicle&#39;s model. |
| color | [string](#string) |  | Optional. The vehicle&#39;s color. |








<a name="supply.common.v1.PaymentFlow"/>

### PaymentFlow
Information about the payment flow used in a ride

| Name | Number | Description |
| ---- | ------ | ----------- |
| OFFLINE_PAYMENT | 0 | Offline payment flow is used. |
| ONLINE_PAYMENT | 1 | Online payment flow is used. |



<a name="supply.common.v1.Vehicle.VehicleType"/>

### Vehicle.VehicleType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Default value - unknown vehicle type. |
| STANDARD | 1 | Standard vehicle. |
| LIMO | 2 | Limousine. |
| VAN | 3 | Van. |
| OTHER | 4 | Other known type - not specified. |










<a name="marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_messages.proto



<a name="supply.rides.v1.CreateSimpleRideRequest"/>

### CreateSimpleRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace ID of the supplier for which we want to create the ride. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID which will be used to identify this ride. |
| ride_details | [SimpleRideDetails](#supply.rides.v1.SimpleRideDetails) |  | Mandatory. Details of the ride creation request. |






<a name="supply.rides.v1.CreateSimpleRideResponse"/>

### CreateSimpleRideResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| accepted_and_looking_for_driver | [bool](#bool) |  | Mandatory. Return true if ride was accepted and supplier is looking for a driver, or false if the ride is rejected. This call should return quickly and not wait for human confirmation. |
| pickup_eta | [supply.common.v1.UnixTime](#supply.common.v1.UnixTime) |  | Optional. Not yet supported. Estimated time of arrival to pickup. |
| booking_estimated_price | [supply.common.v1.Price](#supply.common.v1.Price) |  | Optional. Not yet supported. Estimated price. |






<a name="supply.rides.v1.DemanderCancelRideRequest"/>

### DemanderCancelRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| cancel_reason | [string](#string) |  | Optional. Cancellation reason. |
| cancel_reason_category | [DemanderCancelRideRequest.PassengerCancelReasonCategory](#supply.rides.v1.DemanderCancelRideRequest.PassengerCancelReasonCategory) |  | Optional. Cancellation reason category. |






<a name="supply.rides.v1.DemanderCancelRideResponse"/>

### DemanderCancelRideResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| cancel_accepted | [bool](#bool) |  | Mandatory. True if cancellation went through, false it if ride cannot be cancelled. TBD: cancel and pay fee. |
| cancel_reason | [string](#string) |  | Optional. In case cancellation failed, a textual reason explaining the cause. |






<a name="supply.rides.v1.GetRideStatusRequest"/>

### GetRideStatusRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |






<a name="supply.rides.v1.GetSimpleRideOffersRequest"/>

### GetSimpleRideOffersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| request_id | [string](#string) |  | Mandatory. Unique request ID generated by the marketplace. |
| supplier_id | [string](#string) |  | Mandatory. Marketplace ID of the supplier from which we want to recieve offers. |
| pickup | [supply.common.v1.Location](#supply.common.v1.Location) |  | Mandatory. Origin of the ride (pickup location). |
| destination | [supply.common.v1.Location](#supply.common.v1.Location) |  | Mandatory. Destination of the ride (dropoff location). |
| constraints | [SimpleRideBookingConstraints](#supply.rides.v1.SimpleRideBookingConstraints) |  | Mandatry. Constraints representing the requested ride parameters. |
| pickup_time | [supply.common.v1.UnixTime](#supply.common.v1.UnixTime) |  | Mandatory. Pickup time. |
| passenger_note | [string](#string) |  | Optional. Free-text comments by the passenger. |






<a name="supply.rides.v1.RideEtaUpdate"/>

### RideEtaUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| eta_to_pickup_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until pickup. For example: 60 seconds until the driver will pick you up NOTE: At least one of eta_to_pickup_seconds, eta_to_destination_seconds, eta_to_pickup and eta_to_destination is mandatory. |
| eta_to_destination_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until dropoff. For example: 20 minutes left until dropoff (20*60 = 1200 seconds) NOTE: At least one of eta_to_pickup_seconds, eta_to_destination_seconds, eta_to_pickup and eta_to_destination is mandatory. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.RideLocationUpdate"/>

### RideLocationUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| current_location | [supply.common.v1.Point](#supply.common.v1.Point) |  | Mandatory. Updated location of the vehicle. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.RidePickupAndDestinationUpdate"/>

### RidePickupAndDestinationUpdate
Not yet supported.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| pickup | [supply.common.v1.Location](#supply.common.v1.Location) |  | Optional. Updated pickup location. NOTE: At least one of pickup, destination, eta_to_pickup and eta_to_destination is mandatory. |
| destination | [supply.common.v1.Location](#supply.common.v1.Location) |  | Optional. Updated destination location. NOTE: At least one of pickup, destination, eta_to_pickup and eta_to_destination is mandatory. |
| eta_to_pickup_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until pickup. For example: 60 seconds until the driver will pick the passenger up |
| eta_to_destination_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until dropoff. For example: 20 minutes left until dropoff (20*60 = 1200 seconds) |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.RidePriceUpdate"/>

### RidePriceUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| booking_estimated_price | [supply.common.v1.Price](#supply.common.v1.Price) |  | Optional. Not yet supported. Updated ride estimated price. Currently not implemented. |
| actual_price | [supply.common.v1.Price](#supply.common.v1.Price) |  | Mandatory. Updated ride actual price. |
| is_final_price | [bool](#bool) |  | Optional. Marks the actual price as the final price of the ride. Once this field is set to true additional price updates will be ignored. When an online payment ride will reach status completed and the field is set to true the actual price will be charged. If this field won&#39;t be updated to true within 24 hours after the ride completion, the ride will close without charging |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.RideRequestedPickupTimeUpdate"/>

### RideRequestedPickupTimeUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| prebook_pickup_time | [supply.common.v1.UnixTime](#supply.common.v1.UnixTime) |  | Mandatory. New requested pickup time form the supplier. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.RideVehicleAndDriverUpdate"/>

### RideVehicleAndDriverUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| vehicle | [supply.common.v1.Vehicle](#supply.common.v1.Vehicle) |  | Optional. Updated vehicle details. NOTE: At least one of vehicle or driver is mandatory. |
| driver | [supply.common.v1.DriverDetails](#supply.common.v1.DriverDetails) |  | Optional. Updated driver details. NOTE: At least one of vehicle or driver is mandatory. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.SimpleRideBookingConstraints"/>

### SimpleRideBookingConstraints



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| passengers_no | [uint32](#uint32) |  | Mandatory. Number of passengers. |
| suitcases_no | [uint32](#uint32) |  | Mandatory. Number of suitcases. |






<a name="supply.rides.v1.SimpleRideDetails"/>

### SimpleRideDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| pickup | [supply.common.v1.Location](#supply.common.v1.Location) |  | Mandatory. Origin of the ride. |
| destination | [supply.common.v1.Location](#supply.common.v1.Location) |  | Mandatory. Destination of the ride. |
| constraints | [SimpleRideBookingConstraints](#supply.rides.v1.SimpleRideBookingConstraints) |  | Mandatory. Constraints representing the requested ride parameters. |
| passenger_details | [supply.common.v1.PassengerDetails](#supply.common.v1.PassengerDetails) |  | Mandatory. Details of the passenger. |
| pickup_time | [supply.common.v1.UnixTime](#supply.common.v1.UnixTime) |  | Optional. Ride pickup time recieved in the supplier offer. |
| passenger_note | [string](#string) |  | Optional. Free-text comments by the passenger. |
| dispatcher_offer_id | [string](#string) |  | Mandatory. Supplier generated unique offer ID. See SimpleRideOffer. |
| payment_flow | [supply.common.v1.PaymentFlow](#supply.common.v1.PaymentFlow) |  | Optional. The ride&#39;s payment flow. |






<a name="supply.rides.v1.SimpleRideOffer"/>

### SimpleRideOffer



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| dispatcher_offer_id | [string](#string) |  | Mandatory. Supplier generated unique offer ID. |
| booking_estimated_price | [supply.common.v1.Price](#supply.common.v1.Price) |  | Optional. Estimated price. |
| pickup_eta_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until pickup. For example: 60 seconds until the driver will pick the passenger up. |
| estimated_ride_duration_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds between pickup and dropoff. It does not include the time until pickup. For example: ride duration is 20 minutes (20*60 = 1200 seconds). |






<a name="supply.rides.v1.SimpleRideOffers"/>

### SimpleRideOffers



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offers | [SimpleRideOffer](#supply.rides.v1.SimpleRideOffer) | repeated | Mandatory. A set of offers. |
| sub_supplier_details | [supply.common.v1.Supplier](#supply.common.v1.Supplier) |  | Optional. Details of the sub-supplier. Used only for aggregated suppliers. |






<a name="supply.rides.v1.SupplierCancelRideRequest"/>

### SupplierCancelRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| cancel_reason | [string](#string) |  | Optional. Cancellation reason. |
| cancel_reason_category | [SupplierCancelRideRequest.SupplierCancelReasonCategory](#supply.rides.v1.SupplierCancelRideRequest.SupplierCancelReasonCategory) |  | Mandatory. Cancellation reason category. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |






<a name="supply.rides.v1.SupplierRideStatus"/>

### SupplierRideStatus



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| status_code | [SupplierRideStatus.RideStatus](#supply.rides.v1.SupplierRideStatus.RideStatus) |  | Mandatory. Current status of the ride. |
| status_information | [string](#string) |  | Optional. Additional information regarding the current state. |






<a name="supply.rides.v1.SupplierRideStatusUpdate"/>

### SupplierRideStatusUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Mandatory. Marketplace generated supplier ID. |
| ride_id | [string](#string) |  | Mandatory. Marketplace generated ride ID. |
| status_code | [SupplierRideStatusUpdate.RideStatus](#supply.rides.v1.SupplierRideStatusUpdate.RideStatus) |  | Mandatory. Current status of the ride. |
| status_information | [string](#string) |  | Optional. Additional information regarding the current state. |
| update_id | [string](#string) |  | Mandatory. Dispatcher-generated ID which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Mandatory. Dispatcher-generated timestamp which identifies the update time. |








<a name="supply.rides.v1.DemanderCancelRideRequest.PassengerCancelReasonCategory"/>

### DemanderCancelRideRequest.PassengerCancelReasonCategory
Passenger cancellation reason category

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY | 0 | Unknown cancellation category. |
| DRIVER_NO_SHOW | 1 | Driver did not show up. |
| PRICE_CHANGED | 2 | Ride price changed. |
| ETA_CHANGED | 3 | Ride ETA changed. |
| UNSUITABLE_VEHICLE | 4 | Ride vehicle is not suitable. |
| DRIVER_BEHAVED_INAPPROPRIATELY | 5 | Driver behaved inappropriately. |
| CHANGED_MY_PLANS | 6 | Passenger changed plans. |
| OTHER_PASSENGER_CANCEL_REASON_CATEGORY | 100 | Other. |



<a name="supply.rides.v1.SupplierCancelRideRequest.SupplierCancelReasonCategory"/>

### SupplierCancelRideRequest.SupplierCancelReasonCategory
Supplier cancellation reason category

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_SUPPLIER_CANCEL_REASON_CATEGORY | 0 | Unknown cancellation category. |
| DRIVERS_UNAVAILABLE | 1 | No available drivers for ride. |
| PASSENGER_NO_SHOW | 2 | Passenger did not show up for the ride. |
| PASSENGER_REQUESTED_TO_CANCEL | 3 | Passenger requested to cancel the ride. |
| VEHICLE_MALFUNCTION | 4 | Vehicle malfunction. |
| HEAVY_TRAFFIC | 5 | Heavy traffic. |
| OTHER_SUPPLIER_CANCEL_REASON_CATEGORY | 100 | Other cancellation category. |



<a name="supply.rides.v1.SupplierRideStatus.RideStatus"/>

### SupplierRideStatus.RideStatus
RideStatus represents the different statuses a ride can be at.

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Status is unknown. |
| REJECTED | 8 |  |
| ACCEPTED | 1 | Supplier confirmed the ride, but driver is not yet allocated. |
| DRIVER_ASSIGNED | 2 | Driver is allocated, but ride has not yet started. |
| DRIVER_EN_ROUTE | 3 | Ride started and driver is en-route. |
| AT_PICKUP | 4 | Driver has arrived to the pickup point, but passenger is not yet on board. |
| PASSENGER_ON_BOARD | 5 | Passenger is on board and ride to destination started. |
| AT_DROPOFF | 9 | Driver has arrived to the dropoff point. |
| COMPLETED | 6 | Ride complete and passenger disembarked. |
| CANCELED | 7 | Ride is cancelled (due to either supplier&#39;s or demander&#39;s request). |



<a name="supply.rides.v1.SupplierRideStatusUpdate.RideStatus"/>

### SupplierRideStatusUpdate.RideStatus
RideStatus represents the different statuses a ride can be at.

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Status is unknown. |
| REJECTED | 8 |  |
| ACCEPTED | 1 | Supplier confirmed the ride, but driver is not yet allocated. |
| DRIVER_ASSIGNED | 2 | Driver is allocated, but ride has not yet started. |
| DRIVER_EN_ROUTE | 3 | Ride started and driver is en-route. |
| AT_PICKUP | 4 | Driver has arrived to the pickup point, but passenger is not yet on board. |
| PASSENGER_ON_BOARD | 5 | Passenger is on board and ride to destination started. |
| AT_DROPOFF | 9 | Driver has arrived to the dropoff point. |
| COMPLETED | 6 | Ride complete and passenger disembarked. |
| CANCELED | 7 | Ride is cancelled (due to either supplier&#39;s or demander&#39;s request). |










<a name="marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_rides_service.proto









<a name="supply.rides.v1.RidesDispatchApi"/>

### RidesDispatchApi


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| RequestOffers | [GetSimpleRideOffersRequest](#supply.rides.v1.GetSimpleRideOffersRequest) | [SimpleRideOffers](#supply.rides.v1.GetSimpleRideOffersRequest) | Request ride offers from the supplier |
| CreateRide | [CreateSimpleRideRequest](#supply.rides.v1.CreateSimpleRideRequest) | [CreateSimpleRideResponse](#supply.rides.v1.CreateSimpleRideRequest) | Create a ride with the supplier |
| CancelRide | [DemanderCancelRideRequest](#supply.rides.v1.DemanderCancelRideRequest) | [DemanderCancelRideResponse](#supply.rides.v1.DemanderCancelRideRequest) | Update the supplier that the demander has cancelled the ride. |
| GetRideStatus | [GetRideStatusRequest](#supply.rides.v1.GetRideStatusRequest) | [SupplierRideStatus](#supply.rides.v1.GetRideStatusRequest) | Request the latest status of the ride from the supplier |


<a name="supply.rides.v1.RidesSupplyApi"/>

### RidesSupplyApi


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| UpdateRideStatus | [SupplierRideStatusUpdate](#supply.rides.v1.SupplierRideStatusUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.SupplierRideStatusUpdate) | Update the marketplace that the ride status changed |
| UpdateRideLocation | [RideLocationUpdate](#supply.rides.v1.RideLocationUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RideLocationUpdate) | Update the marketplace that the vehicle location has changed |
| UpdateRideVehicleAndDriver | [RideVehicleAndDriverUpdate](#supply.rides.v1.RideVehicleAndDriverUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RideVehicleAndDriverUpdate) | Update the marketplace that the assigned vehicle and driver have changed |
| UpdateRidePickupAndDestination | [RidePickupAndDestinationUpdate](#supply.rides.v1.RidePickupAndDestinationUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RidePickupAndDestinationUpdate) | Update the marketplace that the meeting pickup and destination points changed |
| UpdateRideEta | [RideEtaUpdate](#supply.rides.v1.RideEtaUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RideEtaUpdate) | Update the marketplace that estimated time to arrival to the origin and and to destination has changed Recommended to update only when there is a major change (1 minute at least) |
| UpdateRidePrice | [RidePriceUpdate](#supply.rides.v1.RidePriceUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RidePriceUpdate) | Update the marketplace that the ride price has changed |
| UpdateRideRequestedPickupTime | [RideRequestedPickupTimeUpdate](#supply.rides.v1.RideRequestedPickupTimeUpdate) | [.supply.common.v1.Empty](#supply.rides.v1.RideRequestedPickupTimeUpdate) |  |
| CancelRide | [SupplierCancelRideRequest](#supply.rides.v1.SupplierCancelRideRequest) | [.supply.common.v1.Empty](#supply.rides.v1.SupplierCancelRideRequest) | Update the marketplace that the assigned supplier has cancelled the ride |





<a name="marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_messages.proto












<a name="marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/v1/gen-doc/supply_handler_shared_rides_service.proto


 

 

 

 



## Scalar Value Types

| .proto Type | Notes | C++ Type | Java Type | Python Type |
| ----------- | ----- | -------- | --------- | ----------- |
| <a name="double" /> double |  | double | double | float |
| <a name="float" /> float |  | float | float | float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long |
| <a name="bool" /> bool |  | bool | boolean | boolean |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str |

