To get access token of shiprocket, follow the steps below.
  - Create a shiprocket account.
  - Create api user in the same.
  - Use the api user email and password in shiprocket authorization api to get bearer token.

Tried different pincodes in check courier serviceability api to know the coverage of shiprocket.

Flow of order, shipment in shiprocket.
  Use "create customer order" API to create an order in shiprocket.
  If want to mention channel, use "create channel specific order" API to create order.
  Complete KYC in shiprocket.
  Use "Generate AWB for shipment" API to generate awb number which is needed further.
  Use "Request shipment pickup" API to request shipment.
  Use "Generate label and Generate manifest" APis to generate the needed information for courier.

Above all apis are combined in a single api called, wrapper API forward.