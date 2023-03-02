| URI                                                                | Method | Returns                                              |
| ------------------------------------------------------------------ | ------ | ---------------------------------------------------- |
| [/fulfillment/v1/fulfillmentstatus](#set-fulfillment-status)       | `POST` | set the fulfillmentstatus of a fulfillmentorder      |

## **Set fulfillment status**

 json data about the processing status of a fulfillment order

- **URL**

  /fulfillment/v1/fulfillmentstatus

- **Method:**

  `POST`

- **Headers**

  **Required:**

  `API-Key` 

- **URL Params**

  None

- **Data Params**

  Exactly one combination of the root attributes in the JSON body below. ordernr and statuscode attributes are mandatory. Description is optional but recommended.

  ```javascript
  {
    "ordernr": "11",
    "statuscode": "10",
    "description": "Order received and validated, fulfillment planned for today"
  }
  ```

- **Success Response:**

  - **Code:** 200 <br />
    **Message:** Order: 12345 status updated succesfully <br />
    **Content:** <br /><br />

- **Error Response:**

  - **Code:** 400 <br />
    **Message:** No content

  - **Code:** 400 <br />
    **Message:** Missing field in order {Ordernr}

  - **Code:** 400 <br />
    **Message:** Missing field in order {Statuscode}

  - **Code:** 401 <br />
    **Message:** Unknown ordernr
