# Getting Started

Dokumen ini dirancang untuk membantu merchant (eCommerce) mengintegrasikan Fastrac sebagai layanan pengiriman barang kepada pelanggan. Dokumen ini berisi spesifikasi API dan web hooks yang dibutuhkan untuk komunikasi antara Fastrac dan merchant. Untuk informasi lebih lanjut, silakan hubungi tim dukungan kami.

## Terms and Conditions for Obtaining an API Key

### API Key Conditions

1. **Limited Access:** API Keys are issued exclusively to Fastrac partners who meet partnership requirements. The API Key is confidential and should only be used for authorized applications or services as specified by Fastrac.
2. **Security:** Every API request requires valid access-key and secret-key headers. Users are fully responsible for safeguarding these keys and preventing unauthorized sharing.
3. **Rate Limiting:** To maintain system stability and prevent abuse, Fastrac may enforce limits on the number of requests per second or per day.
4. **Renewal:** Fastrac reserves the right to update or revoke API Keys based on policy and usage conditions.

### How to Obtain an API Key

1. **Registration:** Users must register as partners on the Fastrac portal, providing necessary business information, and apply for API access.
2. **Verification and Approval:** Fastrac will verify the information and evaluate the eligibility of prospective partners. Upon approval, users will receive instructions for accessing the API Key.
3. **Access Documentation:** Approved users will be provided with their API Key (access-key and secret-key) and detailed documentation on the available endpoints.

## Flow penggunaan

### 1. Authentication and Authorization

- Each API request requires access-key and secret-key in the headers for identifying and authorizing the user.

### 2. Preparing the Request Data

- **Specific Endpoints**: Each API has a dedicated endpoint, such as City, District, Sub-District, and Postal Code.
- **Parameters and Body**: Add the necessary parameters in the URL or body JSON request. For example:

  - GET City requires the province_id parameter.
  - GET District requires the city_id parameter.
  - GET Sub-District requires the district_id parameter.
  - GET Postal Code uses postal_code as a query parameter.

  ### 3. Request Example

  - Each API includes a defined format for requests, using either GET or POST methods, with the endpoint URL, authentication headers, and the required parameters or body.
  - For example, users can apply curl commands while specifying their access-key and secret-key.

### 4. Receiving and Handling the Response

- API responses will include:
  - Success Status: Returns location data, such as the province, city, district, and postal code details as requested.
  - Data Not Found: If the requested data isn’t found, the message "Data not found" will be returned with success: false.
  - Input Errors: If parameters are invalid (e.g., empty or improperly formatted), the error message will indicate the input issue.

### 5. Error Handling

- Each endpoint provides structured responses for success, failure, or exceptions. The system should handle success: false responses and display the error message or message as needed.

### 6. Logging and Monitoring

- Log each request and API response, especially for debugging, monitoring API usage, and adhering to usage policies.

- Flow Pengunaan API
- Rate Limit → Perlu Tim Dev

#### Status Code (Not a priority to implement)

200 - Works fine.
400 - Bad request. Missing required parameters or parameters are not correct
401 - Request lacks authentication (Missing/Invalid Authentication Credentials)
403 - Key doesn't have access to resource (Valid Key but access is not provided)
404 - Not Found
500 - Internal Server Error

## Rate Limit

Rete Limit

## Flowcart

Panduan yang jelas tentang bagaimana API Fastrac beroperasi dan membantu dalam pengembangan serta integrasi sistem.
<https://coda.io/d/_d6byJNi3Vkg/Introduction_suBGEO-t#_lugNu7b8>

&nbsp;
&nbsp;

Kontak Dukungan:

Email: <support@fastrac.id>
