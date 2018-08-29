# Protocol Documentation
<a name="top"/>

## Table of Contents

- [marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_common.proto](#marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_common.proto)
    - [Address](#supply.common.vNext.Address)
    - [DriverDetails](#supply.common.vNext.DriverDetails)
    - [Empty](#supply.common.vNext.Empty)
    - [Location](#supply.common.vNext.Location)
    - [PassengerDetails](#supply.common.vNext.PassengerDetails)
    - [Point](#supply.common.vNext.Point)
    - [Price](#supply.common.vNext.Price)
    - [Supplier](#supply.common.vNext.Supplier)
    - [UnixTime](#supply.common.vNext.UnixTime)
    - [Vehicle](#supply.common.vNext.Vehicle)

    - [EnvironmentType](#supply.common.vNext.EnvironmentType)
    - [Vehicle.VehicleType](#supply.common.vNext.Vehicle.VehicleType)




- [marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_messages.proto](#marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_messages.proto)
    - [CreateSimpleRideRequest](#supply.rides.vNext.CreateSimpleRideRequest)
    - [CreateSimpleRideResponse](#supply.rides.vNext.CreateSimpleRideResponse)
    - [DemanderCancelRideRequest](#supply.rides.vNext.DemanderCancelRideRequest)
    - [DemanderCancelRideResponse](#supply.rides.vNext.DemanderCancelRideResponse)
    - [GetRideStatusRequest](#supply.rides.vNext.GetRideStatusRequest)
    - [GetSimpleRideOffersRequest](#supply.rides.vNext.GetSimpleRideOffersRequest)
    - [RideEtaUpdate](#supply.rides.vNext.RideEtaUpdate)
    - [RideLocationUpdate](#supply.rides.vNext.RideLocationUpdate)
    - [RidePickupAndDestinationUpdate](#supply.rides.vNext.RidePickupAndDestinationUpdate)
    - [RidePriceUpdate](#supply.rides.vNext.RidePriceUpdate)
    - [RideRequestedPickupTimeUpdate](#supply.rides.vNext.RideRequestedPickupTimeUpdate)
    - [RideVehicleAndDriverUpdate](#supply.rides.vNext.RideVehicleAndDriverUpdate)
    - [SimpleRideBookingConstraints](#supply.rides.vNext.SimpleRideBookingConstraints)
    - [SimpleRideDetails](#supply.rides.vNext.SimpleRideDetails)
    - [SimpleRideOffer](#supply.rides.vNext.SimpleRideOffer)
    - [SimpleRideOffers](#supply.rides.vNext.SimpleRideOffers)
    - [SupplierCancelRideRequest](#supply.rides.vNext.SupplierCancelRideRequest)
    - [SupplierRideStatus](#supply.rides.vNext.SupplierRideStatus)
    - [SupplierRideStatusUpdate](#supply.rides.vNext.SupplierRideStatusUpdate)

    - [SupplierRideStatus.RideStatus](#supply.rides.vNext.SupplierRideStatus.RideStatus)
    - [SupplierRideStatusUpdate.RideStatus](#supply.rides.vNext.SupplierRideStatusUpdate.RideStatus)




- [marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_service.proto](#marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_service.proto)



    - [RidesDispatchApi](#supply.rides.vNext.RidesDispatchApi)
    - [RidesSupplyApi](#supply.rides.vNext.RidesSupplyApi)


- [marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_messages.proto](#marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_messages.proto)





- [marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_service.proto](#marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_service.proto)





- [Scalar Value Types](#scalar-value-types)



<a name="marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_common.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_common.proto



<a name="supply.common.vNext.Address"/>

### Address



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| country | [string](#string) |  | Localized country name. |
| country_code | [string](#string) |  | ISO 3166-alpha-3 country code. |
| state | [string](#string) |  | State (first subdivision level below the country, if relevant). |
| county | [string](#string) |  | County (second subdivision level below the country, if relevant). |
| city | [string](#string) |  | City/town. |
| district | [string](#string) |  | District (subdivision level below the city). |
| sub_district | [string](#string) |  | Sub-district (subdivision level below the district; e.g. commonly used in IND). |
| street | [string](#string) |  | Street name. |
| house_number | [string](#string) |  | House number; depending on regional characteristics, can also be house name. |
| postal_code | [string](#string) |  | Postal code (zipcode). |
| building_name | [string](#string) |  | Building name; e.g. commonly used in HKG. |
| line | [string](#string) | repeated | Formatted address lines. |






<a name="supply.common.vNext.DriverDetails"/>

### DriverDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| driver_id | [string](#string) |  | Mandatory. Unique Id of the driver in the dispatcher system. |
| name | [string](#string) |  | Mandatory. Full name of the driver, in English. |
| phone | [string](#string) |  | Mandatory. Phone number though which the driver is reachable. |
| picture_url | [string](#string) |  | URL of a driver photo. |
| driving_license_id | [string](#string) |  | Mandatory in some jurisdictions. License id of the driver. |






<a name="supply.common.vNext.Empty"/>

### Empty







<a name="supply.common.vNext.Location"/>

### Location



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| point | [Point](#supply.common.vNext.Point) |  | geographic coordinates (latitude, longtitude). |
| address | [Address](#supply.common.vNext.Address) |  | description, state and zip code are optional, rest are mandatory. |
| free_text | [string](#string) |  | Place name or street address in a free text format. |






<a name="supply.common.vNext.PassengerDetails"/>

### PassengerDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Full name of the passenger. |
| phone_number | [string](#string) |  | Phone number in full international format. |
| photo_url | [string](#string) |  | Optional URL. |






<a name="supply.common.vNext.Point"/>

### Point



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lat | [double](#double) |  | Latitude. |
| lng | [double](#double) |  | Latitude. |






<a name="supply.common.vNext.Price"/>

### Price



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| fixed | [uint64](#uint64) |  | Amount in cents. Fixed price means a price which the supplier commits to in advance. |
| lower_bound | [uint64](#uint64) |  | Amount in cents. Lower bound of an estimated price. |
| upper_bound | [uint64](#uint64) |  | Amount in cents. Lower bound of an estimated price. |
| currency | [string](#string) |  | ISO 4217 code. |






<a name="supply.common.vNext.Supplier"/>

### Supplier
Ride supplier details


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | A unique supplier ID. |
| english_name | [string](#string) |  | The name of the supplier, in English. |
| local_name | [string](#string) |  | Optional. The name of the supplier in the local language. |
| logo_url | [string](#string) |  | Optional. A URL pointing to a logo image for the supplier. |
| phone_number | [string](#string) |  | The supplier’s telephone number. |
| website_url | [string](#string) |  | URL of the supplier’s website. |






<a name="supply.common.vNext.UnixTime"/>

### UnixTime



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| seconds_since_epoch | [uint64](#uint64) |  | Seconds since epoch UTC. |






<a name="supply.common.vNext.Vehicle"/>

### Vehicle
Vehicle details


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| license_plate_number | [string](#string) |  | The vehicle’s license plate number. |
| vehicle_type | [Vehicle.VehicleType](#supply.common.vNext.Vehicle.VehicleType) |  | The vehicle type (standard, limo, van). |
| make | [string](#string) |  | The vehicle make. |
| model | [string](#string) |  | The vehicle model. |
| color | [string](#string) |  | The vehicle color. |








<a name="supply.common.vNext.EnvironmentType"/>

### EnvironmentType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 |  |
| SANDBOX | 1 |  |
| PRODUCTION | 2 |  |
| TEST | 3 |  |



<a name="supply.common.vNext.Vehicle.VehicleType"/>

### Vehicle.VehicleType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Default value - unknown vehicle type. |
| STANDARD | 1 | Standard vehicle. |
| LIMO | 2 | Limousine. |
| VAN | 3 | Van. |
| OTHER | 4 | Other known type - not specified. |










<a name="marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_messages.proto



<a name="supply.rides.vNext.CreateSimpleRideRequest"/>

### CreateSimpleRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace if of the supplier for which we want to create the ride. |
| ride_id | [string](#string) |  | Marketplace generated ride id which will be used to identify this ride. |
| ride_details | [SimpleRideDetails](#supply.rides.vNext.SimpleRideDetails) |  | Details of the ride creation request. |
| demander_id | [string](#string) |  | additional fields for reporting and GDPR functionality. |
| demander_user_id | [string](#string) |  |  |
| demander_product_id | [string](#string) |  |  |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.CreateSimpleRideResponse"/>

### CreateSimpleRideResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| accepted_and_looking_for_driver | [bool](#bool) |  | Return true if ride was accepted and supplier is looking for a driver, or false if the ride is rejected. This call should return quickly and not wait for human confirmation. |
| pickup_eta | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Estimated time of arrival to pickup. |
| booking_estimated_price | [supply.common.vNext.Price](#supply.common.vNext.Price) |  | Estimated price. |






<a name="supply.rides.vNext.DemanderCancelRideRequest"/>

### DemanderCancelRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| cancel_reason | [string](#string) |  | Cancellation reason. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.DemanderCancelRideResponse"/>

### DemanderCancelRideResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| cancel_accepted | [bool](#bool) |  | true if cancellation went through, false it if ride cannot be cancelled. TBD: cancel and pay fee. |
| cancel_reason | [string](#string) |  | in case cancellation failed, a textual reason explaining the cause. |






<a name="supply.rides.vNext.GetRideStatusRequest"/>

### GetRideStatusRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.GetSimpleRideOffersRequest"/>

### GetSimpleRideOffersRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| request_id | [string](#string) |  | Unique request id generated by the markeplace. |
| supplier_id | [string](#string) |  | Marketplace ID of the supplier from which we want offers. |
| pickup | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Origin of the ride (pickup location). |
| destination | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Destination of the ride (dropoff location). |
| constraints | [SimpleRideBookingConstraints](#supply.rides.vNext.SimpleRideBookingConstraints) |  | Constraints represent the requested ride parameters. |
| pickup_time | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Pickup time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.RideEtaUpdate"/>

### RideEtaUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| eta_to_pickup | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Updated estimated time till pickup. NOTE: DEPRECATED soon - please use eta_to_pickup_seconds. |
| eta_to_destination | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Updated estimated time till destination. NOTE: DEPRECATED soon - please use eta_to_destination_seconds. |
| eta_to_pickup_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Updated estimated time till pickup in seconds. absolute time. |
| eta_to_destination_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Updated estimated time till destination in seconds. absolute time. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.RideLocationUpdate"/>

### RideLocationUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| current_location | [supply.common.vNext.Point](#supply.common.vNext.Point) |  | Updated location of the vehicle. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.RidePickupAndDestinationUpdate"/>

### RidePickupAndDestinationUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| pickup | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Updated pickup location. |
| destination | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Updated destination location. |
| eta_to_pickup | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Updated estimated time of arrival to pickup. NOTE: This field will be deprecated soon, please use eta_to_pickup_seconds instead. |
| eta_to_destination | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Updated estimated time of arrival to destination NOTE: This field will be deprecated soon, please use eta_to_destination_seconds instead. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |
| eta_to_pickup_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Updated estimated time till pickup in seconds. absolute time. |
| eta_to_destination_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Updated estimated time till destination in seconds. absolute time. |






<a name="supply.rides.vNext.RidePriceUpdate"/>

### RidePriceUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| booking_estimated_price | [supply.common.vNext.Price](#supply.common.vNext.Price) |  | Updated estimated price. |
| actual_price | [supply.common.vNext.Price](#supply.common.vNext.Price) |  | Updated actual price of the ride. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.RideRequestedPickupTimeUpdate"/>

### RideRequestedPickupTimeUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| prebook_pickup_time | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | New requested pickup time form the supplier. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.RideVehicleAndDriverUpdate"/>

### RideVehicleAndDriverUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| vehicle | [supply.common.vNext.Vehicle](#supply.common.vNext.Vehicle) |  | Updated vehicle. |
| driver | [supply.common.vNext.DriverDetails](#supply.common.vNext.DriverDetails) |  | Updated driver. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.SimpleRideBookingConstraints"/>

### SimpleRideBookingConstraints



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| passengers_no | [uint32](#uint32) |  | Number of pasengers. |
| suitcases_no | [uint32](#uint32) |  | Number of suitcases. |






<a name="supply.rides.vNext.SimpleRideDetails"/>

### SimpleRideDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| pickup | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Origin of the ride. |
| destination | [supply.common.vNext.Location](#supply.common.vNext.Location) |  | Destination of the ride. |
| constraints | [SimpleRideBookingConstraints](#supply.rides.vNext.SimpleRideBookingConstraints) |  | Special requests of the client. |
| passenger_details | [supply.common.vNext.PassengerDetails](#supply.common.vNext.PassengerDetails) |  | Details of the passenger. |
| pickup_time | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Requested pickuo time. |
| passenger_note | [string](#string) |  | Free-text comments by the passanger. |
| dispatcher_offer_id | [string](#string) |  | Supplier generated unique offer ID. See SimpleRideOffer. |






<a name="supply.rides.vNext.SimpleRideOffer"/>

### SimpleRideOffer



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| dispatcher_offer_id | [string](#string) |  | Supplier generated unique offer ID. Relevant only for selectable offers. |
| pickup_eta | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Estimated pickup time. NOTE: This field will be deprecated soon. please use pickup_eta_seconds instead. |
| dropoff_eta | [supply.common.vNext.UnixTime](#supply.common.vNext.UnixTime) |  | Estimated dropoff time. NOTE: This field will be deprecated soon. please use estimated_ride_duration_seconds instead. |
| booking_estimated_price | [supply.common.vNext.Price](#supply.common.vNext.Price) |  | Estimated price. |
| pickup_eta_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated pickup time in seconds. absolute time. |
| estimated_ride_duration_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated dropoff time in seconds. absolute time. This is the time between pickup to dropoff. It does not contain the time to pickup. |






<a name="supply.rides.vNext.SimpleRideOffers"/>

### SimpleRideOffers



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| request_id | [string](#string) |  | Set to the request_id received in the original GetSimpleRideOffersRequest. |
| is_selectable | [bool](#bool) |  | An offer is selectable if during ride creation, demander can ask for this specific offer to be used to create the ride. |
| offers | [SimpleRideOffer](#supply.rides.vNext.SimpleRideOffer) | repeated | A set of offers. |
| supplier | [supply.common.vNext.Supplier](#supply.common.vNext.Supplier) |  | Details of the supplier. Given for aggregate suppliers. |






<a name="supply.rides.vNext.SupplierCancelRideRequest"/>

### SupplierCancelRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| cancel_reason | [string](#string) |  | Cancellation reason. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |






<a name="supply.rides.vNext.SupplierRideStatus"/>

### SupplierRideStatus



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| status_code | [SupplierRideStatus.RideStatus](#supply.rides.vNext.SupplierRideStatus.RideStatus) |  | Current status of te ride. |
| status_information | [string](#string) |  | Additional information regarding the current state. |






<a name="supply.rides.vNext.SupplierRideStatusUpdate"/>

### SupplierRideStatusUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | Marketplace generated supplier id. |
| ride_id | [string](#string) |  | Marketplace generated ride id. |
| status_code | [SupplierRideStatusUpdate.RideStatus](#supply.rides.vNext.SupplierRideStatusUpdate.RideStatus) |  | Current status of te ride. |
| status_information | [string](#string) |  | Additional information regarding the current state. |
| update_id | [string](#string) |  | Dispatcher-generated id which uniquely identifies this update. |
| update_ts | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | Dispatcher-generated timestamp which identifies the update time. |
| environment_type | [supply.common.vNext.EnvironmentType](#supply.common.vNext.EnvironmentType) |  | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. |








<a name="supply.rides.vNext.SupplierRideStatus.RideStatus"/>

### SupplierRideStatus.RideStatus
RideStatus represents the different statuses a ride can be at.

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Status is unknown. |
| REJECTED | 8 |  |
| ACCEPTED | 1 | Supplier confirmed the ride, but driver is not yet allocated. |
| DRIVER_ASSIGNED | 2 | Driver is allocated, but ride has not yet started. |
| DRIVER_EN_ROUTE | 3 | Drive started and driver is en-route. |
| AT_PICKUP | 4 | Driver is arrived at the pickup point, but passenger is not yet on board. |
| PASSANGER_ON_BOARD | 5 | Passenger is on board and drive to destination starterd. |
| COMPLETED | 6 | Ride complete and passenger disembarked. |
| CANCELED | 7 | Ride is cancelled (due to supplier or due to demander). |



<a name="supply.rides.vNext.SupplierRideStatusUpdate.RideStatus"/>

### SupplierRideStatusUpdate.RideStatus
RideStatus represents the different statuses a ride can be at.

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Status is unknown. |
| REJECTED | 8 |  |
| ACCEPTED | 1 | Supplier confirmed the ride, but driver is not yet allocated. |
| DRIVER_ASSIGNED | 2 | Driver is allocated, but ride has not yet started. |
| DRIVER_EN_ROUTE | 3 | Drive started and driver is en-route. |
| AT_PICKUP | 4 | Driver is arrived at the pickup point, but passenger is not yet on board. |
| PASSANGER_ON_BOARD | 5 | Passenger is on board and drive to destination starterd. |
| COMPLETED | 6 | Ride complete and passenger disembarked. |
| CANCELED | 7 | Ride is cancelled (due to supplier or due to demander). |


 

 

 



<a name="marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_rides_service.proto


 

 

 


<a name="supply.rides.vNext.RidesDispatchApi"/>

### RidesDispatchApi


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| RequestOffers | [GetSimpleRideOffersRequest](#supply.rides.vNext.GetSimpleRideOffersRequest) | [SimpleRideOffers](#supply.rides.vNext.GetSimpleRideOffersRequest) | Request ride offers from the supplier |
| CreateRide | [CreateSimpleRideRequest](#supply.rides.vNext.CreateSimpleRideRequest) | [CreateSimpleRideResponse](#supply.rides.vNext.CreateSimpleRideRequest) | Create a ride with the supplier |
| CancelRide | [DemanderCancelRideRequest](#supply.rides.vNext.DemanderCancelRideRequest) | [DemanderCancelRideResponse](#supply.rides.vNext.DemanderCancelRideRequest) | Update the supplier that the demander has cancelled the ride. |
| GetRideStatus | [GetRideStatusRequest](#supply.rides.vNext.GetRideStatusRequest) | [SupplierRideStatus](#supply.rides.vNext.GetRideStatusRequest) | Request the latest status of the ride from the supplier |


<a name="supply.rides.vNext.RidesSupplyApi"/>

### RidesSupplyApi


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| UpdateRideStatus | [SupplierRideStatusUpdate](#supply.rides.vNext.SupplierRideStatusUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.SupplierRideStatusUpdate) | Update the marketplace that the ride status changed |
| UpdateRideLocation | [RideLocationUpdate](#supply.rides.vNext.RideLocationUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RideLocationUpdate) | Update the marketplace that the vehicle location has changed |
| UpdateRideVehicleAndDriver | [RideVehicleAndDriverUpdate](#supply.rides.vNext.RideVehicleAndDriverUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RideVehicleAndDriverUpdate) | Update the marketplace that the assigned vehicle and driver have changed |
| UpdateRidePickupAndDestination | [RidePickupAndDestinationUpdate](#supply.rides.vNext.RidePickupAndDestinationUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RidePickupAndDestinationUpdate) | Update the marketplace that the meeting pickup and destination points changed |
| UpdateRideEta | [RideEtaUpdate](#supply.rides.vNext.RideEtaUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RideEtaUpdate) | Update the marketplace that estimated time to arrival to the origin and and to destination has changed Recommended to update only when there is a major change (1 minute at least) |
| UpdateRidePrice | [RidePriceUpdate](#supply.rides.vNext.RidePriceUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RidePriceUpdate) | Update the marketplace that the ride price has changed |
| UpdateRideRequestedPickupTime | [RideRequestedPickupTimeUpdate](#supply.rides.vNext.RideRequestedPickupTimeUpdate) | [.supply.common.vNext.Empty](#supply.rides.vNext.RideRequestedPickupTimeUpdate) |  |
| CancelRide | [SupplierCancelRideRequest](#supply.rides.vNext.SupplierCancelRideRequest) | [.supply.common.vNext.Empty](#supply.rides.vNext.SupplierCancelRideRequest) | Update the marketplace that the assigned supplier has cancelled the ride |

 



<a name="marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_messages.proto


 

 

 

 



<a name="marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/supply_handler/vNext/gen-doc/supply_handler_shared_rides_service.proto


 

 

 

 



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
