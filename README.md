# migration_service
Request:
{
    "orderFlow":[{
        "type":"5g",
    "orderlist":["20071705","20005791","20073509"],
    "locationlist":["0026301","D031501","20073509"]
    },
	{
	 "type":"TradeIn",
    "orderlist":["20002234","30001281","20001162","20001167"],						
    "locationlist":["E247201","N832401","E248201","E248201"]
	}]
}


Response:
{
    "meta": {
        "timestamp": "2022-10-10T05:47:13.071+00:00",
        "cxpCorrelationId": "2022-10-09T22:47:13.-0700:5d1cefbfd3ac653e:TSDCVPA05VI0465:payload:local"
    },
    "data": {
        "dataSync": [
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_EnforceCallBackInsert",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_InsertEnforceRemarks",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_InsertOrdRemarks",
                "success": 8,
                "failure": 1,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_SAP_5G_3PL_Delivery_Notification",
                "success": 1,
                "failure": 1,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_SAP_5G_Order_Creation_Notification",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_SAP_Recovery_Box_Shipment_Change_Confirmation_Notification",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_SaveAndUpdateOrderPaymentAndCustOrderDetails_Alt",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_SkusAndRdbUpdate",
                "success": 2,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateEnforceOrderInfo",
                "success": 2,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateMultiOrderStatus",
                "success": 2,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateNodeStatusDetails",
                "success": 2,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateOrdLnDetailsAndInsertRemark",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateOrderLineStatusAndRemarks",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateReserveNodeDetails",
                "success": 2,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateServiceItemWriteDetails",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "DMS_UpdateStatusCIB",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "5g",
                "type_def_name": "Generate_PaymentOrder_Gift_Reciepts",
                "success": 4,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_InsertOrdRemarks",
                "success": 12,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_UpdateTradeInItemDetails",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_UpdateTradeInItemDetailsDevr",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_UpdateTradeInItemDetailsGiftCard",
                "success": 1,
                "failure": 0,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_UpdateTradeInItemDetailsPayout",
                "success": 1,
                "failure": 5,
                "in_processing": 0
            },
            {
                "flow_Type": "TradeIn",
                "type_def_name": "DMS_UpdateTradeinItemDetailsPKGRPreIssueCredit",
                "success": 3,
                "failure": 0,
                "in_processing": 0
            }
        ],
        "dataCompare": [
            {
                "flow_Type": "5g",
                "milestones": "DMS_SaveAndUpdateOrderPaymentAndCustOrderDetails_Alt",
                "success": 1,
                "failure": 0
            },
            {
                "flow_Type": "5g",
                "milestones": "DMS_SkusAndRdbUpdate",
                "success": 0,
                "failure": 1
            },
            {
                "flow_Type": "5g",
                "milestones": "SubmitPayment",
                "success": 0,
                "failure": 2
            },
            {
                "flow_Type": "5g",
                "milestones": "FulfillmentRequest",
                "success": 0,
                "failure": 1
            },
            {
                "flow_Type": "TradeIn",
                "milestones": "DMS_UpdateTradeInItemDetailsDevr",
                "success": 0,
                "failure": 3
            }
        ],
        "apiCompare": [
            {
                "flow_Type": "5g",
                "api_type": "SAP_CIB",
                "success": 0,
                "failed": 2
            },
            {
                "flow_Type": "5g",
                "api_type": "ENFORCE_FILL_ORDER",
                "success": 0,
                "failed": 1
            },
            {
                "flow_Type": "5g",
                "api_type": "SAP_RDB",
                "success": 0,
                "failed": 1
            },
            {
                "flow_Type": "5g",
                "api_type": "NAUTILUS_CONFIRM_NOD",
                "success": 0,
                "failed": 1
            },
            {
                "flow_Type": "5g",
                "api_type": "NAUTILUS_RESERVE_NOD",
                "success": 0,
                "failed": 1
            },
            {
                "flow_Type": "TradeIn",
                "api_type": "PAYPAL_PAYOUT",
                "success": 0,
                "failed": 1
            },
            {
                "flow_Type": "TradeIn",
                "api_type": "GC_ACTIVATION",
                "success": 0,
                "failed": 1
            }
        ]
    }
}
