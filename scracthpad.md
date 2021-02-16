# Scratchpad

This file contains text snippets you'll need during the workshop to save you typing.

## API Modelling

### Naming

API: 
```
BillPayment
```

Resource:
```
/billPayment
```

API Key:
```
api_key
```

### BillPaymentRequest

Sample Request:
```
{
    "billId": "12345",
    "totalAmount": {
        "unit": "AUD",
        "value": 24.95
    },
    "paymentMethod": {
        "id": "15492654",
        "referredType": "Voucher"
    }
}
```

Schema Name:
```
BillPaymentRequest
```

### BillPaymentResponse

Sample Reponse:
```
{
    "id": "323553",
    "paymentDate": "2020-01-08T12:06:38.230Z"
}
```

Schema Name:
```
BillPaymentResponse
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
