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

## API Development

### Database Connection

Name:
```
custDB
```

Host:
```
mysqltciinstance.ccvct4moy0lt.us-east-1.rds.amazonaws.com
```

Port:
```
3306
```

Database Name:
```
CustomerDB
```

User:
```
******** (Provide by workshop facilitator)
```

Password:
```
******** (Provide by workshop facilitator)
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
