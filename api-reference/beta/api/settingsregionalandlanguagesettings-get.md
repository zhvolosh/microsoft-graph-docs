---
title: "Get regionalAndLanguageSettings resource"
description: "Retrieve the properties and relationships of a user's regionalAndLanguageSettings"
author: "jasonbro"
localization_priority: Normal
ms.prod: "settings"
doc_type: apiPageType
---
## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Type             |Permission (from least to most privileged)     |
|-----------------|---------------------------------------------- |
|Read             |User.Read, User.Read.All                       |
|Write            |User.ReadWrite, User.ReadWrite.All             |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /settings/regionalAndLanguageSettings
```

## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.
|Pattern               |Supported |Syntax                                                        |
|----------------------|----------|--------------------------------------------------------------|
|Select                |Yes       |`/?$select=defaultDisplayLanguage,defaultTranslationLanguage` |

## Request headers
| Header       | Value|
|:-----------|:------|
| Authorization  | Bearer {token}. Required.|
| Content-Type   | application/json |

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and [regionalAndLanguageSettings](../resources/settingsregionalandlanguagesettings.md) object in the response body.

## Example

### Example 1: Get the properties of the signed-in user

#### Request


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_regionalAndLanguageSettings"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/me/settings/regionalAndLanguageSettings
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
    "defaultDisplayLanguage": {
        "locale": "en-US",
        "displayName": "English (United States)"
    },
    "authoringLanguages": [
        {
            "locale": "fr-FR",
            "displayName": "French (France)"
        },
        {
            "locale": "de-DE",
            "displayName": "German (Germany)"
        },
    ],
    "defaultTranslationLanguage": {
        "locale": "en-US",
        "displayName": "English (United States)"
    },
    "defaultSpeechInputLanguage": {
        "locale": "en-US",
        "displayName": "English (United States)"
    },
    "defaultRegionalFormat": {
        "locale": "en-GB",
        "displayName": "English (United Kingdom)"
    },
    "regionalFormatOverrides": {
        "calendar": "Gregorian Calendar",
        "firstDayOfWeek": "Sunday",
        "shortDateFormat": "yyyy-MM-dd",
        "longDateFormat": "dddd, MMMM d, yyyy",
        "shortTimeFormat": "HH:mm",
        "longTimeFormat": "h:mm:ss tt",
        "timeZone": "Pacific Standard Time"
    }
}
```

<!--
{
  "type": "#page.annotation",
  "description": "Get regionalAndLanguageSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->