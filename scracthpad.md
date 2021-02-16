# Scratchpad

This file contains text snippets you'll need during the workshop to save you typing.

## API Modelling

### Naming

API Group: 
```
ShipmentWaiverProject
```

API: 
```
Shipment Waiver
```

Resource:
```
/shipmentWaiver
```

API Key:
```
api_key
```

### ShipmentWaiverRequest

Sample Request:
```
{ 
    "customer" : { 
        "loginid" : "johndoe@tibco.com" 
    },
    "order" : {
        "id" : "1", 
        "shipping amount" : 10, 
        "Total amount" : 100
    }
}
```

Schema Name:
```
ShipmentWaiverInput
```

### ShipmentWaiverResponse

Sample Response:
```
{ 
    "OrderSummary": { 
        "Message": "Shipment Waived Successfully", 
        "Order Number": "318441" 
    } 
}
```

Schema Name:
```
ShipmentWaiverOutput
```









## Exposing an API

### TIBCO Cloud Mashery URL
https://account.cloud.tibco.com/launchtenant/MASHERY

### Package and Plan

Plan Name:
```
BillPayment
```

Plan Name:
```
BillPaymentInternal
```

## Registering for an API

Application Name:
BillPayment

## Orchestrating Services

### Naming

App:
BillPayment

```
GetBillDetails
```

```
DoPayment
```

### BillPayment Test Body

```
{
    "billId": "325366",
    "totalAmount": {
        "unit": "AUD",
        "value": 29.95
    },
    "paymentMethod": {
        "id": "73432381",
        "referredType": "Voucher"
    }
}
```
