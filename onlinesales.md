| URI                                                                | Method | Returns                                              |
| ------------------------------------------------------------------ | ------ | ---------------------------------------------------- |
| [/onlinesales/v1/verlengverzoekakkoord](#accordeer-verlengverzoek) | `POST` | approve and process extension request                |

## **Accordeer verlengverzoek**

approves and processes extension request

- **URL**

  /onlinesales/v1/verlengverzoekakkoord

- **Method:**

  `POST`

- **Headers**

  **Required:**

  `API-Key`

- **URL Params**

  **Required**

  `betaalkenmerk=[string]` unique identifier for extension request to be approved

  **Optional:**

  none

- **Success Response:**

  - **Code:** 200 <br />
    **Message:** Verlengverzoek voor betaalkenmerk {betaalkenmerk} geaccordeerd <br />

    **Description:** returns no additonal data <br />

    **Content:**

    none

- **Error Response:**

  - **Code:** 406 <br />
    **Message:** Path parameter {betaalkenmerk} empty or missing

  - **Code:** 404 <br />
    **Message:** Verlengverzoek voor betaalkenmerk {betaalkenmerk} is niet gevonden

  - **Code:** 406 <br />
    **Message:** Verlengverzoek voor betaalkenmerk {betaalkenmerk} is ongeldig

  - **Code:** 406 <br />
    **Message:** Voor verlengverzoek voor betaalkenmerk {betaalkenmerk} is het afletterproces reeds gestart

  - **Code:** 406 <br />
    **Message:** Voor verlengverzoek met betaalkenmerk {betaalkenmerk} bestaat reeds een een overeenkomstige pasverkoop

  - **Code:** 406 <br />
    **Message:** Voor verlengverzoek met betaalkenmerk {betaalkenmerk} bestaat reeds een verlengde of vervangen pas
