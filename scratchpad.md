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

## API Implementation

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

### Implement an App

App Name:
```
ShipmentWaiverApp
```

MySQL Activity Name:
```
FetchCustomerDetails
```

MySQL Activity SQL Statement:
```
select * from customer_details where Email=?para_email;
```

Log Message Activity Name:
```
LogCRMOutput
```

Input Message:
```
$activity[FetchCustomerDetails].Output.records[0].FirstName
```

### Import App and Enable it as Cloud Mesh 

App Name:
```
CreateMarketoLeadFlow
```

## Putting all together - Import an Prebuilt Flogo App 

App Name:
```
ShipmentWaiverFlow
```

LogMarketoOutput Message mapping:
```
string.tostring($activity[InvokeMarketoService].responseCodes["200"])
```
### Testing the Flogo App

loginid:
```
"jtamboli@tibco.com"
```

order id:
```
"4"
```

Shipping amount:
```
10
```

Total amount:
```
100
```

## Deploy and test the App 

Sample Request:
```
{
    "customer": {
        "loginid": "jtamboli@tibco.com"
    },
    "order": {
        "id": "001",
        "Total amount": 100,
        "shipping amount": 10
    }
}
```


# Optional

## Mashery-Exposing an API

API Definition:
```
ShipmentWaiver
```

Package Name:
```
Basic Package
```

Plan Name:
```
Standard Plan
```

### TIBCO Cloud Mashery URL
https://account.cloud.tibco.com/launchtenant/MASHERY


## Mashery-Manage an API

Public API URL:
```
processOrder/v1/shipmentwaiver
```

## Mashery-Add user Application

Application Name:
```
ShipmentWaiver_APP
```

 ## Mashery-Test Application

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
