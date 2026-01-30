# API Reference

The TradieScribe API allows you to integrate TradieScribe with your existing tools and workflows.

## Overview

The TradieScribe API is a RESTful API that uses JSON for request and response payloads.

**Base URL:** `https://api.tradiescribe.com/v1`

## Authentication

All API requests require authentication using an API key.

### Getting Your API Key

1. Log in to TradieScribe
2. Navigate to Settings → API
3. Click "Generate API Key"
4. Store your key securely

### Using Your API Key

Include your API key in the `Authorization` header:

```bash
Authorization: Bearer YOUR_API_KEY
```

**Example:**

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
     https://api.tradiescribe.com/v1/projects
```

## Rate Limiting

API requests are rate limited to:
- 1000 requests per hour for standard plans
- 5000 requests per hour for premium plans

Rate limit headers are included in each response:
- `X-RateLimit-Limit`: Total requests allowed
- `X-RateLimit-Remaining`: Requests remaining
- `X-RateLimit-Reset`: Time when limit resets (Unix timestamp)

## Endpoints

### Projects

- [List Projects](endpoints/projects.md#list-projects) - `GET /projects`
- [Get Project](endpoints/projects.md#get-project) - `GET /projects/:id`
- [Create Project](endpoints/projects.md#create-project) - `POST /projects`
- [Update Project](endpoints/projects.md#update-project) - `PUT /projects/:id`
- [Delete Project](endpoints/projects.md#delete-project) - `DELETE /projects/:id`

### Clients

- [List Clients](endpoints/clients.md#list-clients) - `GET /clients`
- [Get Client](endpoints/clients.md#get-client) - `GET /clients/:id`
- [Create Client](endpoints/clients.md#create-client) - `POST /clients`
- [Update Client](endpoints/clients.md#update-client) - `PUT /clients/:id`

### Invoices

- [List Invoices](endpoints/invoices.md#list-invoices) - `GET /invoices`
- [Get Invoice](endpoints/invoices.md#get-invoice) - `GET /invoices/:id`
- [Create Invoice](endpoints/invoices.md#create-invoice) - `POST /invoices`
- [Send Invoice](endpoints/invoices.md#send-invoice) - `POST /invoices/:id/send`

### Quotes

- [List Quotes](endpoints/quotes.md#list-quotes) - `GET /quotes`
- [Get Quote](endpoints/quotes.md#get-quote) - `GET /quotes/:id`
- [Create Quote](endpoints/quotes.md#create-quote) - `POST /quotes`
- [Convert Quote](endpoints/quotes.md#convert-quote) - `POST /quotes/:id/convert`

## Response Format

All responses are returned in JSON format with the following structure:

### Success Response

```json
{
  "success": true,
  "data": {
    // Response data here
  }
}
```

### Error Response

```json
{
  "success": false,
  "error": {
    "code": "ERROR_CODE",
    "message": "Human readable error message"
  }
}
```

## Error Codes

| Code | HTTP Status | Description |
|------|-------------|-------------|
| `UNAUTHORIZED` | 401 | Invalid or missing API key |
| `FORBIDDEN` | 403 | Insufficient permissions |
| `NOT_FOUND` | 404 | Resource not found |
| `VALIDATION_ERROR` | 422 | Request validation failed |
| `RATE_LIMIT_EXCEEDED` | 429 | Too many requests |
| `SERVER_ERROR` | 500 | Internal server error |

## Webhooks

TradieScribe can send webhook notifications for important events.

[Learn more about Webhooks →](webhooks.md)

## SDKs and Libraries

Official SDKs:
- [JavaScript/Node.js](sdks/javascript.md)
- [Python](sdks/python.md)
- [PHP](sdks/php.md)

## Examples

Check out our [API Examples](examples.md) for common use cases and code snippets.

## Support

Need help with the API?
- [API FAQ](api-faq.md)
- [Community Forum](https://community.tradiescribe.com)
- Email: api-support@tradiescribe.com
