



##### [Back to Platform docs](./README.md)

## Customer Methods
Authentication Service
* [verify](#verify)
* [resendPaymentRequest](#resendpaymentrequest)
* [createOrder](#createorder)
* [link](#link)
* [unlink](#unlink)
* [getAccessToken](#getaccesstoken)
* [renewAccessToken](#renewaccesstoken)
* [refund](#refund)
* [refundStatus](#refundstatus)
* [getSchemes](#getschemes)
* [checkEligibility](#checkeligibility)



## Methods with example and description


### verify
Verify Customer




```java
customer.verify(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [VerifyCustomer](#VerifyCustomer) | yes | Request body |


Use this API to verify the customer based on  mobile number and countryCode.

*Returned Response:*




[VerifyCustomerSuccess](#VerifyCustomerSuccess)

Success. Returns a JSON object as shown below. Refer `VerifyCustomerSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; VerifyCustomerEnabledResponseExample</i></summary>

```json
{
  "value": {
    "status": "ENABLED",
    "userStatus": "USER_AUTHORISED",
    "message": "Kindly proceed to complete your order"
  }
}
```
</details>

<details>
<summary><i>&nbsp; VerifyCustomerDisabledResponseExample</i></summary>

```json
{
  "value": {
    "status": "DISABLED",
    "userStatus": "CREDIT_EXAHUSTED",
    "message": "Order value exceeds the available limit of ₹36,452"
  }
}
```
</details>

</details>









---


### resendPaymentRequest
Resend Payment Request




```java
customer.resendPaymentRequest(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [ResendPaymentRequest](#ResendPaymentRequest) | yes | Request body |


Use this API to resend payment request to user

*Returned Response:*




[CreateTransactionSuccess](#CreateTransactionSuccess)

Success. Returns a JSON object as shown below. Refer `CreateTransactionSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; redirectUrl</i></summary>

```json
"https://account.potleex0.de/auth/login?onboardingToken=e738521b-a763-460d-a440-d9570e79be47&redirectUrl=https://local.potleex0.de:3003/callback?apiKey=0c8e7bbf-6c0c-41b1-8a37-7e066e8fbd4a&apiSecret=48a7d96f46868f78297be845b6afb5da50893d0b&domain=https://api.potleex0.de"
```
</details>

<details>
<summary><i>&nbsp; message</i></summary>

```json
"Payment Authorised"
```
</details>

<details>
<summary><i>&nbsp; userStatus</i></summary>

```json
"PAYMENT_AUTHORISED"
```
</details>

</details>









---


### createOrder
Create Order




```java
customer.createOrder(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [CreateTransaction](#CreateTransaction) | yes | Request body |


Use this API to create transaction for user

*Returned Response:*




[CreateTransactionSuccess](#CreateTransactionSuccess)

Success. Returns a JSON object as shown below. Refer `CreateTransactionSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; CreateTransactionResponseExample</i></summary>

```json
{
  "value": {
    "redirectUrl": "https://account.potlee.co.in/auth/login?onboardingToken=e738521b-a763-460d-a440-d9570e79be47&redirectUrl=https://url.merchant.com/callback",
    "message": "Payment Authorised",
    "userStatus": "PAYMENT_AUTHORISED"
  }
}
```
</details>

</details>









---


### link
Link account




```java
customer.link(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [LinkAccount](#LinkAccount) | yes | Request body |


Use this API to link account with merchant

*Returned Response:*




[LinkAccountSuccess](#LinkAccountSuccess)

Success. Returns a JSON object as shown below. Refer `LinkAccountSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; redirectUrl</i></summary>

```json
"https://account.potlee.co.in/auth/login?linkingToken=1245rtfyg765"
```
</details>

</details>









---


### unlink
Unlink account




```java
customer.unlink(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [UnlinkAccount](#UnlinkAccount) | yes | Request body |


Use this API to unlink account from merchant

*Returned Response:*




[UnlinkAccountSuccess](#UnlinkAccountSuccess)

Success. Returns a JSON object as shown below. Refer `UnlinkAccountSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; success</i></summary>

```json
true
```
</details>

</details>









---


### getAccessToken
Get Access Token




```java
customer.getAccessToken() {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  



Use this API to get access token

*Returned Response:*




[GetAccessTokenResponse](#GetAccessTokenResponse)

Success. Returns a JSON object as shown below. Refer `GetAccessTokenResponse` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; success</i></summary>

```json
true
```
</details>

<details>
<summary><i>&nbsp; accessToken</i></summary>

```json
"oa-0a7a064dd15ef22fe002946f90c1e7b22eea47de"
```
</details>

<details>
<summary><i>&nbsp; refreshToken</i></summary>

```json
"oa-d2f33b6be9957050386be051501b84b008f5ef6f"
```
</details>

<details>
<summary><i>&nbsp; tokenExpireAt</i></summary>

```json
"2023-06-27T09:43:07.818Z"
```
</details>

<details>
<summary><i>&nbsp; tokenExpiryIn</i></summary>

```json
"600"
```
</details>

<details>
<summary><i>&nbsp; refreshTokenExpiryAt</i></summary>

```json
"2023-06-27T10:33:07.822Z"
```
</details>

<details>
<summary><i>&nbsp; refreshTokenExpiryIn</i></summary>

```json
"3600"
```
</details>

<details>
<summary><i>&nbsp; scope</i></summary>

```json
[
  "transaction"
]
```
</details>

</details>









---


### renewAccessToken
Renew Access Token




```java
customer.renewAccessToken(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [RefreshTokenRequest](#RefreshTokenRequest) | yes | Request body |


Use this API to renew access token

*Returned Response:*




[RefreshTokenResponse](#RefreshTokenResponse)

Success. Returns a JSON object as shown below. Refer `RefreshTokenResponse` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; success</i></summary>

```json
true
```
</details>

<details>
<summary><i>&nbsp; accessToken</i></summary>

```json
"oa-de1496c16c91c45396ba87a888eed20fb223995d"
```
</details>

<details>
<summary><i>&nbsp; tokenExpireAt</i></summary>

```json
"2023-06-26T19:23:46.977Z"
```
</details>

<details>
<summary><i>&nbsp; tokenExpiryIn</i></summary>

```json
"600"
```
</details>

</details>









---


### refund
Refund customer order amount




```java
customer.refund(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [Refund](#Refund) | yes | Request body |


Use this API to verify the refund customer order amount

*Returned Response:*




[RefundResponse](#RefundResponse)

Success. Returns a JSON object as shown below. Refer `RefundResponse` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; status</i></summary>

```json
"SUCCESS"
```
</details>

<details>
<summary><i>&nbsp; message</i></summary>

```json
"Refund request has been successfully recorded."
```
</details>

<details>
<summary><i>&nbsp; refundId</i></summary>

```json
"R123"
```
</details>

<details>
<summary><i>&nbsp; transactionId</i></summary>

```json
"TXN1234567dsfg"
```
</details>

</details>









---


### refundStatus
Refund status




```java
customer.refundStatus( refundId,  orderId) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |   
| refundId | String? | no | This is the refund ID |   
| orderId | String? | no | This is the order ID |  



Use this API to fetch the refund status

*Returned Response:*




[RefundStatus](#RefundStatus)

Success. Returns a JSON object as shown below. Refer `RefundStatus` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; orderId</i></summary>

```json
"PM-28"
```
</details>

<details>
<summary><i>&nbsp; userId</i></summary>

```json
"c004a863-bce5-492b-b7aa-ba2890bc9e25"
```
</details>

<details>
<summary><i>&nbsp; merchantId</i></summary>

```json
"3e0cf7da-ad5f-4c99-a9e7-49cad484ef37"
```
</details>

<details>
<summary><i>&nbsp; lenderId</i></summary>

```json
"f622b3e8-c797-434d-948f-d0fda56e3db6"
```
</details>

<details>
<summary><i>&nbsp; refund</i></summary>

```json
[
  {
    "id": "10122313672606485999",
    "loanAccountNumber": "CASHe-1686764747795",
    "orderItems": {
      "list": [
        {
          "sku": "1",
          "rate": "1",
          "category": "1",
          "quantity": 1
        }
      ]
    },
    "amount": 3000,
    "status": "SUCCESS",
    "processedDate": "2023-06-14T17:44:28.052Z",
    "createdAt": "2023-06-14T17:44:28.052Z"
  }
]
```
</details>

</details>









---


### getSchemes
Fetch schemes




```java
customer.getSchemes(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [GetSchemesRequest](#GetSchemesRequest) | yes | Request body |


Use this API to fetch available schemes for user order.

*Returned Response:*




[GetSchemesSuccess](#GetSchemesSuccess)

Success. Returns a JSON object as shown below. Refer `GetSchemesSuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; userId</i></summary>

```json
"bf94b96a-1a15-406b-8d2f-0b37bfe47732"
```
</details>

<details>
<summary><i>&nbsp; lenders</i></summary>

```json
[
  {
    "slug": "cashe",
    "name": "CASHe",
    "title": "CASHe",
    "subtitle": "Bhanix Finance and Investment Limited",
    "isDefault": false,
    "logoUrl": "https://cdn.pixelbin.io/v2/potlee/original/public/lenders/lenderLogo/v2/512h-logo/cashe-logo.png",
    "amount": 5000,
    "paymentOptions": {
      "emis": [
        {
          "id": 62,
          "title": "3 Months - EMIs",
          "subtitle": "CASHe Shop 3EMI (PaymentGateway)",
          "description": "3 Months - No cost EMIs",
          "tenure": 3,
          "interest": 0,
          "processingFee": 75,
          "amount": 1692,
          "emiSchedule": [
            {
              "installmentNo": 1,
              "installmentAmount": 1741,
              "dueDate": "2023-12-22T12:00:00.000+00:00",
              "dueAmount": 3334
            },
            {
              "installmentNo": 2,
              "installmentAmount": 1666,
              "dueDate": "2024-01-22T12:00:00.000+00:00",
              "dueAmount": 1668
            },
            {
              "installmentNo": 3,
              "installmentAmount": 1666,
              "dueDate": "2024-02-22T12:00:00.000+00:00",
              "dueAmount": 2
            }
          ],
          "isDefault": false
        }
      ],
      "payLater": {
        "id": 1,
        "title": "PayLater",
        "subtitle": "CASHe_PayLater",
        "description": "Customer can pay after 30days",
        "tenure": 1,
        "interest": 0,
        "processingFee": 0,
        "amount": 5000,
        "emiSchedule": null,
        "isDefault": true
      }
    }
  }
]
```
</details>

</details>









---


### checkEligibility
Check Credit Eligibility




```java
customer.checkEligibility(body body) {
  //use response
}
```



| Argument  |  Type  | Required | Description |
| --------- | -----  | -------- | ----------- | 
| organizationId | String | yes | This is organizationId |  
| body | [CheckEligibilityRequest](#CheckEligibilityRequest) | yes | Request body |


Use this API to pre approve by checking the customer's credit eligibility based on mobile number and countryCode and vintage data of monthly transactions.

*Returned Response:*




[EligibilitySuccess](#EligibilitySuccess)

Success. Returns a JSON object as shown below. Refer `EligibilitySuccess` for more details.




<details>
<summary><i>&nbsp; Examples:</i></summary>


<details>
<summary><i>&nbsp; $ref</i></summary>

```json
"#/components/examples/EligibilitySuccess"
```
</details>

</details>









---



### Schemas

 
 
 #### [RefundResponse](#RefundResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | message | String? |  yes  |  |
 | transactionId | String? |  yes  |  |
 | refundId | String? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [UserSchema](#UserSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | email | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | dob | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | profilePicUrl | String? |  yes  |  |
 | isEmailVerified | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |

---


 
 
 #### [count](#count)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | totalUsers | String? |  yes  |  |

---


 
 
 #### [FilterByDate](#FilterByDate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | startDate | String? |  yes  |  |
 | endDate | String? |  yes  |  |

---


 
 
 #### [LenderCount](#LenderCount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | totalLenders | String? |  yes  |  |

---


 
 
 #### [LenderSchema](#LenderSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |

---


 
 
 #### [TotalUsersPerLender](#TotalUsersPerLender)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[Filters](#Filters)> |  no  |  |
 | page | [PageResponse](#PageResponse) |  no  |  |
 | lenderList | ArrayList<[TotalUsersPerLenderData](#TotalUsersPerLenderData)> |  no  |  |

---


 
 
 #### [TotalUsersPerLenderData](#TotalUsersPerLenderData)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |
 | totalUsers | String? |  yes  |  |

---


 
 
 #### [TotalUserByLender](#TotalUserByLender)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | count | String? |  yes  |  |

---


 
 
 #### [UsersByLender](#UsersByLender)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | email | String? |  yes  |  |
 | name | String? |  yes  |  |

---


 
 
 #### [ErrorResponse](#ErrorResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |
 | info | String? |  yes  |  |
 | code | String? |  yes  |  |
 | requestId | String? |  yes  |  |
 | meta | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [EditProfileRequest](#EditProfileRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | String? |  yes  |  |
 | lastName | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | email | String? |  yes  |  |
 | gender | String? |  yes  |  |
 | dob | String? |  yes  |  |
 | registrationToken | String? |  yes  |  |

---


 
 
 #### [VerifyOtpRequest](#VerifyOtpRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | requestId | String |  no  |  |
 | otp | String |  no  |  |
 | captchaCode | String? |  yes  |  |
 | androidHash | String? |  yes  |  |
 | referralCode | String? |  yes  |  |
 | onboardingToken | String? |  yes  |  |

---


 
 
 #### [SendMobileOtpRequest](#SendMobileOtpRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String |  no  |  |
 | mobile | String |  no  |  |
 | captchaCode | String? |  yes  |  |
 | androidHash | String? |  yes  |  |
 | force | String? |  yes  |  |

---


 
 
 #### [ReSendMobileOtpRequest](#ReSendMobileOtpRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | captchaCode | String? |  yes  |  |
 | token | String |  no  |  |
 | androidHash | String? |  yes  |  |

---


 
 
 #### [SendOtpRequest](#SendOtpRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | captchaCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |

---


 
 
 #### [ApplicationUser](#ApplicationUser)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |

---


 
 
 #### [SendOtpResponse](#SendOtpResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | resendTimer | Integer? |  yes  |  |
 | resendToken | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | requestId | String? |  yes  |  |
 | message | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | email | String? |  yes  |  |
 | resendEmailToken | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | userExists | Boolean? |  yes  |  |

---


 
 
 #### [EmailUpdate](#EmailUpdate)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | email | String? |  yes  |  |

---


 
 
 #### [UserUpdateRequest](#UserUpdateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | firstName | Object? |  yes  |  |
 | lastName | Object? |  yes  |  |
 | countryCode | String |  no  |  |
 | mobile | String |  no  |  |
 | email | Object? |  yes  |  |
 | gender | Object? |  yes  |  |
 | dob | Object? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | profilePictureUrl | Object? |  yes  |  |
 | isEmailVerified | Boolean? |  yes  |  |

---


 
 
 #### [LenderUpdateRequest](#LenderUpdateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [ProfileEditSuccess](#ProfileEditSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | resendEmailToken | String? |  yes  |  |
 | userExists | Boolean? |  yes  |  |
 | verifyEmailLink | Boolean? |  yes  |  |
 | verifyEmailOtp | Boolean? |  yes  |  |
 | verifyMobileOtp | Boolean? |  yes  |  |
 | email | String? |  yes  |  |
 | requestId | String? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | message | String? |  yes  |  |
 | resendTimer | Integer? |  yes  |  |
 | resendToken | String? |  yes  |  |

---


 
 
 #### [LoginSuccess](#LoginSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | requestId | String? |  yes  |  |
 | registerToken | String? |  yes  |  |

---


 
 
 #### [VerifyOtpSuccess](#VerifyOtpSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |
 | userExists | Boolean? |  yes  |  |
 | isNew | Boolean? |  yes  |  |

---


 
 
 #### [LogoutSuccess](#LogoutSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | logout | Boolean? |  yes  |  |

---


 
 
 #### [OtpSuccess](#OtpSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | resendTimer | Integer? |  yes  |  |
 | resendToken | String? |  yes  |  |
 | registerToken | String? |  yes  |  |
 | success | Boolean? |  yes  |  |
 | requestId | String? |  yes  |  |
 | message | String? |  yes  |  |
 | mobile | String? |  yes  |  |
 | isNew | Boolean? |  yes  |  |
 | countryCode | String? |  yes  |  |
 | otpLength | Double? |  yes  |  |

---


 
 
 #### [SessionListSuccess](#SessionListSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sessions | ArrayList<String>? |  yes  |  |

---


 
 
 #### [VerifyMobileOTPSuccess](#VerifyMobileOTPSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | user | [UserSchema](#UserSchema)? |  yes  |  |

---


 
 
 #### [Location](#Location)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | latitude | Double? |  yes  |  |
 | longitude | Double? |  yes  |  |

---


 
 
 #### [OrderAddress](#OrderAddress)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | line1 | String? |  yes  |  |
 | line2 | String? |  yes  |  |
 | city | String? |  yes  |  |
 | state | String? |  yes  |  |
 | country | String? |  yes  |  |
 | pincode | String? |  yes  |  |
 | type | String? |  yes  |  |
 | geoLocation | [Location](#Location)? |  yes  |  |

---


 
 
 #### [CustomerObject](#CustomerObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String? |  yes  |  |
 | mobile | String |  no  |  |
 | uid | String |  no  |  |
 | email | String? |  yes  |  |
 | firstname | String? |  yes  |  |
 | middleName | String? |  yes  |  |
 | lastName | String? |  yes  |  |

---


 
 
 #### [Order](#Order)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | valueInPaise | Integer |  no  |  |
 | uid | String |  no  |  |
 | items | ArrayList<[Items](#Items)>? |  yes  |  |
 | shippingAddress | [OrderAddress](#OrderAddress)? |  yes  |  |
 | billingAddress | [OrderAddress](#OrderAddress)? |  yes  |  |

---


 
 
 #### [OrderUid](#OrderUid)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | valueInPaise | Integer? |  yes  |  |
 | uid | String |  no  |  |
 | items | ArrayList<[Items](#Items)>? |  yes  |  |
 | shippingAddress | [OrderAddress](#OrderAddress)? |  yes  |  |
 | billingAddress | [OrderAddress](#OrderAddress)? |  yes  |  |

---


 
 
 #### [CustomerMeta](#CustomerMeta)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ip | String |  no  |  |
 | appVersion | String |  no  |  |
 | appIdentifier | String? |  yes  |  |
 | customerUserAgent | String? |  yes  |  |
 | deviceId | String |  no  |  |

---


 
 
 #### [Device](#Device)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | ipAddress | String |  no  |  |
 | userAgent | String |  no  |  |
 | latitude | Double? |  yes  |  |
 | longitude | Double? |  yes  |  |

---


 
 
 #### [VerifyCustomer](#VerifyCustomer)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | order | [Order](#Order) |  no  |  |
 | device | [Device](#Device) |  no  |  |
 | meta | HashMap<String,Object>? |  yes  |  |
 | fetchLimitOptions | Boolean? |  yes  |  |
 | fetchPlans | Boolean? |  yes  |  |

---


 
 
 #### [CreateTransaction](#CreateTransaction)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | autoCapture | Boolean? |  yes  | If autoCapture is true, transaction will automatically be created without requiring the user to login, provided that other details such as user session, emiTenure and lenderId are valid. Default value is false. User session has to be passed in session field in case of SDK integration or in Cookie header with key user.session in case of direct integration. |
 | redirectUrl | String |  no  | User will be redirected back to this URL after a successful or a failed transaction. |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | order | [Order](#Order) |  no  |  |
 | device | [Device](#Device) |  no  |  |
 | meta | HashMap<String,Object>? |  yes  | Any additional details |
 | emiTenure | Integer? |  yes  | EMI tenure selected by customer |
 | lenderSlug | String? |  yes  | slug of lender selected by customer |
 | consents | ArrayList<[Consents](#Consents)>? |  yes  | Consent for AUTO_DISBURSAL is mandatory while calling createOrder API. |

---


 
 
 #### [ResendPaymentRequest](#ResendPaymentRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | autoCapture | Boolean? |  yes  |  |
 | redirectUrl | String? |  yes  |  |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | order | [OrderUid](#OrderUid) |  no  |  |

---


 
 
 #### [VerifyCustomerSuccess](#VerifyCustomerSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String |  no  | Indicates whether a user is allowed to perform the transaction or not |
 | userStatus | String |  no  | Represents the status of the user for transaction eligibility |
 | message | String |  no  | Message to be displayed to the user |
 | schemes | ArrayList<[SchemeResponse](#SchemeResponse)>? |  yes  | An array of possible schemes of lenders available for a transaction. |
 | limit | [LimitResponse](#LimitResponse)? |  yes  | Limit details of available and possible lenders for a transaction. |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [CreateTransactionSuccess](#CreateTransactionSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | chargeToken | String? |  yes  | A unique token for completing the transaction. Charge token is received only if a valid user session is passed in request and auto capture is false. ASP merchants do not receive charge token. |
 | redirectUrl | String? |  yes  | URL to which the user is redirected to complete the transaction. This is received only when transaction cannot be created without requiring the user to login on Potlee, for example, when autoCapture is false or user session is invalid. |
 | message | String |  no  | A message or information related to the transaction. |
 | transactionId | String? |  yes  | A unique identifier for the transaction. This is received only if session is passed and auto capture is true in request. ASP merchants do not receive transaction ID in this response. |
 | status | String? |  yes  | Indicates transaction status in case of auto disbursal. |
 | userStatus | String? |  yes  | Represents the status of the user for transaction eligibility |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [SupportDocuments](#SupportDocuments)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | fileName | String? |  yes  |  |
 | fileUrl | String? |  yes  |  |

---


 
 
 #### [CreateTicketResponse](#CreateTicketResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | serviceRequestId | String? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [CreateTicket](#CreateTicket)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | String |  no  |  |
 | transactionId | String? |  yes  |  |
 | description | String |  no  |  |
 | documents | ArrayList<[SupportDocuments](#SupportDocuments)>? |  yes  |  |

---


 
 
 #### [InitiateTransactions](#InitiateTransactions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [GetMobileFromToken](#GetMobileFromToken)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [GetDataFromToken](#GetDataFromToken)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [MerchantDetails](#MerchantDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | website | String? |  yes  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [InitiateTransactionsSuccess](#InitiateTransactionsSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | chargeToken | String |  no  |  |
 | session | String? |  yes  |  |
 | expiry | String? |  yes  |  |
 | hash | String? |  yes  |  |
 | order | [Order](#Order)? |  yes  |  |
 | isAsp | Boolean? |  yes  |  |
 | merchant | [MerchantDetails](#MerchantDetails)? |  yes  |  |

---


 
 
 #### [RetrieveMobileFromToken](#RetrieveMobileFromToken)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String |  no  |  |
 | mobile | String |  no  |  |

---


 
 
 #### [CreateDashboardTemplateRequest](#CreateDashboardTemplateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | version | String |  no  |  |
 | isDefault | Boolean? |  yes  |  |
 | sections | ArrayList<[TemplateSections](#TemplateSections)> |  no  |  |

---


 
 
 #### [TemplateSections](#TemplateSections)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sequence | Integer |  no  |  |
 | isAvailableInMobile | Boolean |  no  |  |
 | isAvailableInDesktop | Boolean |  no  |  |
 | component | [TemplateComponent](#TemplateComponent) |  no  |  |

---


 
 
 #### [TemplateComponent](#TemplateComponent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | description | String |  no  |  |
 | isAvailableInDesktop | Boolean? |  yes  |  |
 | partnerApplications | ArrayList<[PartnerApplications](#PartnerApplications)>? |  yes  |  |
 | banners | ArrayList<[Banners](#Banners)>? |  yes  |  |
 | tips | ArrayList<[Tips](#Tips)>? |  yes  |  |

---


 
 
 #### [PartnerApplications](#PartnerApplications)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | description | String? |  yes  |  |
 | urlPath | String? |  yes  |  |
 | urlTarget | String? |  yes  |  |
 | imageUrl | String |  no  |  |
 | sequence | Integer? |  yes  |  |

---


 
 
 #### [Offerings](#Offerings)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | description | String? |  yes  |  |
 | urlPath | String? |  yes  |  |
 | urlTarget | String? |  yes  |  |
 | imageUrl | String |  no  |  |
 | sequence | Integer? |  yes  |  |
 | gradient | ArrayList<String> |  no  |  |

---


 
 
 #### [Banners](#Banners)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | imageUrl | String |  no  |  |
 | action | [ActionSchema](#ActionSchema)? |  yes  |  |

---


 
 
 #### [Tips](#Tips)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | urlPath | String |  no  |  |
 | urlTarget | String? |  yes  |  |
 | imageUrl | String? |  yes  |  |
 | sequence | Integer? |  yes  |  |

---


 
 
 #### [DashboardTemplateResponse](#DashboardTemplateResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String? |  yes  |  |
 | version | String? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | sections | ArrayList<[SectionSchema](#SectionSchema)> |  no  |  |

---


 
 
 #### [SectionSchema](#SectionSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | partners | ArrayList<[PartnerApplicationsResponse](#PartnerApplicationsResponse)>? |  yes  |  |
 | banners | ArrayList<[BannersResponse](#BannersResponse)>? |  yes  |  |
 | tips | ArrayList<[TipsResponse](#TipsResponse)>? |  yes  |  |

---


 
 
 #### [PartnerApplicationsResponse](#PartnerApplicationsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String |  no  |  |
 | description | String? |  yes  |  |
 | action | [ActionSchema](#ActionSchema) |  no  |  |
 | imageUrl | String |  no  |  |

---


 
 
 #### [OfferingsResponse](#OfferingsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String |  no  |  |
 | description | String? |  yes  |  |
 | action | [ActionSchema](#ActionSchema) |  no  |  |
 | imageUrl | String |  no  |  |
 | gradient | ArrayList<String> |  no  |  |

---


 
 
 #### [BannersResponse](#BannersResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | action | [ActionSchema](#ActionSchema)? |  yes  |  |
 | imageUrl | String |  no  |  |

---


 
 
 #### [TipsSection](#TipsSection)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tips | ArrayList<[TipsResponse](#TipsResponse)>? |  yes  |  |
 | categories | ArrayList<[TipsCategories](#TipsCategories)>? |  yes  |  |
 | action | [ActionSchema](#ActionSchema)? |  yes  |  |

---


 
 
 #### [TipsResponse](#TipsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | category | String? |  yes  |  |
 | description | String? |  yes  |  |
 | action | [ActionSchema](#ActionSchema) |  no  |  |
 | imageUrl | String? |  yes  |  |

---


 
 
 #### [TipsCategories](#TipsCategories)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | title | String |  no  |  |

---


 
 
 #### [ActionSchema](#ActionSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | page | [PageSchema](#PageSchema)? |  yes  |  |
 | popup | [PageSchema](#PageSchema)? |  yes  |  |

---


 
 
 #### [UpdateDashboardTemplateRequest](#UpdateDashboardTemplateRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | version | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | sections | ArrayList<[UpdateTemplateSections](#UpdateTemplateSections)>? |  yes  |  |

---


 
 
 #### [UpdateTemplateSections](#UpdateTemplateSections)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | sequence | Integer? |  yes  |  |
 | isAvailableInMobile | Boolean? |  yes  |  |
 | isAvailableInDesktop | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | component | [UpdateTemplateComponent](#UpdateTemplateComponent)? |  yes  |  |

---


 
 
 #### [UpdateTemplateComponent](#UpdateTemplateComponent)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | isAvailableInDesktop | Boolean? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | partners | ArrayList<[UpdatePartnerApplications](#UpdatePartnerApplications)>? |  yes  |  |
 | banners | ArrayList<[UpdateBanners](#UpdateBanners)>? |  yes  |  |
 | tips | ArrayList<[UpdateTips](#UpdateTips)>? |  yes  |  |

---


 
 
 #### [UpdatePartnerApplications](#UpdatePartnerApplications)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | action | HashMap<String,Object>? |  yes  |  |
 | imageUrl | String? |  yes  |  |
 | sequence | Integer? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [UpdateOfferings](#UpdateOfferings)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | urlPath | String? |  yes  |  |
 | urlTarget | String? |  yes  |  |
 | imageUrl | String? |  yes  |  |
 | sequence | Integer? |  yes  |  |
 | gradient | ArrayList<String>? |  yes  |  |

---


 
 
 #### [UpdateBanners](#UpdateBanners)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | imageUrl | String? |  yes  |  |
 | action | HashMap<String,Object>? |  yes  |  |
 | sequence | Integer? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [UpdateTips](#UpdateTips)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |
 | name | String? |  yes  |  |
 | description | String? |  yes  |  |
 | imageUrl | String? |  yes  |  |
 | action | HashMap<String,Object>? |  yes  |  |
 | sequence | Integer? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [NavigationsMobileResponse](#NavigationsMobileResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | tabs | ArrayList<[TabsSchema](#TabsSchema)> |  no  |  |
 | profileSections | ArrayList<[ProfileSectionSchema](#ProfileSectionSchema)> |  no  |  |

---


 
 
 #### [TabsSchema](#TabsSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  |  |
 | page | [PageSchema](#PageSchema) |  no  |  |
 | icon | String |  no  |  |
 | activeIcon | String |  no  |  |
 | active | Boolean |  no  |  |

---


 
 
 #### [PageSchema](#PageSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | link | String? |  yes  |  |
 | type | [PageType](#PageType)? |  yes  |  |
 | params | HashMap<String,ArrayList<String>>? |  yes  |  |
 | query | HashMap<String,String>? |  yes  |  |

---


 
 
 #### [ProfileSectionSchema](#ProfileSectionSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  |  |
 | navigations | ArrayList<[ProfileNavigationSchema](#ProfileNavigationSchema)> |  no  |  |
 | active | Boolean |  no  |  |

---


 
 
 #### [ProfileNavigationSchema](#ProfileNavigationSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | title | String |  no  |  |
 | description | String? |  yes  |  |
 | icon | String |  no  |  |
 | type | String |  no  |  |
 | action | [ActionSchema](#ActionSchema)? |  yes  |  |
 | active | Boolean? |  yes  |  |

---


 
 
 #### [SendPNSRegisterRequest](#SendPNSRegisterRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | deviceId | String |  no  |  |
 | deviceType | String |  no  |  |
 | token | String |  no  |  |

---


 
 
 #### [PNSRegisterResponse](#PNSRegisterResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | Boolean? |  yes  |  |
 | message | String? |  yes  |  |

---


 
 
 #### [FaqResponse](#FaqResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | categories | ArrayList<[CategorySchema](#CategorySchema)>? |  yes  |  |

---


 
 
 #### [CategorySchema](#CategorySchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | String |  no  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | logo | String? |  yes  |  |
 | questions | ArrayList<[QuestionSchema](#QuestionSchema)>? |  yes  |  |

---


 
 
 #### [QuestionSchema](#QuestionSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | uid | String |  no  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | displayOrder | Integer? |  yes  |  |
 | canRaiseRequest | Boolean? |  yes  |  |

---


 
 
 #### [SupportCategories](#SupportCategories)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | kind | String? |  yes  |  |
 | display | String? |  yes  |  |

---


 
 
 #### [SupportCategoriesResponse](#SupportCategoriesResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | categories | ArrayList<[SupportCategories](#SupportCategories)>? |  yes  |  |

---


 
 
 #### [SanctionLetterResponse](#SanctionLetterResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | sanctionedLetterFileUrl | String |  no  |  |

---


 
 
 #### [KfsDocumentResponse](#KfsDocumentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | kfsFileUrl | String |  no  |  |

---


 
 
 #### [UserWhiteListedResponse](#UserWhiteListedResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |

---


 
 
 #### [UserConsentRequest](#UserConsentRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | consents | ArrayList<String>? |  yes  |  |

---


 
 
 #### [Consents](#Consents)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String? |  yes  |  |
 | text | String? |  yes  |  |
 | purpose | String? |  yes  | If consent type is AUTO_DISBURSAL, purpose will be uid of order. |

---


 
 
 #### [UserConsentRequestV2](#UserConsentRequestV2)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | consents | ArrayList<[Consents](#Consents)>? |  yes  |  |

---


 
 
 #### [UserConsentResponse](#UserConsentResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |

---


 
 
 #### [UserKycSteps](#UserKycSteps)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | index | String? |  yes  |  |
 | name | String? |  yes  |  |
 | rules | HashMap<String,Object>? |  yes  |  |
 | active | Boolean? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |

---


 
 
 #### [CreateKycStepRequest](#CreateKycStepRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String |  no  |  |
 | index | String |  no  |  |
 | active | Boolean |  no  |  |
 | rules | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [RemoveKycStepRequest](#RemoveKycStepRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | name | String? |  yes  |  |
 | index | String |  no  |  |
 | active | Boolean? |  yes  |  |
 | rules | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [KycUpdateMessage](#KycUpdateMessage)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | message | String? |  yes  |  |

---


 
 
 #### [MobileFromLinkingRequest](#MobileFromLinkingRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [MobileFromLinkingResponse](#MobileFromLinkingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | countryCode | String |  no  |  |
 | mobile | String |  no  |  |

---


 
 
 #### [SessionFromLinkingRequest](#SessionFromLinkingRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [SessionFromLinkingResponse](#SessionFromLinkingResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | session | String |  no  |  |
 | expiry | Integer |  no  |  |

---


 
 
 #### [LinkAccount](#LinkAccount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | redirectUrl | String |  no  |  |
 | device | [Device](#Device) |  no  |  |

---


 
 
 #### [LinkAccountSuccess](#LinkAccountSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | redirectUrl | String? |  yes  |  |
 | statusCode | Double? |  yes  |  |
 | status | String? |  yes  |  |
 | message | String? |  yes  |  |
 | errorCode | String? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [UnlinkAccount](#UnlinkAccount)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | device | [Device](#Device) |  no  |  |

---


 
 
 #### [UnlinkAccountSuccess](#UnlinkAccountSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String |  no  |  |
 | message | String |  no  |  |
 | statusCode | Double |  no  |  |
 | userStatus | String? |  yes  |  |
 | errorCode | String? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [Refund](#Refund)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | fingerprint | String? |  yes  |  |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | refundItems | ArrayList<[Items](#Items)>? |  yes  |  |
 | orderId | String |  no  |  |
 | refundId | String |  no  |  |
 | refundAmount | Double |  no  |  |

---


 
 
 #### [Translation](#Translation)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | content | Object? |  yes  |  |

---


 
 
 #### [FilterKeys](#FilterKeys)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | name | String? |  yes  |  |
 | kind | String? |  yes  |  |

---


 
 
 #### [FilterValues](#FilterValues)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | display | String? |  yes  |  |
 | isSelected | Boolean? |  yes  |  |
 | value | String? |  yes  |  |

---


 
 
 #### [Filters](#Filters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | key | [FilterKeys](#FilterKeys)? |  yes  |  |
 | values | ArrayList<[FilterValues](#FilterValues)>? |  yes  |  |

---


 
 
 #### [PageResponse](#PageResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | current | Integer |  no  |  |
 | hasPrevious | Boolean |  no  |  |
 | hasNext | Boolean |  no  |  |
 | size | Integer |  no  |  |
 | itemTotal | Integer |  no  |  |

---


 
 
 #### [UserResponse](#UserResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[Filters](#Filters)> |  no  |  |
 | page | [PageResponse](#PageResponse) |  no  |  |
 | listOfUsers | ArrayList<[UserSchema](#UserSchema)> |  no  |  |

---


 
 
 #### [UserDetailRequest](#UserDetailRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  |  |

---


 
 
 #### [UserConsents](#UserConsents)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | ipAddress | String? |  yes  |  |
 | text | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |

---


 
 
 #### [CreditScoreSchema](#CreditScoreSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | cibil | Double? |  yes  |  |
 | finbox | String? |  yes  |  |
 | systemAwarded | String? |  yes  |  |
 | isActive | Boolean? |  yes  |  |
 | deletedAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | createdAt | String? |  yes  |  |

---


 
 
 #### [CreditLimitSchema](#CreditLimitSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | creditLimit | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | updatedAt | String? |  yes  |  |
 | deletedAt | String? |  yes  |  |

---


 
 
 #### [Screen](#Screen)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | screenType | String? |  yes  |  |
 | name | String? |  yes  |  |
 | link | String? |  yes  |  |

---


 
 
 #### [UserStateSchema](#UserStateSchema)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | screen | [Screen](#Screen)? |  yes  |  |

---


 
 
 #### [GetAccessTokenResponse](#GetAccessTokenResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | accessToken | String? |  yes  |  |
 | refreshToken | String? |  yes  |  |
 | tokenExpireAt | String? |  yes  |  |
 | tokenExpiryIn | String? |  yes  |  |
 | refreshTokenExpiryAt | String? |  yes  |  |
 | refreshTokenExpiryIn | String? |  yes  |  |
 | scope | ArrayList<String>? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [RefreshTokenResponse](#RefreshTokenResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | success | Boolean? |  yes  |  |
 | accessToken | String? |  yes  |  |
 | tokenExpireAt | String? |  yes  |  |
 | tokenExpiryIn | String? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [RefreshTokenRequest](#RefreshTokenRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | token | String |  no  |  |

---


 
 
 #### [Items](#Items)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | String? |  yes  |  |
 | sku | String? |  yes  |  |
 | rate | Double? |  yes  |  |
 | quantity | Double? |  yes  |  |

---


 
 
 #### [RefundStatusList](#RefundStatusList)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | orderItems | ArrayList<[Items](#Items)>? |  yes  |  |
 | amount | Double? |  yes  |  |
 | status | String? |  yes  |  |
 | createdAt | String? |  yes  |  |
 | processedDate | String? |  yes  |  |

---


 
 
 #### [RefundStatus](#RefundStatus)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | orderId | String? |  yes  |  |
 | userId | String? |  yes  |  |
 | merchantId | String? |  yes  |  |
 | lenderId | String? |  yes  |  |
 | loanAccountNumber | String? |  yes  |  |
 | refund | ArrayList<[RefundStatusList](#RefundStatusList)>? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [GetSchemesSuccess](#GetSchemesSuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String? |  yes  |  |
 | lenders | ArrayList<[SchemeResponse](#SchemeResponse)> |  no  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [CustomerMetricsPivots](#CustomerMetricsPivots)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | date | String? |  yes  |  |
 | sum | Double? |  yes  |  |

---


 
 
 #### [CustomerMetricsSubResponse](#CustomerMetricsSubResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | total | String? |  yes  |  |
 | pivots | ArrayList<[CustomerMetricsPivots](#CustomerMetricsPivots)>? |  yes  |  |
 | title | String? |  yes  |  |
 | description | String? |  yes  |  |
 | valueFormat | String? |  yes  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [CustomerMetricsAnalytics](#CustomerMetricsAnalytics)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | totalCustomers | [CustomerMetricsSubResponse](#CustomerMetricsSubResponse)? |  yes  |  |
 | source | [CustomerMetricsSubResponse](#CustomerMetricsSubResponse)? |  yes  |  |

---


 
 
 #### [CustomerMetricsFilters](#CustomerMetricsFilters)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | type | String |  no  |  |
 | display | String |  no  |  |
 | value | ArrayList<String> |  no  |  |
 | isSelected | Boolean? |  yes  |  |
 | isActive | Boolean |  no  |  |

---


 
 
 #### [CustomerMetrics](#CustomerMetrics)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | metrics | [CustomerMetricsAnalytics](#CustomerMetricsAnalytics)? |  yes  |  |
 | filters | ArrayList<[CustomerMetricsFilters](#CustomerMetricsFilters)>? |  yes  |  |
 | sort | ArrayList<[CustomerMetricsFilters](#CustomerMetricsFilters)>? |  yes  |  |

---


 
 
 #### [SchemeResponse](#SchemeResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String |  no  | A slug identifier for the lender. |
 | isDefault | Boolean |  no  | Indicates if this is the default lender |
 | logoUrl | String |  no  | URL to the logo of the lender |
 | name | String |  no  | Name of the lender |
 | title | String |  no  | Title of the lender |
 | subtitle | String |  no  | Subtitle or additional information about the lender |
 | amount | Double? |  yes  | Transaction amount |
 | paymentOptions | [SchemePaymentOptionsResponse](#SchemePaymentOptionsResponse) |  no  |  |

---


 
 
 #### [SchemePaymentOptionsResponse](#SchemePaymentOptionsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | emis | ArrayList<[SchemeEmiPaymentOptionResponse](#SchemeEmiPaymentOptionResponse)>? |  yes  |  |
 | payLater | [SchemePayLaterPaymentOptionResponse](#SchemePayLaterPaymentOptionResponse)? |  yes  |  |

---


 
 
 #### [SchemeEmiPaymentOptionResponse](#SchemeEmiPaymentOptionResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  | Unique identifier for the payment option. |
 | isDefault | Boolean |  no  | Indicates if this is the default payment option. |
 | description | String |  no  | Description of the payment option. |
 | title | String |  no  | Title of the payment option. |
 | subtitle | String |  no  | Subtitle or additional information about the payment option. |
 | amount | Double |  no  | Total amount for this EMI. |
 | interest | Double? |  yes  | Interest rate applicable to the EMIn. |
 | processingFee | Double |  no  | Processing fee associated with the EMI. |
 | tenure | Double |  no  | Tenure of the EMI in months. |
 | emiSchedule | ArrayList<[SchemeEmiScheduleResponse](#SchemeEmiScheduleResponse)> |  no  | Schedule of EMIs. |

---


 
 
 #### [SchemeEmiScheduleResponse](#SchemeEmiScheduleResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | installmentNo | Integer |  no  | The installment number. |
 | installmentAmount | Double |  no  | The total amount due for this installment. |
 | dueDate | String |  no  | The date by which the installment is due, in ISO 8601 format. |

---


 
 
 #### [SchemePayLaterPaymentOptionResponse](#SchemePayLaterPaymentOptionResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String |  no  | Unique identifier for the PayLater option |
 | title | String |  no  | Title of the PayLater option |
 | subtitle | String |  no  | Subtitle or additional descriptor for the PayLater option |
 | description | String |  no  | Detailed description of the PayLater option |
 | tenure | Integer |  no  | The tenure of the PayLater option, in months |
 | interest | Integer |  no  | Interest amount for the PayLater option |
 | processingFee | Integer |  no  | Processing fee for the PayLater option |
 | amount | Integer |  no  | The amount to be paid in Rupees |
 | isDefault | Boolean |  no  | Indicates if this is the default payment option |

---


 
 
 #### [LimitResponse](#LimitResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | available | ArrayList<[AvailableOrPossibleLender](#AvailableOrPossibleLender)>? |  yes  |  |
 | possible | ArrayList<[AvailableOrPossibleLender](#AvailableOrPossibleLender)>? |  yes  |  |

---


 
 
 #### [AvailableOrPossibleLender](#AvailableOrPossibleLender)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | limit | Double |  no  | The available credit limit from the lender. |
 | lenderName | String |  no  | The name of the lender. |
 | slug | String |  no  | A slug identifier for the lender. |
 | isDefault | Boolean |  no  | Indicates if this is the default lender option. |
 | logo | String |  no  | URL to the lender's logo. |

---


 
 
 #### [GetSchemesRequest](#GetSchemesRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | order | [Order](#Order) |  no  |  |
 | device | [Device](#Device) |  no  |  |
 | meta | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [CustomerMetricsResponse](#CustomerMetricsResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | data | [CustomerMetrics](#CustomerMetrics)? |  yes  |  |

---


 
 
 #### [CustomerMetricsRequest](#CustomerMetricsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[CustomerMetricsFilters](#CustomerMetricsFilters)>? |  yes  |  |
 | sort | ArrayList<[CustomerMetricsFilters](#CustomerMetricsFilters)>? |  yes  |  |
 | merchantId | String? |  yes  |  |
 | lenderId | String? |  yes  |  |
 | pivotPoints | Double? |  yes  |  |

---


 
 
 #### [SourceAnalyticsRequest](#SourceAnalyticsRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | filters | ArrayList<[CustomerMetricsFilters](#CustomerMetricsFilters)>? |  yes  |  |

---


 
 
 #### [LenderResponse](#LenderResponse)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | slug | String? |  yes  |  |
 | name | String? |  yes  |  |
 | logo | String? |  yes  |  |

---


 
 
 #### [CreditLimitObject](#CreditLimitObject)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | availableLimit | Double? |  yes  |  |
 | possibleLimit | Double? |  yes  |  |
 | lender | [LenderResponse](#LenderResponse)? |  yes  |  |

---


 
 
 #### [BusinessDetails](#BusinessDetails)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | category | String |  no  |  |
 | shopName | String? |  yes  |  |
 | legalName | String |  no  |  |
 | address | String? |  yes  |  |
 | type | String? |  yes  |  |
 | pincode | String? |  yes  |  |

---


 
 
 #### [DocumentItems](#DocumentItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | number | String |  no  |  |
 | category | String? |  yes  |  |
 | type | String |  no  |  |
 | name | String? |  yes  |  |
 | issuedOn | String? |  yes  |  |
 | issuedAt | String? |  yes  |  |
 | issuedBy | String? |  yes  |  |
 | expiryOn | String? |  yes  |  |

---


 
 
 #### [VintageItems](#VintageItems)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | month | Integer |  no  |  |
 | year | Integer |  no  |  |
 | totalTransactions | Integer |  no  |  |
 | totalTransactionAmount | Double |  no  |  |
 | totalCancellations | Integer? |  yes  |  |
 | totalCancellationAmount | Double? |  yes  |  |

---


 
 
 #### [EligibilitySuccess](#EligibilitySuccess)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | status | String? |  yes  |  |
 | message | String? |  yes  |  |
 | redirectUrl | String? |  yes  |  |
 | creditLimits | ArrayList<[CreditLimitObject](#CreditLimitObject)>? |  yes  |  |
 | headers | HashMap<String,Object>? |  yes  |  |

---


 
 
 #### [CheckEligibilityRequest](#CheckEligibilityRequest)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | customer | [CustomerObject](#CustomerObject) |  no  |  |
 | order | [Order](#Order)? |  yes  |  |
 | businessDetails | [BusinessDetails](#BusinessDetails)? |  yes  |  |
 | documents | ArrayList<[DocumentItems](#DocumentItems)>? |  yes  |  |
 | device | [Device](#Device) |  no  |  |
 | vintage | ArrayList<[VintageItems](#VintageItems)>? |  yes  |  |
 | meta | HashMap<String,Object>? |  yes  |  |
 | fetchLimitOptions | Boolean? |  yes  |  |

---


 
 
 #### [EmiSchedule](#EmiSchedule)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | installmentNo | Integer? |  yes  |  |
 | installmentAmount | Integer? |  yes  |  |
 | dueDate | String? |  yes  |  |

---


 
 
 #### [PaymentOption](#PaymentOption)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | title | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | description | String? |  yes  |  |
 | tenure | Integer? |  yes  |  |
 | processingFee | Integer? |  yes  |  |
 | amount | Integer? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | emiSchedule | ArrayList<[EmiSchedule](#EmiSchedule)>? |  yes  |  |

---


 
 
 #### [PaymentOptions](#PaymentOptions)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | payLater | [PaymentOption](#PaymentOption)? |  yes  |  |
 | emis | ArrayList<[PaymentOption](#PaymentOption)>? |  yes  |  |

---


 
 
 #### [LenderAndPaymentOption](#LenderAndPaymentOption)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | id | String? |  yes  |  |
 | name | String |  no  |  |
 | title | String? |  yes  |  |
 | subtitle | String? |  yes  |  |
 | isDefault | Boolean? |  yes  |  |
 | logoUrl | String |  no  |  |
 | amount | Integer? |  yes  |  |
 | paymentOptions | [PaymentOptions](#PaymentOptions)? |  yes  |  |

---


 
 
 #### [GetSchemesSuccessOld](#GetSchemesSuccessOld)

 | Properties | Type | Nullable | Description |
 | ---------- | ---- | -------- | ----------- |
 | userId | String |  no  |  |
 | lenders | ArrayList<[LenderAndPaymentOption](#LenderAndPaymentOption)>? |  yes  |  |

---




### Enums





 #### [PageType](#PageType)
 Type : string

 | Name | Value | Description |
 | ---- | ----- | ----------- |
 | external | external | Symbolic link for External Link: /external/:url |
 | login | login | Symbolic link for Login: /login |
 | home | home | Symbolic link for Home: / |
 | transactions | transactions | Symbolic link for Transactions: /transactions |
 | transactionDetails | transactionDetails | Symbolic link for Transaction Details: /transactions/:id |
 | rewards | rewards | Symbolic link for Rewards: /rewards |
 | referAndEarn | referAndEarn | Symbolic link for Refer: /refer |
 | profile | profile | Symbolic link for Profile: /profile |
 | setupAutopay | setupAutopay | Symbolic link for AutoPay: /autopay |
 | updateEmail | updateEmail | Symbolic link for Update Email: /profile/email |
 | reportIssue | reportIssue | Symbolic link for Report Issue: /profile/report |
 | creditScore | creditScore | Symbolic link for Credit Score: /credit-score |
 | autoPay | autoPay | Symbolic link for Setup Autopay: /autopay |
 | helpCenter | helpCenter | Symbolic link for Help Center: /profile/help-center |
 | kycInit | kycInit | Symbolic link for Start KYC: /kyc |
 | accessDigilocker | accessDigilocker | Symbolic link for Access Digilocker: /kyc/:lender/access-digilocker |
 | liveliness | liveliness | Symbolic link for Liveliness: /kyc/:lender/selfie |
 | lenderOnboard | lenderOnboard | Symbolic link for Lender Onboard: /kyc/:lender/lender-onboard |
 | lender | lender | Symbolic link for Lender: /lender/:lenderName |
 | kycDocs | kycDocs | Symbolic link for Verify KYC Documents: /kyc/documents |
 | kycSelfie | kycSelfie | Symbolic link for Verify KYC Selfie: /kyc/selfie |
 | kycStatus | kycStatus | Symbolic link for KYC Status: /kyc/status |
 | kycError | kycError | Symbolic link for KYC Error: /kyc/error |
 | kycDigilockerResponse | kycDigilockerResponse | Symbolic link for KYC Digilocker Response: /kyc/digilocker-response |
 | kycInitResponse | kycInitResponse | Symbolic link for KYC Init Response: /kyc/init-response |
 | repayment | repayment | Symbolic link for Repayment: /repayment |
 | netBankingRepayment | netBankingRepayment | Symbolic link for Net Banking Repayment: /repayment/netbanking |
 | upiRepayment | upiRepayment | Symbolic link for UPI Repayment: /repayment/upi |
 | sanctionLetter | sanctionLetter | Symbolic link for Sanction Letter: /sanction/:userId |
 | kfs | kfs | Symbolic link for KFS: /kfs/:userId |

---





