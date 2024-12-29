# GetCID API and PIDMS License Checker API Documentation

Welcome to the **GetCID** and **PIDMS License Checker** API documentation. This guide provides detailed information on integrating our APIs into your applications for seamless Microsoft product activation and license validation.

---

## 🌟 **Overview**

**GetCID** and **PIDMS License Checker** are services designed to assist in the activation and validation of Microsoft products. Our APIs offer developers the tools to automate these processes efficiently.

- **GetCID API**: Automates the generation of Confirmation IDs (CIDs) required for activating Microsoft products.
- **PIDMS License Checker API**: Validates Microsoft license keys to ensure their authenticity and compliance.

For more information, visit our [API Services Page](https://msconfirmationid.com/getcid-api/).

---

## 🚀 **Getting Started**

To begin using our APIs, follow these steps:

1. **Register**: Sign up on our [API Services Page](https://msconfirmationid.com/getcid-api/) to obtain your API key.
2. **Documentation**: Review the API endpoints and parameters detailed below.
3. **Integration**: Implement the APIs into your application using the provided endpoints and sample code.

---

## 🔑 **Authentication**

All API requests require an API key for authentication. Include your API key in the request headers as follows:

```http
Authorization: Bearer YOUR_API_KEY
```

---

## 📘 **API Endpoints**

### **1. GetCID API**

**Endpoint**: `/api/getcid`

**Method**: `POST`

**Description**: Generates a Confirmation ID (CID) for activating Microsoft products.

**Request Parameters**:

- `installation_id` (string): The Installation ID provided by the Microsoft product.
- `product_id` (string): The Product ID of the Microsoft product.

**Response**:

- `confirmation_id` (string): The generated Confirmation ID.

**Example Request**:

```http
POST /api/getcid
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "installation_id": "123456789012345678901234567890123456789012345678901234567",
  "product_id": "XXXXX-XXXXX-XXXXX-XXXXX"
}
```

**Example Response**:

```json
{
  "confirmation_id": "123456789012345678901234567"
}
```

---

### **2. PIDMS License Checker API**

**Endpoint**: `/api/license-check`

**Method**: `POST`

**Description**: Validates a Microsoft license key.

**Request Parameters**:

- `license_key` (string): The Microsoft license key to be validated.

**Response**:

- `valid` (boolean): Indicates whether the license key is valid.
- `product` (string): The associated Microsoft product.
- `expiration_date` (string): The expiration date of the license, if applicable.

**Example Request**:

```http
POST /api/license-check
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "license_key": "XXXXX-XXXXX-XXXXX-XXXXX-XXXXX"
}
```

**Example Response**:

```json
{
  "valid": true,
  "product": "Microsoft Office 2021 Professional Plus",
  "expiration_date": "2025-12-31"
}
```

---

## 💻 **Integration Tips**

- Ensure your API key is kept secure and not exposed in client-side code.
- Handle API responses appropriately, including error handling for invalid requests.
- Monitor your API usage to stay within any rate limits.

---

## 🛠️ **Support and Contact**

If you have any questions or need support, feel free to reach out:

- **Telegram**: [@MicrosoftKeySeller](https://t.me/MicrosoftKeySeller)
- **Email**: [care@msconfirmationid.com](mailto:care@msconfirmationid.com)
- **Skype**: [live:.cid.afc21522bf98cf1b](https://join.skype.com/invite/.cid.afc21522bf98cf1b)
- **Website**: [GetCID Services](https://msconfirmationid.com/get-confirmation-id/)

---

Thank you for choosing our services! 🚀 
