Create an order:
{
    "order_id": "762345",
    "order_date": "2023-09-12",
    "pickup_location": "Primary",
    "channel_id": "",
    "comment": "",
    "reseller_name": "",
    "company_name": "",
    "billing_customer_name": "Sarika",
    "billing_last_name": "",
    "billing_address": "29, perumal koil st",
    "billing_address_2": "",
    "billing_isd_code": "",
    "billing_city": "Trichy",
    "billing_pincode": "621103",
    "billing_state": "TamilNadu",
    "billing_country": "India",
    "billing_email": "sdha@ad.com",
    "billing_phone": "8778491312",
    "billing_alternate_phone":"",
    "shipping_is_billing": true,
    "shipping_customer_name": "",
    "shipping_last_name": "",
    "shipping_address": "",
    "shipping_address_2": "",
    "shipping_city": "",
    "shipping_pincode": "",
    "shipping_country": "",
    "shipping_state": "",
    "shipping_email": "",
    "shipping_phone": "",
    "order_items": [
        {
            "name": "Jeans",
            "sku": "sda23",
            "units": 10,
            "selling_price": "900",
            "discount": "",
            "tax": "",
            "hsn": ""
        }
    ],
    "payment_method": "COD",
    "shipping_charges": "",
    "giftwrap_charges": "",
    "transaction_charges": "",
    "total_discount": "",
    "sub_total": 9000,
    "length": 10,
    "breadth": 10,
    "height": 10,
    "weight": 2,
    "ewaybill_no": "",
    "customer_gstin": "",
    "invoice_number":"",
    "order_type":""
}

Response:

{
    "order_id": 404574974,
    "shipment_id": 402780410,
    "status": "NEW",
    "status_code": 1,
    "onboarding_completed_now": 0,
    "awb_code": "",
    "courier_company_id": "",
    "courier_name": ""
}

Generate AWB for Shipment:

{
  "shipment_id": "402780410",
  "courier_id": "",
  "status": ""
 
}

Response:

{
    "awb_assign_status": 1,
    "response": {
        "data": {
            "courier_company_id": 19,
            "awb_code": "658056710",
            "cod": 1,
            "order_id": 404574974,
            "shipment_id": 402780410,
            "awb_code_status": 1,
            "assigned_date_time": {
                "date": "2023-09-13 17:08:51.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "applied_weight": 2,
            "company_id": 3775362,
            "courier_name": "Ecom Express Surface 2kg",
            "child_courier_name": null,
            "freight_charges": 83.04,
            "routing_code": "",
            "rto_routing_code": "",
            "invoice_no": "Retail00002",
            "transporter_id": "07AADCE1344F1Z2",
            "transporter_name": "Ecom Express",
            "shipped_by": {
                "shipper_company_name": "ABS",
                "shipper_address_1": "29, perumal koil st , A Mettur po",
                "shipper_address_2": "",
                "shipper_city": "Perambalur",
                "shipper_state": "Tamil Nadu",
                "shipper_country": "India",
                "shipper_postcode": "621103",
                "shipper_first_mile_activated": 0,
                "shipper_phone": "8903863677",
                "lat": null,
                "long": null,
                "shipper_email": "kpk@abstractit.in",
                "extra_info": {
                    "delhivery_trent_clientware_id": "kartrocket-Perambalur-621103-ABS-3775362-4102434",
                    "delhivery_bellavita_clientware_id": "IDAM SR SURFACE-Perambalur-621103-ABS-3775362-4102434",
                    "delhivery_zomato_2kg_clientware_id": "ZOMATO SR SURFACE-Perambalur-621103-ABS-3775362-4102434",
                    "delhivery_bellavita_2kg_clientware_id": "IDAM SR 2KG-Perambalur-621103-ABS-3775362-4102434",
                    "delhivery_bellavita_5kg_clientware_id": "IDAM SR 5KG-Perambalur-621103-ABS-3775362-4102434"
                },
                "rto_company_name": "ABS",
                "rto_address_1": "29, perumal koil st , A Mettur po",
                "rto_address_2": "",
                "rto_city": "Perambalur",
                "rto_state": "Tamil Nadu",
                "rto_country": "India",
                "rto_postcode": "621103",
                "rto_phone": "8903863677",
                "rto_email": "kpk@abstractit.in"
            }
        }
    },
    "no_pickup_popup": 0,
    "quick_pick": 0
}


Cancel an order:

{
  "ids": [404574974]
}

Response:

{
    "status": 200,
    "message": "Your request to cancel order id 762345 has been taken.The freight amount against the order is blocked and will be added back automatically to your wallet in 3-4 working days subject to confirmation from the courier."
}


Cancel a shipment:

{
"awbs": ["658056710"]
}

Response: 

{
    "message": "Shipment(s) cancellation is in progress. Please wait for 24 hours."
}