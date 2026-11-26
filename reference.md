# Reference
## Customer
<details><summary><code>client.customer.<a href="/src/api/resources/customer/client/Client.ts">search</a>({ ...params }) -> FiveOneEat.SearchCustomerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns grouped results for each type. Use per_type to control how many results
appear per section. Optionally filter by category, city, or geo radius.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.search({
    q: "q"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.SearchCustomerRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomerClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PublicLists
<details><summary><code>client.publicLists.<a href="/src/api/resources/publicLists/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetPublicListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read a publicly shared list. No authentication required — this is what a
share link resolves to.

A private list returns 404 rather than 403: a 403 would confirm the list
exists, which is more than a stranger should learn from a guessed URL.
Items exclude delisted businesses, so a business that has left the
platform cannot leak through someone's shared link.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicLists.get({
    businessList: "businessList"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.GetPublicListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Auth
<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">register</a>({ ...params }) -> FiveOneEat.RegisterAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new business user account and return an API token for immediate authentication.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.register({
    name: "name",
    email: "email",
    password: "password",
    device_name: "device_name",
    password_confirmation: "password_confirmation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.RegisterBusinessRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">login</a>({ ...params }) -> FiveOneEat.LoginAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Exchange business user credentials for an API token. Returns a 422 if the account is not a business account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.login({
    email: "email",
    password: "password",
    device_name: "device_name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.LoginBusinessRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">forgotPassword</a>({ ...params }) -> FiveOneEat.ForgotPasswordAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sends a password reset link to the provided email address if an account exists.
Always returns a 200 response to prevent email enumeration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.forgotPassword({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ForgotPasswordRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">resetPassword</a>({ ...params }) -> FiveOneEat.ResetPasswordAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Validates the reset token and updates the user's password. All existing API tokens
are revoked after a successful reset, requiring re-authentication on all devices.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.resetPassword({
    token: "token",
    email: "email",
    password: "password",
    password_confirmation: "password_confirmation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ResetPasswordRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">me</a>() -> FiveOneEat.MeAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the current authenticated business user with their active business and all owned businesses.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.me();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">logout</a>() -> FiveOneEat.LogoutAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke the current API token and log out the business user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.logout();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">logoutAll</a>() -> FiveOneEat.LogoutAllAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke all API tokens for the authenticated business user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.logoutAll();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.<a href="/src/api/resources/business/resources/auth/client/Client.ts">switchBusiness</a>({ ...params }) -> FiveOneEat.SwitchBusinessAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Set a different business as the active business for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.switchBusiness({
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.SwitchBusinessAuthRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Bulletins
<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">list</a>() -> FiveOneEat.ListBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.create({
    title: "title",
    content: "content",
    type: "post"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreBulletinRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.get({
    bulletin: "bulletin"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.update({
    bulletin: "bulletin",
    title: "title",
    content: "content",
    type: "post"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateBulletinRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.delete({
    bulletin: "bulletin"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">togglePinned</a>({ ...params }) -> FiveOneEat.TogglePinnedBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.togglePinned({
    bulletin: "bulletin"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.TogglePinnedBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.<a href="/src/api/resources/business/resources/bulletins/client/Client.ts">togglePublished</a>({ ...params }) -> FiveOneEat.TogglePublishedBulletinsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.togglePublished({
    bulletin: "bulletin"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.TogglePublishedBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Businesses
<details><summary><code>client.business.businesses.<a href="/src/api/resources/business/resources/businesses/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of all businesses owned by the authenticated user.
Useful for rendering a business picker in the companion mobile app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.businesses.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ListBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.businesses.<a href="/src/api/resources/business/resources/businesses/client/Client.ts">create</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new business owned by the authenticated user. The newly created
business is automatically set as the user's active business.

When the business matches unclaimed listings already on 51Eat (same
phone, website domain, or name within 2 km), nothing is created and the
response is 409 with those listings in `existing_listings`: offer to
claim one (`POST /claim-requests`), or send `create_anyway: true` to
create it regardless.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.businesses.create({
    name: "name",
    handle: "handle",
    category_ids: [1]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreBusinessRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.businesses.<a href="/src/api/resources/business/resources/businesses/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single business owned by the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.businesses.get({
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.businesses.<a href="/src/api/resources/business/resources/businesses/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update core fields for a business owned by the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.businesses.update({
    business: "business",
    name: "name",
    handle: "handle",
    category_ids: [1]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateBusinessRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.businesses.<a href="/src/api/resources/business/resources/businesses/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a business owned by the authenticated user. A business with
market history (dues or market-day attendance), or one that has taken
payments, can't be deleted (422).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.businesses.delete({
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Claims
<details><summary><code>client.business.claims.<a href="/src/api/resources/business/resources/claims/client/Client.ts">listClaimableBusinesses</a>({ ...params }) -> FiveOneEat.ListClaimableBusinessesClaimsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.claims.listClaimableBusinesses();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ListClaimableBusinessesClaimsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.claims.<a href="/src/api/resources/business/resources/claims/client/Client.ts">listClaimRequests</a>() -> FiveOneEat.ListClaimRequestsClaimsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.claims.listClaimRequests();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.claims.<a href="/src/api/resources/business/resources/claims/client/Client.ts">requestClaim</a>({ ...params }) -> FiveOneEat.RequestClaimClaimsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.claims.requestClaim({
    business_id: "business_id",
    message: "message"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreClaimRequestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.claims.<a href="/src/api/resources/business/resources/claims/client/Client.ts">claimViaToken</a>({ ...params }) -> FiveOneEat.ClaimViaTokenClaimsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.claims.claimViaToken({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ClaimViaTokenClaimsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business ProductOrders
<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListProductOrdersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ListProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetProductOrdersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.get({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">fulfill</a>({ ...params }) -> FiveOneEat.FulfillProductOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The business's part is done, and the customer is told. A shipped order
becomes `fulfilled` (on its way); a pickup order becomes
`ready_for_pickup`, and `mark-picked-up` completes it once collected.
A farm-stand order is fulfilled at checkout and is refused here.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.fulfill({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.FulfillProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">markPickedUp</a>({ ...params }) -> FiveOneEat.MarkPickedUpProductOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only a pickup order, `unfulfilled` or `ready_for_pickup`; it becomes `fulfilled`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.markPickedUp({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.MarkPickedUpProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">addTracking</a>({ ...params }) -> FiveOneEat.AddTrackingProductOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

For a label bought elsewhere: records it as a shipment, marks the order
sent and sends the tracking to the customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.addTracking({
    order: "order",
    carrier: "carrier",
    tracking_number: "tracking_number"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreTrackingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">refund</a>({ ...params }) -> FiveOneEat.RefundProductOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refunds `amount` (dollars) of the order, or everything still refundable
when `amount` is omitted, through Stripe. Sales tax on the refunded part
is reversed automatically.

Send an `Idempotency-Key` header (1–255 characters, unique per refund you
mean to make) to make retries safe: a repeat with the same key returns
the order with the refund already made, with 200, instead of refunding
again — even when nothing is left to refund. Without it, a retry after a
lost response may refund twice.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.refund({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.RefundOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">getLabelRates</a>({ ...params }) -> FiveOneEat.GetLabelRatesProductOrdersResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A 422 has the body `{"error": "..."}`, not the usual validation shape:
"Shipping account not configured." when the business has no active
shipping account, or "Order has no shipping address."
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.getLabelRates({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetLabelRatesProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productOrders.<a href="/src/api/resources/business/resources/productOrders/client/Client.ts">purchaseLabel</a>({ ...params }) -> FiveOneEat.PurchaseLabelProductOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Buys a label at the chosen rate, records it as a shipment, marks the
order sent and sends the tracking to the customer. Nothing is bought
when the order is refused.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productOrders.purchaseLabel({
    order: "order",
    provider_rate_id: "provider_rate_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.PurchaseLabelRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Events
<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">list</a>() -> FiveOneEat.ListEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepts an optional `filter` query param: `upcoming`, `past`, or `all` (default `all`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.create({
    title: "title",
    starts_at: "2024-01-15T09:30:00Z",
    ends_at: "2024-01-15T09:30:00Z"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreEventRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.get({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.update({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateEventRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

An event with ticket sales can't be deleted (422); unpublish it instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.delete({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">togglePublished</a>({ ...params }) -> FiveOneEat.TogglePublishedEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.togglePublished({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.TogglePublishedEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">uploadImage</a>({ ...params }) -> FiveOneEat.UploadImageEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Upload and replace the image for the given event. Any existing image will be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.uploadImage({
    image: fs.createReadStream("/path/to/your/file"),
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UploadEventImageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">deleteImage</a>({ ...params }) -> FiveOneEat.DeleteImageEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.deleteImage({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteImageEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">listRsvps</a>({ ...params }) -> FiveOneEat.ListRsvpsEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepts an optional `status` query param: `attending`, `not_attending`, or `maybe`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.listRsvps({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ListRsvpsEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">listAttendees</a>({ ...params }) -> FiveOneEat.ListAttendeesEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepts an optional `status` query param matching the ticket status
(`valid`, `used`, `cancelled`, `refunded`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.listAttendees({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ListAttendeesEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.<a href="/src/api/resources/business/resources/events/client/Client.ts">salesSummary</a>({ ...params }) -> FiveOneEat.SalesSummaryEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns aggregated sales totals: gross revenue, refunds, tickets sold,
and a per-ticket-type breakdown. Gross revenue counts every paid order,
including those refunded since; refunds are subtracted once for net.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.salesSummary({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.SalesSummaryEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Gallery
<details><summary><code>client.business.gallery.<a href="/src/api/resources/business/resources/gallery/client/Client.ts">list</a>() -> FiveOneEat.ListGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.gallery.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `GalleryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.gallery.<a href="/src/api/resources/business/resources/gallery/client/Client.ts">upload</a>({ ...params }) -> FiveOneEat.UploadGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.gallery.upload({
    photo: fs.createReadStream("/path/to/your/file")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreGalleryPhotoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GalleryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.gallery.<a href="/src/api/resources/business/resources/gallery/client/Client.ts">reorder</a>({ ...params }) -> FiveOneEat.ReorderGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.gallery.reorder({
    photos: [{
            id: "id",
            sort_order: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ReorderGalleryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GalleryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.gallery.<a href="/src/api/resources/business/resources/gallery/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.gallery.update({
    photo: "photo"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateGalleryPhotoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GalleryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.gallery.<a href="/src/api/resources/business/resources/gallery/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.gallery.delete({
    photo: "photo"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteGalleryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GalleryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Hours
<details><summary><code>client.business.hours.<a href="/src/api/resources/business/resources/hours/client/Client.ts">get</a>() -> FiveOneEat.GetHoursResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.hours.get();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `HoursClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.hours.<a href="/src/api/resources/business/resources/hours/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateHoursResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.hours.update({
    slots: [{
            day_of_week: 1,
            opens_at: "opens_at",
            closes_at: "closes_at"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateBusinessHoursRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HoursClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Menus
<details><summary><code>client.business.menus.<a href="/src/api/resources/business/resources/menus/client/Client.ts">list</a>() -> FiveOneEat.ListMenusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all menus with their full group/item hierarchy for the authenticated user's active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MenusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.<a href="/src/api/resources/business/resources/menus/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateMenusResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.create({
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreMenuRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MenusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.<a href="/src/api/resources/business/resources/menus/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetMenusResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.get({
    menu: "menu"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetMenusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MenusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.<a href="/src/api/resources/business/resources/menus/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateMenusResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.update({
    menu: "menu",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateMenuRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MenusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.<a href="/src/api/resources/business/resources/menus/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteMenusResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.delete({
    menu: "menu"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteMenusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MenusClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Messaging
<details><summary><code>client.business.messaging.<a href="/src/api/resources/business/resources/messaging/client/Client.ts">channelAuth</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint is used by the business companion mobile app to authenticate with
Pusher channels. It validates that the authenticated business user has
permission to access the requested channel, scoped to their active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.channelAuth({
    channel_name: "channel_name",
    socket_id: "socket_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.ChannelAuthMessagingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Profile
<details><summary><code>client.business.profile.<a href="/src/api/resources/business/resources/profile/client/Client.ts">get</a>() -> FiveOneEat.GetProfileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the full editable profile for the authenticated user's active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.get();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.profile.<a href="/src/api/resources/business/resources/profile/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateProfileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update core profile fields for the authenticated user's active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.update();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateBusinessProfileRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.profile.<a href="/src/api/resources/business/resources/profile/client/Client.ts">syncCuisines</a>({ ...params }) -> FiveOneEat.SyncCuisinesProfileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replace the set of cuisines associated with the authenticated user's active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.syncCuisines({
    cuisine_ids: [1]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.SyncCuisinesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.profile.<a href="/src/api/resources/business/resources/profile/client/Client.ts">syncCertifications</a>({ ...params }) -> FiveOneEat.SyncCertificationsProfileResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replace the set of certifications associated with the authenticated user's active business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.syncCertifications({
    certification_ids: [1]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.SyncCertificationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProfileClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business PushNotifications
<details><summary><code>client.business.pushNotifications.<a href="/src/api/resources/business/resources/pushNotifications/client/Client.ts">register</a>({ ...params }) -> FiveOneEat.RegisterPushNotificationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register (or update) the authenticated business user's Expo push token for a
device. If a `device_id` is provided, an existing registration for that device
is updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.pushNotifications.register({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StorePushTokenRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PushNotificationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.pushNotifications.<a href="/src/api/resources/business/resources/pushNotifications/client/Client.ts">unregister</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete the authenticated business user's Expo push token registration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.pushNotifications.unregister({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UnregisterPushNotificationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PushNotificationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Stands
<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">list</a>() -> FiveOneEat.ListStandsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateStandsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.create({
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreStandRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetStandsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.get({
    stand: "stand"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetStandsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateStandsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.update({
    stand: "stand"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateStandRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.delete({
    stand: "stand"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteStandsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stands.<a href="/src/api/resources/business/resources/stands/client/Client.ts">syncProducts</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replaces the stand's product list with the submitted set. Send an empty
array to clear all assignments. Only products belonging to the
authenticated business are accepted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stands.syncProducts({
    stand: "stand",
    product_ids: ["product_ids"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.SyncStandProductsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business StripeConnect
<details><summary><code>client.business.stripeConnect.<a href="/src/api/resources/business/resources/stripeConnect/client/Client.ts">status</a>() -> FiveOneEat.StatusStripeConnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Connect with `POST /api/v1/business/stripe-connect` instead.
This endpoint returns the active business's Stripe Connect connection,
still creating a new Express account on Stripe if it has none, along with
the publishable key and the flags the mobile client uses to decide whether
to present onboarding or the management UI. Opening an account on a GET
leaves a new Express account behind every time a disconnected business
opens the screen, so once the app connects with POST this endpoint will
only read the existing connection.

A 409 with a message means a parallel connect raced this one and
its connection was disconnected meanwhile: ask the owner to try again.

A 403 with a message means 51Eat hasn't approved the business to sell
yet; nothing is opened on Stripe until it has.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stripeConnect.status();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StripeConnectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stripeConnect.<a href="/src/api/resources/business/resources/stripeConnect/client/Client.ts">connect</a>() -> FiveOneEat.ConnectStripeConnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Opens a new Express account on Stripe for the active business when it
has no live connection (none yet, or it was disconnected), and returns
the connection in the same shape as the status endpoint. A business that
is already connected gets its existing connection back, with its status
refreshed from Stripe. Call this when the owner chooses to connect, then
request an account session for onboarding.

A 409 with a message means a parallel connect raced this one and
its connection was disconnected meanwhile: ask the owner to try again.

A 403 with a message means 51Eat hasn't approved the business to sell
yet; nothing is opened on Stripe until it has.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stripeConnect.connect();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StripeConnectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stripeConnect.<a href="/src/api/resources/business/resources/stripeConnect/client/Client.ts">disconnect</a>() -> FiveOneEat.DisconnectStripeConnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deauthorizes the business's StripeConnection; the row stays as history.
The Stripe account itself is not deleted. Connecting again opens a new
account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stripeConnect.disconnect();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StripeConnectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stripeConnect.<a href="/src/api/resources/business/resources/stripeConnect/client/Client.ts">createAccountSession</a>({ ...params }) -> FiveOneEat.CreateAccountSessionStripeConnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The request body specifies which embedded components to enable on the
session. Use `account_onboarding` during onboarding and any of the
management components (payments, payouts, balances, documents,
account_management, notification_banner, tax_settings, tax_registrations)
after the connected account has submitted their details.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stripeConnect.createAccountSession({
    components: [{
            enabled: true,
            features: ["features"]
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.CreateAccountSessionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StripeConnectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.stripeConnect.<a href="/src/api/resources/business/resources/stripeConnect/client/Client.ts">refresh</a>() -> FiveOneEat.RefreshStripeConnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Pulls the latest account data from Stripe and updates the local
`stripe_connections` record. Provided as a belt-and-suspenders option
alongside the `account.updated` webhook so mobile clients can guarantee
freshness immediately after returning from an onboarding flow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.stripeConnect.refresh();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StripeConnectClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Cuisines
<details><summary><code>client.business.cuisines.<a href="/src/api/resources/business/resources/cuisines/client/Client.ts">list</a>() -> FiveOneEat.ListCuisinesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all cuisines, ordered alphabetically. Use these IDs to
populate the `cuisine_ids` field when updating a business profile.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.cuisines.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CuisinesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Certifications
<details><summary><code>client.business.certifications.<a href="/src/api/resources/business/resources/certifications/client/Client.ts">list</a>() -> FiveOneEat.ListCertificationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all certifications, ordered alphabetically. Use these IDs
to populate the `certification_ids` field when updating a business profile.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.certifications.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CertificationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Categories
<details><summary><code>client.business.categories.<a href="/src/api/resources/business/resources/categories/client/Client.ts">list</a>() -> FiveOneEat.ListCategoriesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all business categories, ordered by sort order and name.
Use these IDs to populate the `category_ids` field when creating or updating a business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.categories.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CategoriesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Allergens
<details><summary><code>client.business.allergens.<a href="/src/api/resources/business/resources/allergens/client/Client.ts">list</a>() -> FiveOneEat.ListAllergensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all allergens, ordered alphabetically. Use these UUIDs
in the `allergens` array when creating or updating a menu item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.allergens.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AllergensClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business TemporaryLocations
<details><summary><code>client.business.temporaryLocations.<a href="/src/api/resources/business/resources/temporaryLocations/client/Client.ts">list</a>() -> FiveOneEat.ListTemporaryLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.temporaryLocations.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TemporaryLocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.temporaryLocations.<a href="/src/api/resources/business/resources/temporaryLocations/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateTemporaryLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.temporaryLocations.create({
    title: "title",
    starts_at: "2024-01-15T09:30:00Z",
    ends_at: "2024-01-15T09:30:00Z"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.StoreTemporaryLocationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TemporaryLocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.temporaryLocations.<a href="/src/api/resources/business/resources/temporaryLocations/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetTemporaryLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.temporaryLocations.get({
    temporaryLocation: "temporaryLocation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.GetTemporaryLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TemporaryLocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.temporaryLocations.<a href="/src/api/resources/business/resources/temporaryLocations/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateTemporaryLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.temporaryLocations.update({
    temporaryLocation: "temporaryLocation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateTemporaryLocationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TemporaryLocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.temporaryLocations.<a href="/src/api/resources/business/resources/temporaryLocations/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteTemporaryLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.temporaryLocations.delete({
    temporaryLocation: "temporaryLocation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteTemporaryLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TemporaryLocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business ProductCategories
<details><summary><code>client.business.productCategories.<a href="/src/api/resources/business/resources/productCategories/client/Client.ts">list</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productCategories.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ProductCategoriesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productCategories.<a href="/src/api/resources/business/resources/productCategories/client/Client.ts">create</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productCategories.create();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ProductCategoriesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productCategories.<a href="/src/api/resources/business/resources/productCategories/client/Client.ts">update</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productCategories.update({
    productCategory: "productCategory"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.UpdateProductCategoriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductCategoriesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.productCategories.<a href="/src/api/resources/business/resources/productCategories/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.productCategories.delete({
    productCategory: "productCategory"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.DeleteProductCategoriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductCategoriesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Auth Tokens
<details><summary><code>client.business.auth.tokens.<a href="/src/api/resources/business/resources/auth/resources/tokens/client/Client.ts">list</a>() -> FiveOneEat.ListTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all API tokens for the authenticated business user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.tokens.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TokensClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.auth.tokens.<a href="/src/api/resources/business/resources/auth/resources/tokens/client/Client.ts">revoke</a>({ ...params }) -> FiveOneEat.RevokeTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific API token by its ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.auth.tokens.revoke({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.auth.RevokeTokensRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TokensClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Bulletins Comments
<details><summary><code>client.business.bulletins.comments.<a href="/src/api/resources/business/resources/bulletins/resources/comments/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListCommentsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.comments.list({
    bulletin: "bulletin"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.bulletins.ListCommentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.bulletins.comments.<a href="/src/api/resources/business/resources/bulletins/resources/comments/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateCommentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Omit `parent_id` for a top-level comment. Set `parent_id` to a top-level
comment's id to post a one-level reply (replies to replies are not allowed).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.bulletins.comments.create({
    bulletin: "bulletin",
    body: "body"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.bulletins.StoreBulletinCommentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Commerce Locations
<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">list</a>() -> FiveOneEat.ListLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Every store and stand of the business, main store first and then by
name, including ones switched off, blocked by the plan or archived.
Each carries why it can't sell yet (`blocker`) and its open pickup
orders still to come (`affected_orders`), the same as the web's list.
`can_add_store` says whether the plan has room for another store.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Answers 201. `kind` is `store` or `stand`. A Free plan has one store,
the main one: a second is refused with a form error on `kind`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.create({
    "Idempotency-Key": "Idempotency-Key",
    kind: "store"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.StoreLocationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.get({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.GetLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The main store saves only its name: its address, timezone and phone
are the business's.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.update({
    location: "location",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.UpdateLocationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">delete</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only one that never sold anything and holds no stock: otherwise 409,
and it is archived instead. The main store can't be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.delete({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.DeleteLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">setActive</a>({ ...params }) -> FiveOneEat.SetActiveLocationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.setActive({
    location: "location",
    active: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.SetLocationActiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">archive</a>({ ...params }) -> FiveOneEat.ArchiveLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Hides it and stops it taking orders, keeping its history and freeing
its name and, for a store, its place in the plan's limit. The main
store can't be archived.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.archive({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.ArchiveLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">flyer</a>({ ...params }) -> FiveOneEat.FlyerLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A download link that works for a few minutes. `url` is null while the
flyer is still being generated. Only a stand has a flyer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.flyer({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.FlyerLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">offerMainStoreProducts</a>({ ...params }) -> FiveOneEat.OfferMainStoreProductsLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Offers, for pickup, every product the main store offers; those already
offered are left as they are. Only an extra store takes products this
way. `added` is how many it added, so a second call adds none.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.offerMainStoreProducts({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.OfferMainStoreProductsLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">getPickup</a>({ ...params }) -> FiveOneEat.GetPickupLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Its pickup settings, weekly windows with slot capacity and date
exceptions, and whether the plan lets it take pickup orders
(`can_offer_pickup`: a stand needs Pro).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.getPickup({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.GetPickupLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">updatePickup</a>({ ...params }) -> FiveOneEat.UpdatePickupLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replaces the whole schedule. A window never runs past midnight and
two windows on a day can't overlap. Turning pickup on at a stand on a
Free plan is refused with a form error on `offers_pickup`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.updatePickup({
    location: "location",
    offers_pickup: true,
    preparation_minutes: 1,
    pickup_slot_minutes: 1,
    windows: [{
            day_of_week: 1,
            opens_at: "opens_at",
            closes_at: "closes_at"
        }],
    exceptions: ["exceptions"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.UpdatePickupScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">previewPickupAffectedOrders</a>({ ...params }) -> FiveOneEat.PreviewPickupAffectedOrdersLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send the schedule you are about to save. The answer lists the open
pickup orders it would leave outside its windows, so the owner can
contact those buyers or cancel the orders first. It changes nothing,
and so, unlike the writes, takes no `Idempotency-Key`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.previewPickupAffectedOrders({
    location: "location",
    offers_pickup: true,
    preparation_minutes: 1,
    pickup_slot_minutes: 1,
    windows: [{
            day_of_week: 1,
            opens_at: "opens_at",
            closes_at: "closes_at"
        }],
    exceptions: ["exceptions"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.PreviewPickupScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">getHours</a>({ ...params }) -> FiveOneEat.GetHoursLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Its weekly slots and exceptions, and whether it is open now. The main
store and stands answer 404: the main store's hours are the business
hours.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.getHours({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.GetHoursLocationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.locations.<a href="/src/api/resources/business/resources/commerce/resources/locations/client/Client.ts">updateHours</a>({ ...params }) -> FiveOneEat.UpdateHoursLocationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replaces the whole schedule, with the business hours' rules: a slot
may close after midnight, and two slots on a day can't overlap. Send
every slot and exception to keep; none to clear them.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.locations.updateHours({
    location: "location",
    slots: [{
            day_of_week: 1,
            opens_at: "opens_at",
            closes_at: "closes_at"
        }],
    exceptions: ["exceptions"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.UpdateOpeningHoursRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LocationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Commerce Orders
<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The business's orders, newest first, 25 to a page: `open`, `completed`,
`cancelled` and `no_show` ones. An order still waiting on its payment,
or whose payment never went through, isn't listed. Each order carries
its store, the copy made when it was placed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.ListOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

With its store, buyer, lines (ordered, handed over, cancelled, still
open and refunded), payments and event log. A 404 for an order that
isn't listed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.get({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.GetOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">markReady</a>({ ...params }) -> FiveOneEat.MarkReadyOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only an open pickup order that isn't ready yet. The buyer is told.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.markReady({
    "Idempotency-Key": "Idempotency-Key",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.MarkReadyOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">markPickedUp</a>({ ...params }) -> FiveOneEat.MarkPickedUpOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send `lines` (the quantity collected, by order line ID) for a partial
pickup, or nothing for everything still open. The order is `completed`
once nothing is left.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.markPickedUp({
    "Idempotency-Key": "Idempotency-Key",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.PickUpOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">cancel</a>({ ...params }) -> FiveOneEat.CancelOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send `lines` to cancel some, or nothing for everything still open. A
line already handed over can't be cancelled. Paid lines are refunded
in the same step, with 51Eat's fee share back, unless the buyer has
disputed the payment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.cancel({
    "Idempotency-Key": "Idempotency-Key",
    order: "order",
    reason: "business_cancelled"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.CancelOrderLinesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">markNoShow</a>({ ...params }) -> FiveOneEat.MarkNoShowOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only once the pickup slot has ended (`pickup.ends_at`). What is still
open is cancelled and its stock returned. Nothing is refunded: refund
part or all of it, or keep the payment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.markNoShow({
    "Idempotency-Key": "Idempotency-Key",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.MarkNoShowOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">keepPayment</a>({ ...params }) -> FiveOneEat.KeepPaymentOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The business keeps the money rather than refund it. It's recorded as a
`payment_kept` event; no money moves, and a refund is still possible
later. Doing it twice changes nothing.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.keepPayment({
    "Idempotency-Key": "Idempotency-Key",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.KeepPaymentOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.orders.<a href="/src/api/resources/business/resources/commerce/resources/orders/client/Client.ts">refund</a>({ ...params }) -> FiveOneEat.RefundOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A quantity of each line to refund, why, and per line a store to put the
returned units back on hand. For `oversell`, `business_cancelled`,
`unavailable` and `platform_error` the buyer gets 51Eat's fee share
back too; for `changed_mind`, `no_show` and `other` 51Eat keeps it.
Nothing can be refunded while the payment is disputed.

A retry with the same `Idempotency-Key` returns the refund already
made, with the same status, and never refunds twice.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.orders.refund({
    "Idempotency-Key": "Idempotency-Key",
    order: "order",
    lines: [{
            order_item_id: "order_item_id",
            quantity: "quantity"
        }],
    reason: "oversell"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.RefundOrderLinesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Commerce Selling
<details><summary><code>client.business.commerce.selling.<a href="/src/api/resources/business/resources/commerce/resources/selling/client/Client.ts">get</a>() -> FiveOneEat.GetSellingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Selling on or off, why it can't sell yet (`blocker`, which leaves out
the switch and the seller terms, since `seller_terms` answers those),
the seller terms it is on and whether a newer version is due, how many
stores and stands sell, and where 51Eat's approval stands.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.selling.get();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `SellingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.selling.<a href="/src/api/resources/business/resources/commerce/resources/selling/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateSellingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Switching it on doesn't let the business sell until it has accepted the
current seller terms, is approved and has payments set up: `blocker` and
`seller_terms.due` still say what is left.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.selling.update({
    enabled: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.UpdateSellingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SellingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.selling.<a href="/src/api/resources/business/resources/commerce/resources/selling/client/Client.ts">getSellerTerms</a>() -> FiveOneEat.GetSellerTermsSellingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The current version with its text as safe HTML, and whether the
business has accepted it. 404 before 51Eat publishes the first version.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.selling.getSellerTerms();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `SellingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.selling.<a href="/src/api/resources/business/resources/commerce/resources/selling/client/Client.ts">acceptSellerTerms</a>({ ...params }) -> FiveOneEat.AcceptSellerTermsSellingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send the `id` of the version the owner read as `version_id`. Only the
owner can accept, the IP address is recorded, and a version that isn't
the current one is refused with 422 on `version_id`. Accepting the
version the business is already on changes nothing.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.selling.acceptSellerTerms({
    "Idempotency-Key": "Idempotency-Key",
    version_id: "version_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.AcceptSellerTermsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SellingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.selling.<a href="/src/api/resources/business/resources/commerce/resources/selling/client/Client.ts">requestApproval</a>({ ...params }) -> FiveOneEat.RequestApprovalSellingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

`sells_prepared_food` is only a hint for the admin who decides. Asking
again changes nothing and tells nobody twice; a business 51Eat turned
down can't ask again (422 on `selling_approval`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.selling.requestApproval({
    "Idempotency-Key": "Idempotency-Key",
    sells_prepared_food: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.RequestSellingApprovalRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SellingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Commerce Stock
<details><summary><code>client.business.commerce.stock.<a href="/src/api/resources/business/resources/commerce/resources/stock/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListStockResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Each option the business counts, alphabetically by product, 100 to a
page: on hand, committed, available, and whether a recount is needed.
An option nobody has counted here reads as zero.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.stock.list({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.ListStockRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StockClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.commerce.stock.<a href="/src/api/resources/business/resources/commerce/resources/stock/client/Client.ts">adjust</a>({ ...params }) -> FiveOneEat.AdjustStockResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send `count` (what's on the shelf now; it clears the recount flag) or
`delta` (whole items added or taken away), never both, and an optional
`note`. The option must count its stock, and the location must keep
stock and not be archived.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.commerce.stock.adjust({
    "Idempotency-Key": "Idempotency-Key",
    location: "location",
    variant: "variant"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.commerce.AdjustLocationStockRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StockClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Events TicketTypes
<details><summary><code>client.business.events.ticketTypes.<a href="/src/api/resources/business/resources/events/resources/ticketTypes/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListTicketTypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.ticketTypes.list({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.ListTicketTypesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketTypesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.ticketTypes.<a href="/src/api/resources/business/resources/events/resources/ticketTypes/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateTicketTypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.ticketTypes.create({
    event: "event",
    name: "name",
    price: 1.1,
    quantity_available: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.StoreTicketTypeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketTypesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.ticketTypes.<a href="/src/api/resources/business/resources/events/resources/ticketTypes/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetTicketTypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.ticketTypes.get({
    ticketType: "ticketType"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.GetTicketTypesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketTypesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.ticketTypes.<a href="/src/api/resources/business/resources/events/resources/ticketTypes/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateTicketTypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.ticketTypes.update({
    ticketType: "ticketType"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.UpdateTicketTypeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketTypesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.ticketTypes.<a href="/src/api/resources/business/resources/events/resources/ticketTypes/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteTicketTypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.ticketTypes.delete({
    ticketType: "ticketType"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.DeleteTicketTypesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketTypesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Events Orders
<details><summary><code>client.business.events.orders.<a href="/src/api/resources/business/resources/events/resources/orders/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepts an optional `status` query param (`pending`, `paid`, `failed`, `refunded`, `partially_refunded`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.orders.list({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.ListOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.orders.<a href="/src/api/resources/business/resources/events/resources/orders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetOrdersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.orders.get({
    event: "event",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.GetOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Events CheckIn
<details><summary><code>client.business.events.checkIn.<a href="/src/api/resources/business/resources/events/resources/checkIn/client/Client.ts">lookup</a>({ ...params }) -> FiveOneEat.LookupCheckInResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Decodes the base64 QR payload and returns ticket details without performing check-in.
Accepts either a `ticket_id` or `ticket_number` inside the QR payload.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.checkIn.lookup({
    event: "event",
    qr_data: "qr_data"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.LookupTicketRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckInClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.checkIn.<a href="/src/api/resources/business/resources/events/resources/checkIn/client/Client.ts">scan</a>({ ...params }) -> FiveOneEat.ScanCheckInResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Decodes the base64 QR payload, validates the ticket's current status, marks it as used,
and broadcasts the `ticket.checked-in` event via Pusher.

Returns `409` if the ticket has already been checked in, `400` for refunded or otherwise
invalid tickets.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.checkIn.scan({
    event: "event",
    qr_data: "qr_data"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.ScanTicketRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckInClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.checkIn.<a href="/src/api/resources/business/resources/events/resources/checkIn/client/Client.ts">stats</a>({ ...params }) -> FiveOneEat.StatsCheckInResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns ticket counts and check-in rate for the event dashboard.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.checkIn.stats({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.StatsCheckInRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckInClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.events.checkIn.<a href="/src/api/resources/business/resources/events/resources/checkIn/client/Client.ts">recent</a>({ ...params }) -> FiveOneEat.RecentCheckInResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns checked-in tickets ordered by check-in time descending.
Accepts an optional `limit` query param (default `20`, max `100`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.events.checkIn.recent({
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.events.RecentCheckInRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckInClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Hours Exceptions
<details><summary><code>client.business.hours.exceptions.<a href="/src/api/resources/business/resources/hours/resources/exceptions/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateExceptionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.hours.exceptions.create({
    starts_on: "2024-01-15T09:30:00Z",
    is_closed: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.hours.StoreBusinessHourExceptionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExceptionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.hours.exceptions.<a href="/src/api/resources/business/resources/hours/resources/exceptions/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.hours.exceptions.delete({
    exception: "exception"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.hours.DeleteExceptionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExceptionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.hours.exceptions.<a href="/src/api/resources/business/resources/hours/resources/exceptions/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateExceptionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.hours.exceptions.update({
    exception: "exception",
    starts_on: "2024-01-15T09:30:00Z",
    is_closed: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.hours.UpdateBusinessHourExceptionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExceptionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Menus Groups
<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListGroupsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.list({
    menu: "menu"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.ListGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateGroupsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.create({
    menu: "menu",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.StoreMenuGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetGroupsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.get({
    menu: "menu",
    group: "group"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.GetGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateGroupsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.update({
    menu: "menu",
    group: "group",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.UpdateMenuGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteGroupsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.delete({
    menu: "menu",
    group: "group"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.DeleteGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.groups.<a href="/src/api/resources/business/resources/menus/resources/groups/client/Client.ts">reorder</a>({ ...params }) -> FiveOneEat.ReorderGroupsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Batch-update sort_order for groups. Groups not belonging to this menu are silently skipped.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.groups.reorder({
    menu: "menu",
    groups: [{
            id: "id",
            sort_order: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.ReorderMenuGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GroupsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Menus Items
<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListItemsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.list({
    menu: "menu"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.ListItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateItemsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.create({
    menu: "menu",
    name: "name",
    price: 1.1,
    menu_group_id: "menu_group_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.StoreMenuItemRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetItemsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.get({
    menu: "menu",
    item: "item"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.GetItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateItemsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.update({
    menu: "menu",
    item: "item",
    name: "name",
    price: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.UpdateMenuItemRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteItemsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.delete({
    menu: "menu",
    item: "item"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.DeleteItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">reorder</a>({ ...params }) -> FiveOneEat.ReorderItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Batch-update sort_order for items. Items not belonging to this group are silently skipped.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.reorder({
    group: "group",
    items: [{
            id: "id",
            sort_order: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.ReorderMenuItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.<a href="/src/api/resources/business/resources/menus/resources/items/client/Client.ts">move</a>({ ...params }) -> FiveOneEat.MoveItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Moves the item to the target group at the specified sort order, shifting existing items to make room.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.move({
    item: "item",
    target_group_id: "target_group_id",
    new_sort_order: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.MoveMenuItemRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Menus Items Variations
<details><summary><code>client.business.menus.items.variations.<a href="/src/api/resources/business/resources/menus/resources/items/resources/variations/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListVariationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.variations.list({
    menuItem: "menuItem"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.ListVariationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VariationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.variations.<a href="/src/api/resources/business/resources/menus/resources/items/resources/variations/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateVariationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.variations.create({
    menuItem: "menuItem",
    name: "name",
    price: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.StoreMenuItemVariationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VariationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.variations.<a href="/src/api/resources/business/resources/menus/resources/items/resources/variations/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateVariationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.variations.update({
    variation: "variation",
    name: "name",
    price: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.UpdateMenuItemVariationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VariationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.variations.<a href="/src/api/resources/business/resources/menus/resources/items/resources/variations/client/Client.ts">delete</a>({ ...params }) -> FiveOneEat.DeleteVariationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.variations.delete({
    variation: "variation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.DeleteVariationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `VariationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Menus Items Modifiers
<details><summary><code>client.business.menus.items.modifiers.<a href="/src/api/resources/business/resources/menus/resources/items/resources/modifiers/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListModifiersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.modifiers.list({
    menuItem: "menuItem"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.ListModifiersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ModifiersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.modifiers.<a href="/src/api/resources/business/resources/menus/resources/items/resources/modifiers/client/Client.ts">attach</a>({ ...params }) -> FiveOneEat.AttachModifiersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates the modifier if it does not already exist (matched by name), then attaches it to the item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.modifiers.attach({
    menuItem: "menuItem",
    name: "name",
    price: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.StoreMenuItemModifierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ModifiersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.menus.items.modifiers.<a href="/src/api/resources/business/resources/menus/resources/items/resources/modifiers/client/Client.ts">detach</a>({ ...params }) -> FiveOneEat.DetachModifiersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the association between the modifier and the item. The modifier itself is not deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.menus.items.modifiers.detach({
    menuItem: "menuItem",
    modifier: "modifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.menus.items.DetachModifiersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ModifiersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Messaging Conversations
<details><summary><code>client.business.messaging.conversations.<a href="/src/api/resources/business/resources/messaging/resources/conversations/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of all conversations for the authenticated business,
ordered by the most recent message first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.conversations.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.ListConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.messaging.conversations.<a href="/src/api/resources/business/resources/messaging/resources/conversations/client/Client.ts">search</a>({ ...params }) -> FiveOneEat.SearchConversationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.conversations.search({
    q: "q"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.SearchConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.messaging.conversations.<a href="/src/api/resources/business/resources/messaging/resources/conversations/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve details of a specific conversation including the customer information
and the latest message.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.conversations.get({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.GetConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Messaging Messages
<details><summary><code>client.business.messaging.messages.<a href="/src/api/resources/business/resources/messaging/resources/messages/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of all messages in a specific conversation,
ordered by creation time (oldest first).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.messages.list({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.ListMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.messaging.messages.<a href="/src/api/resources/business/resources/messaging/resources/messages/client/Client.ts">send</a>({ ...params }) -> FiveOneEat.SendMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a new message to a specific conversation as the business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.messages.send({
    conversation: "550e8400-e29b-41d4-a716-446655440000",
    content: "content"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.StoreMessageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.messaging.messages.<a href="/src/api/resources/business/resources/messaging/resources/messages/client/Client.ts">markAsRead</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark all messages from the customer as read by the business user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.messages.markAsRead({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.MarkAsReadMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.messaging.messages.<a href="/src/api/resources/business/resources/messaging/resources/messages/client/Client.ts">unreadCount</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the count of unread messages from the customer in a specific conversation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.messaging.messages.unreadCount({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.messaging.UnreadCountMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Profile Logo
<details><summary><code>client.business.profile.logo.<a href="/src/api/resources/business/resources/profile/resources/logo/client/Client.ts">upload</a>({ ...params }) -> FiveOneEat.UploadLogoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Upload and replace the logo for the authenticated user's active business. Any existing logo file will be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.logo.upload({
    logo: fs.createReadStream("/path/to/your/file")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.profile.UploadLogoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LogoClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.profile.logo.<a href="/src/api/resources/business/resources/profile/resources/logo/client/Client.ts">delete</a>() -> FiveOneEat.DeleteLogoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove the logo for the authenticated user's active business, including the stored file.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.profile.logo.delete();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `LogoClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Shipping Account
<details><summary><code>client.business.shipping.account.<a href="/src/api/resources/business/resources/shipping/resources/account/client/Client.ts">get</a>() -> FiveOneEat.GetAccountResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.account.get();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.account.<a href="/src/api/resources/business/resources/shipping/resources/account/client/Client.ts">setupIntent</a>() -> FiveOneEat.SetupIntentAccountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Use the returned client_secret with the Stripe mobile SDK to collect
a payment method for label billing. Pass the resulting pm_* ID to
POST /shipping/account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.account.setupIntent();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.account.<a href="/src/api/resources/business/resources/shipping/resources/account/client/Client.ts">setup</a>({ ...params }) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Uses the business's Stripe Customer for label billing (created on first
use), attaches the provided payment method, and activates the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.account.setup({
    payment_method_id: "payment_method_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.shipping.SetupShippingAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.account.<a href="/src/api/resources/business/resources/shipping/resources/account/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateAccountResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.account.update();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.shipping.UpdateShippingAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.account.<a href="/src/api/resources/business/resources/shipping/resources/account/client/Client.ts">delete</a>() -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the billing card, turns shipping off and stops the online store
offering it (a ship-only store falls back to pickup). The Stripe customer
is kept for the next setup.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.account.delete();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Business Shipping Rates
<details><summary><code>client.business.shipping.rates.<a href="/src/api/resources/business/resources/shipping/resources/rates/client/Client.ts">list</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.rates.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `RatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.rates.<a href="/src/api/resources/business/resources/shipping/resources/rates/client/Client.ts">create</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.rates.create();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `RatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.rates.<a href="/src/api/resources/business/resources/shipping/resources/rates/client/Client.ts">update</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.rates.update({
    shippingRate: "shippingRate"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.shipping.UpdateRatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.business.shipping.rates.<a href="/src/api/resources/business/resources/shipping/resources/rates/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.business.shipping.rates.delete({
    shippingRate: "shippingRate"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.business.shipping.DeleteRatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Commerce Carts
<details><summary><code>client.commerce.carts.<a href="/src/api/resources/commerce/resources/carts/client/Client.ts">open</a>({ ...params }) -> FiveOneEat.OpenCartsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A signed-in buyer gets their open cart at the business for that
channel, made when they have none. A guest always gets a new cart.
The answer is the only one that shows the cart's `token`: send it as
`X-Cart-Token` on every other cart request. An `in_person` cart needs
a stand that sells in person; an `online` cart may name the store to
pick up from now or later. 404 for a business that isn't public.
422 `checkout_off` while the cart's checkout surface (web, app or
stand) is switched off.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.open({
    business: "business",
    channel: "online"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.OpenCartRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CartsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.carts.<a href="/src/api/resources/commerce/resources/carts/client/Client.ts">getCurrent</a>({ ...params }) -> FiveOneEat.GetCurrentCartsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The open cart `X-Cart-Token` names, with its lines flagged where they
can't be bought as the cart stands. `data` is null when the token
names no open cart, such as one whose order was paid. While selling is
paused the answer is always that.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.getCurrent({
    "X-Cart-Token": "X-Cart-Token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.GetCurrentCartsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CartsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.carts.<a href="/src/api/resources/commerce/resources/carts/client/Client.ts">updateCurrent</a>({ ...params }) -> FiveOneEat.UpdateCurrentCartsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Any of: the store or stand (`location_id`), which clears the pickup
time when it changes and leaves lines not offered there flagged; the
pickup time (`pickup_at`, a slot's `starts_at`, or null); the buyer's
details; the note. Applied in that order. An online cart takes a
location that offers pickup now, an in-person cart a stand that sells
in person now.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.updateCurrent({
    "X-Cart-Token": "X-Cart-Token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.UpdateCartRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CartsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.carts.<a href="/src/api/resources/commerce/resources/carts/client/Client.ts">listPickupSlots</a>({ ...params }) -> FiveOneEat.CatalogPickupSlots</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The pickup slots at the cart's location from `from` to `until`, on the
location's own clock: a week from today unless asked otherwise, and
at most 14 days. Each says how many places are left. A location that
doesn't take pickup orders at the moment has none. 422 for a cart with
no location yet, or an in-person cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.listPickupSlots({
    "X-Cart-Token": "X-Cart-Token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.ListPickupSlotsCartsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CartsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Commerce Checkout
<details><summary><code>client.commerce.checkout.<a href="/src/api/resources/commerce/resources/checkout/client/Client.ts">quote</a>({ ...params }) -> FiveOneEat.QuoteCheckoutResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

What the cart costs now, with sales tax per line and the service fee,
worked out at the chosen store. Show `total_cents` and send it to Pay
as `shown_total_cents`. `blocker` says why the cart can't be paid as
it stands. 503 `tax_unavailable` when sales tax can't be worked out
right now. 422 `checkout_off` while the cart's checkout surface (web,
app or stand) is switched off.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.checkout.quote({
    "X-Cart-Token": "X-Cart-Token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.QuoteCheckoutRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckoutClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.checkout.<a href="/src/api/resources/commerce/resources/checkout/client/Client.ts">pay</a>({ ...params }) -> FiveOneEat.PayResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Re-checks the store, re-prices the cart, takes the stock and the pickup
slot, and charges the confirmation token. `status` is `succeeded` (the
order is placed), `requires_action` (call `stripe.handleNextAction()`
with `client_secret`, then the payment result), `processing` (Stripe
is still taking the money) or `unconfirmed` (Stripe didn't answer; show
`message`).

A refusal has a `code` and a `message`: `selling_paused`,
`checkout_off` (the cart's checkout surface is switched off) and
`selling_blocked` (with `blocker`) 422, `total_changed` 409 (with the
new `quote`), `line_unavailable` 409 (with `line_ids`), `sold_out` 409
(with `line_id` and `available`), `slot_full` and `slot_unavailable`
409, `tax_not_collected` 422, `tax_unavailable` 503, `below_minimum`
422, `payment_in_progress` 409, `captcha_required` 428 (render
Turnstile with action `checkout` and send `captcha_token`),
`too_many_unfinished_orders` 429, and `payment_failed` 402.

Send a new `Idempotency-Key` for each tap: a retry with the same key
gets the first answer back.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.checkout.pay({
    "X-Cart-Token": "X-Cart-Token",
    "Idempotency-Key": "Idempotency-Key",
    shown_total_cents: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.PayRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckoutClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.checkout.<a href="/src/api/resources/commerce/resources/checkout/client/Client.ts">settlePayment</a>({ ...params }) -> FiveOneEat.PayResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

After `stripe.handleNextAction()`: reads the payment at Stripe and
places or cancels the order to match. Answers as Pay does;
`payment_failed` 402 when it didn't go through. Its cart's token or
its signed-in buyer may ask.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.checkout.settlePayment({
    "Idempotency-Key": "Idempotency-Key",
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.SettlePaymentCheckoutRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CheckoutClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Commerce Orders
<details><summary><code>client.commerce.orders.<a href="/src/api/resources/commerce/resources/orders/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The signed-in buyer's orders, newest first, 24 to a page. An order
whose payment is still in flight or never went through isn't listed.
While selling is paused the list is empty.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.orders.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.ListOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.orders.<a href="/src/api/resources/commerce/resources/orders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

One order, for its signed-in buyer, for whoever holds a signed link to
it (`signature` and the rest of the link's query, which never expires;
a guest's link shows only their own order), or for whoever holds the
token of the cart it was placed from.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.orders.get({
    order: "order"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.GetOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Commerce Carts Lines
<details><summary><code>client.commerce.carts.lines.<a href="/src/api/resources/commerce/resources/carts/resources/lines/client/Client.ts">add</a>({ ...params }) -> FiveOneEat.AddLinesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Puts a variant in the cart, or adds to its line when it's there. The
variant has to be the business's and for sale. An in-person cart takes
what its stand sells. An online cart takes what any of the business's
locations offers for pickup: when the cart's own store doesn't, a cart
with items keeps its store and the line comes back with `offered_here`
false (the quote blocks it until the buyer removes it or switches to a
store that offers it), and a cart with no items drops its store, so
`location` is null and the buyer chooses one. The quantity is in the
variant's unit, a whole number of its `quantity_step`, from 1 to 1000
steps. Answers with the cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.lines.add({
    "X-Cart-Token": "X-Cart-Token",
    variant_id: "variant_id",
    quantity: "quantity"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.carts.CartLineRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.carts.lines.<a href="/src/api/resources/commerce/resources/carts/resources/lines/client/Client.ts">remove</a>({ ...params }) -> FiveOneEat.RemoveLinesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Answers with the cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.lines.remove({
    "X-Cart-Token": "X-Cart-Token",
    line: "line"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.carts.RemoveLinesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.commerce.carts.lines.<a href="/src/api/resources/commerce/resources/carts/resources/lines/client/Client.ts">change</a>({ ...params }) -> FiveOneEat.ChangeLinesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The quantity follows the same rules as adding. Answers with the cart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.commerce.carts.lines.change({
    "X-Cart-Token": "X-Cart-Token",
    line: "line",
    quantity: "quantity"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.commerce.carts.ChangeCartLineRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Ads
<details><summary><code>client.customer.ads.<a href="/src/api/resources/customer/resources/ads/client/Client.ts">serve</a>({ ...params }) -> FiveOneEat.ServeAdsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns an active advertisement for the given placement, or no content if none is available.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.ads.serve({
    placement: "placement"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ServeAdsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AdsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.ads.<a href="/src/api/resources/customer/resources/ads/client/Client.ts">recordClick</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Records a click on an active advertisement for attribution.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.ads.recordClick({
    advertisement: "advertisement"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.RecordClickAdsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AdsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Auth
<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">register</a>({ ...params }) -> FiveOneEat.RegisterAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new customer account and return an API token for immediate authentication.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.register({
    name: "name",
    email: "email",
    password: "password",
    device_name: "device_name",
    password_confirmation: "password_confirmation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.RegisterCustomerRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">login</a>({ ...params }) -> FiveOneEat.LoginAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Exchange user credentials for an API token that can be used for subsequent authenticated requests.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.login({
    email: "email",
    password: "password",
    device_name: "device_name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.LoginCustomerRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">forgotPassword</a>({ ...params }) -> FiveOneEat.ForgotPasswordAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sends a password reset link to the provided email address if an account exists.
Always returns a 200 response to prevent email enumeration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.forgotPassword({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.AppHttpRequestsApiV1CustomerAuthForgotPasswordRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">resetPassword</a>({ ...params }) -> FiveOneEat.ResetPasswordAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Validates the reset token and updates the user's password. All existing API tokens
are revoked after a successful reset, requiring re-authentication on all devices.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.resetPassword({
    token: "token",
    email: "email",
    password: "password",
    password_confirmation: "password_confirmation"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.AppHttpRequestsApiV1CustomerAuthResetPasswordRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">me</a>() -> FiveOneEat.MeAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the current authenticated user's profile information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.me();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">updateProfile</a>({ ...params }) -> FiveOneEat.UpdateProfileAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update name, email, phone, and/or password. All fields are optional. Send `phone: null` to clear it. To change the
password, `current_password` must be provided alongside `password` and `password_confirmation`.
Changing the email clears its verification.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.updateProfile();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.UpdateUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">deleteAccount</a>({ ...params }) -> FiveOneEat.DeleteAccountAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete the account and its associated data, cancel any billing,
and revoke every API token. This cannot be undone. Requires the current
password for confirmation. Accounts that manage a business cannot be deleted
here and return a 422 explaining how to proceed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.deleteAccount({
    password: "password"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.DeleteAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">uploadAvatar</a>({ ...params }) -> FiveOneEat.UploadAvatarAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Upload and replace the avatar for the authenticated customer. The previous avatar file is deleted once the new one is stored.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.uploadAvatar({
    avatar: "avatar"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.UploadAvatarRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">deleteAvatar</a>() -> FiveOneEat.DeleteAvatarAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove the avatar for the authenticated customer. Returns the updated user with a null avatar_url.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.deleteAvatar();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">logout</a>() -> FiveOneEat.LogoutAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke the current API token and log out the user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.logout();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.<a href="/src/api/resources/customer/resources/auth/client/Client.ts">logoutAll</a>() -> FiveOneEat.LogoutAllAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke all API tokens for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.logoutAll();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer BusinessSubmissions
<details><summary><code>client.customer.businessSubmissions.<a href="/src/api/resources/customer/resources/businessSubmissions/client/Client.ts">list</a>() -> FiveOneEat.ListBusinessSubmissionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businessSubmissions.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BusinessSubmissionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businessSubmissions.<a href="/src/api/resources/customer/resources/businessSubmissions/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateBusinessSubmissionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

When it matches unclaimed listings already on the map (same phone,
website domain, or name within 2 km), nothing is submitted and the
response is 409 with those listings in `existing_listings`: show them,
offer the owner the claim flow, or send `submit_anyway: true`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businessSubmissions.create({
    name: "name",
    address: "address",
    city: "city",
    state: "state",
    zipcode: "zipcode",
    country: "country",
    latitude: 1.1,
    longitude: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.StoreBusinessSubmissionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessSubmissionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businessSubmissions.<a href="/src/api/resources/customer/resources/businessSubmissions/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetBusinessSubmissionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businessSubmissions.get({
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.GetBusinessSubmissionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessSubmissionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Businesses
<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">profile</a>({ ...params }) -> FiveOneEat.ProfileBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve core business information for the profile page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.profile({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ProfileBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">menus</a>({ ...params }) -> FiveOneEat.MenusBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all menus organized by groups for the business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.menus({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.MenusBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">photos</a>({ ...params }) -> FiveOneEat.PhotosBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve photo gallery for the business with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.photos({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.PhotosBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">listTemporaryLocations</a>({ ...params }) -> FiveOneEat.ListTemporaryLocationsBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve active and upcoming temporary locations for a business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.listTemporaryLocations({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ListTemporaryLocationsBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">getPickupTimeslots</a>({ ...params }) -> FiveOneEat.GetPickupTimeslotsBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the pickup timeslots still open at a business's main store on a
given date, as `HH:MM` start times in the store's local time. Kept for
older app builds until the relaunch replaces it.

- A slot is listed only when it starts before its pickup window closes,
  so the closing time itself is not a slot.
- Full slots (every place taken) are left out.
- Days the store is closed or has no pickup, and slots inside its
  preparation time, return no slots.
- A business without a main store gets `"timeslots": []`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.getPickupTimeslots({
    handle: "katzs-deli",
    date: "2023-01-15"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.GetPickupTimeslotsBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">favorite</a>({ ...params }) -> FiveOneEat.FavoriteBusinessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a business to the authenticated user's favorites.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.favorite({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.FavoriteBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.<a href="/src/api/resources/customer/resources/businesses/client/Client.ts">unfavorite</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a business from the authenticated user's favorites.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.unfavorite({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.UnfavoriteBusinessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BusinessesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Catalog
<details><summary><code>client.customer.catalog.<a href="/src/api/resources/customer/resources/catalog/client/Client.ts">listLocations</a>({ ...params }) -> FiveOneEat.ListLocationsCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The stores and stands buyers can use: the main store first, then the
other stores and the stands by name. Switched-off and archived
locations are left out, and so are extra stores the owner's plan
doesn't cover. 404 unless the business is public.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.catalog.listLocations({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ListLocationsCatalogRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CatalogClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.catalog.<a href="/src/api/resources/customer/resources/catalog/client/Client.ts">listProducts</a>({ ...params }) -> FiveOneEat.ListProductsCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The products on offer at one location, 24 to a page: at the main store
unless `location` says otherwise, bought online (pickup) unless
`channel` says otherwise. `location=any` lists what's offered online
at any listed store. Prices are the public price, whoever asks. A
location that isn't listed is a 404, as is a business that isn't
public.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.catalog.listProducts({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ListProductsCatalogRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CatalogClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.catalog.<a href="/src/api/resources/customer/resources/catalog/client/Client.ts">getProduct</a>({ ...params }) -> FiveOneEat.GetProductCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

One product, as the list shows it. 404 when it isn't offered at that
location this way.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.catalog.getProduct({
    business: "katzs-deli",
    product: "pasture-raised-eggs"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.GetProductCatalogRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CatalogClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.catalog.<a href="/src/api/resources/customer/resources/catalog/client/Client.ts">listCategories</a>({ ...params }) -> FiveOneEat.ListCategoriesCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The categories with at least one product on offer where the list of
products would look, with the same `location` and `channel` filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.catalog.listCategories({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ListCategoriesCatalogRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CatalogClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.catalog.<a href="/src/api/resources/customer/resources/catalog/client/Client.ts">listPickupSlots</a>({ ...params }) -> FiveOneEat.CatalogPickupSlots</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The pickup slots from a day, `days` of them (7 by default, 14 at most),
each with whether every place is taken. Times are on the location's
own clock. A location that doesn't take pickup orders at the moment
has no slots. 404 unless the location is listed and its business is
public.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.catalog.listPickupSlots({
    location: "location"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ListPickupSlotsCatalogRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CatalogClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Discovery
<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">feed</a>({ ...params }) -> FiveOneEat.DiscoveryFeed</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of populated business categories, each with up to 10 businesses
embedded. Use `total_businesses` to link to the full paginated category view.
Supports optional filtering by search term, cuisines, and certifications.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.feed();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.FeedDiscoveryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">highlights</a>() -> FiveOneEat.DiscoveryHighlights</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns curated sections of businesses for the discovery home screen,
including staff picks and founding partners. This endpoint is designed
to be extended with additional sections (e.g. editorial, trending) over time.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.highlights();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">categories</a>({ ...params }) -> FiveOneEat.CategoriesDiscoveryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all business categories with their business counts.
This endpoint is used to populate category filters and navigation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.categories();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.CategoriesDiscoveryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">cuisines</a>() -> FiveOneEat.CuisinesDiscoveryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all cuisines, ordered alphabetically.
This endpoint is used to populate cuisine filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.cuisines();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">certifications</a>() -> FiveOneEat.CertificationsDiscoveryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all certifications, ordered alphabetically.
This endpoint is used to populate certification filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.certifications();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">allergens</a>() -> FiveOneEat.AllergensDiscoveryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all allergens, ordered alphabetically, for use in
filters, labels, and other customer-facing display.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.allergens();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.discovery.<a href="/src/api/resources/customer/resources/discovery/client/Client.ts">categoryBusinesses</a>({ ...params }) -> FiveOneEat.CategoryBusinessesDiscoveryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve businesses for a specific category with pagination support.
Results are optimized for list display.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.discovery.categoryBusinesses({
    category: "restaurant"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.CategoryBusinessesDiscoveryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DiscoveryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Explore
<details><summary><code>client.customer.explore.<a href="/src/api/resources/customer/resources/explore/client/Client.ts">businesses</a>({ ...params }) -> FiveOneEat.BusinessesExploreResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve businesses within the specified map bounds for map view.
Results are optimized for map display with essential business information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.explore.businesses({
    bounds: "bounds"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.BusinessesExploreRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExploreClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Editorials
<details><summary><code>client.customer.editorials.<a href="/src/api/resources/customer/resources/editorials/client/Client.ts">list</a>() -> FiveOneEat.ListEditorialsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a paginated list of published editorials with basic business info.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.editorials.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `EditorialsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.editorials.<a href="/src/api/resources/customer/resources/editorials/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetEditorialsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a published editorial by slug, with the full augmented body
including resolved menu item, product, and event references.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.editorials.get({
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.GetEditorialsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EditorialsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Events
<details><summary><code>client.customer.events.<a href="/src/api/resources/customer/resources/events/client/Client.ts">feed</a>({ ...params }) -> FiveOneEat.FeedEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated feed of upcoming events across all businesses.
Defaults to all events starting from now, ordered by start date ascending.
Optionally filter by a date range using date_from and date_to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.feed();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.FeedEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Messaging
<details><summary><code>client.customer.messaging.<a href="/src/api/resources/customer/resources/messaging/client/Client.ts">channelAuth</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint is used by the mobile app to authenticate with Pusher channels.
It validates that the user has permission to access the requested channel.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.channelAuth({
    channel_name: "channel_name",
    socket_id: "socket_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.ChannelAuthMessagingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me
<details><summary><code>client.customer.me.<a href="/src/api/resources/customer/resources/me/client/Client.ts">favoriteFacets</a>() -> FiveOneEat.FavoriteFacetsMeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The filter options available for this user's favorites — only taxonomies
actually present among them, each with a count. An option that cannot
match anything is never returned.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.favoriteFacets();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MeClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.<a href="/src/api/resources/customer/resources/me/client/Client.ts">favorites</a>({ ...params }) -> FiveOneEat.FavoritesMeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The authenticated user's favorited businesses, optionally narrowed by
search term and taxonomy facets. Values within one facet are OR; separate
facets compose as AND.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.favorites();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.FavoritesMeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MeClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.<a href="/src/api/resources/customer/resources/me/client/Client.ts">rsvps</a>({ ...params }) -> FiveOneEat.RsvpsMeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the authenticated user's event RSVPs with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.rsvps();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.RsvpsMeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MeClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer ProductOrders
<details><summary><code>client.customer.productOrders.<a href="/src/api/resources/customer/resources/productOrders/client/Client.ts">list</a>() -> FiveOneEat.ListProductOrdersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.productOrders.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.productOrders.<a href="/src/api/resources/customer/resources/productOrders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetProductOrdersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.productOrders.get({
    productOrder: "productOrder"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.GetProductOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer PushNotifications
<details><summary><code>client.customer.pushNotifications.<a href="/src/api/resources/customer/resources/pushNotifications/client/Client.ts">register</a>({ ...params }) -> FiveOneEat.RegisterPushNotificationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register (or update) the authenticated user's Expo push token for a device. If
a `device_id` is provided, an existing registration for that device is updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.pushNotifications.register({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.AppHttpRequestsApiV1CustomerPushTokensStorePushTokenRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PushNotificationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.pushNotifications.<a href="/src/api/resources/customer/resources/pushNotifications/client/Client.ts">unregister</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete the authenticated user's Expo push token registration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.pushNotifications.unregister({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.UnregisterPushNotificationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PushNotificationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Stands
<details><summary><code>client.customer.stands.<a href="/src/api/resources/customer/resources/stands/client/Client.ts">notice</a>({ ...params }) -> FiveOneEat.NoticeStandsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

What the app shows for a stand link or the "You're at a stand" card
instead of stand checkout: the stand, its business, and a title and
message the server sets. Doesn't log a scan.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.stands.notice({
    stand: "stand"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.NoticeStandsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.stands.<a href="/src/api/resources/customer/resources/stands/client/Client.ts">nearby</a>({ ...params }) -> FiveOneEat.NearbyStandsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The nearest stands that can take a payment right now, closest first:
up to 20 within 50 km. `is_here` marks a stand within the arrival
radius (`meta.arrival_radius_meters`), where the app offers its
self-checkout without a QR scan. The coordinates are used for this
lookup only and are never stored.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.stands.nearby({
    latitude: 1.1,
    longitude: 1.1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.NearbyStandsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StandsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Auth Tokens
<details><summary><code>client.customer.auth.tokens.<a href="/src/api/resources/customer/resources/auth/resources/tokens/client/Client.ts">list</a>() -> FiveOneEat.ListTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a list of all API tokens for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.tokens.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TokensClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.auth.tokens.<a href="/src/api/resources/customer/resources/auth/resources/tokens/client/Client.ts">revoke</a>({ ...params }) -> FiveOneEat.RevokeTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a specific API token by its ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.auth.tokens.revoke({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.auth.RevokeTokensRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TokensClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer BusinessSubmissions Photos
<details><summary><code>client.customer.businessSubmissions.photos.<a href="/src/api/resources/customer/resources/businessSubmissions/resources/photos/client/Client.ts">upload</a>({ ...params }) -> FiveOneEat.UploadPhotosResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businessSubmissions.photos.upload({
    image: fs.createReadStream("/path/to/your/file"),
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businessSubmissions.UploadSubmissionPhotoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhotosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businessSubmissions.photos.<a href="/src/api/resources/customer/resources/businessSubmissions/resources/photos/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businessSubmissions.photos.delete({
    business: "business",
    photo: "photo"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businessSubmissions.DeletePhotosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhotosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Businesses Bulletins
<details><summary><code>client.customer.businesses.bulletins.<a href="/src/api/resources/customer/resources/businesses/resources/bulletins/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListBulletinsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve business announcements and updates with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.bulletins.list({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.ListBulletinsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BulletinsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Businesses Events
<details><summary><code>client.customer.businesses.events.<a href="/src/api/resources/customer/resources/businesses/resources/events/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve upcoming events for the business with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.events.list({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.ListEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.events.<a href="/src/api/resources/customer/resources/businesses/resources/events/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve full details for a single upcoming event belonging to the business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.events.get({
    business: "katzs-deli",
    event: "event"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.GetEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.events.<a href="/src/api/resources/customer/resources/businesses/resources/events/client/Client.ts">rsvp</a>({ ...params }) -> FiveOneEat.RsvpEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create or update the authenticated user's RSVP for a business event.
Ticketed events and events that have ended take no RSVPs (404).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.events.rsvp({
    business: "katzs-deli",
    event: "01950e7d-1234-7000-abcd-ef0123456789",
    status: "attending"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.StoreEventRsvpRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.events.<a href="/src/api/resources/customer/resources/businesses/resources/events/client/Client.ts">cancelRsvp</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel the authenticated user's RSVP for a business event.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.events.cancelRsvp({
    business: "katzs-deli",
    event: "01950e7d-1234-7000-abcd-ef0123456789"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.CancelRsvpEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Businesses Bulletins Comments
<details><summary><code>client.customer.businesses.bulletins.comments.<a href="/src/api/resources/customer/resources/businesses/resources/bulletins/resources/comments/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListCommentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve paginated comments for a published business bulletin.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.bulletins.comments.list({
    business: "katzs-deli",
    bulletin: "01950e7d-1234-7000-abcd-ef0123456789"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.bulletins.ListCommentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.bulletins.comments.<a href="/src/api/resources/customer/resources/businesses/resources/bulletins/resources/comments/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateCommentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Post a comment on a business bulletin. Requires authentication.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.bulletins.comments.create({
    business: "katzs-deli",
    bulletin: "01950e7d-1234-7000-abcd-ef0123456789",
    body: "body"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.bulletins.AppHttpRequestsApiV1CustomerBusinessesStoreBulletinCommentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.bulletins.comments.<a href="/src/api/resources/customer/resources/businesses/resources/bulletins/resources/comments/client/Client.ts">listReplies</a>({ ...params }) -> FiveOneEat.ListRepliesCommentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve paginated replies for a top-level comment on a published bulletin.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.bulletins.comments.listReplies({
    business: "katzs-deli",
    bulletin: "01950e7d-1234-7000-abcd-ef0123456789",
    comment: "01950e7d-5678-7000-abcd-ef0123456789"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.bulletins.ListRepliesCommentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.businesses.bulletins.comments.<a href="/src/api/resources/customer/resources/businesses/resources/bulletins/resources/comments/client/Client.ts">reply</a>({ ...params }) -> FiveOneEat.ReplyCommentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Post a reply to a top-level comment on a published bulletin. Requires authentication.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.businesses.bulletins.comments.reply({
    business: "katzs-deli",
    bulletin: "01950e7d-1234-7000-abcd-ef0123456789",
    comment: "01950e7d-5678-7000-abcd-ef0123456789",
    body: "body"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.businesses.bulletins.StoreBulletinCommentReplyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CommentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Events Ticketing
<details><summary><code>client.customer.events.ticketing.<a href="/src/api/resources/customer/resources/events/resources/ticketing/client/Client.ts">holdTickets</a>({ ...params }) -> FiveOneEat.HoldTicketsTicketingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Place a temporary hold on tickets for the specified event. Holds expire after 10 minutes.
A 403 means no ticket type is on sale, or a requested one isn't (inactive, or outside its
sales window). A sold-out
event answers 422, like any hold that asks for more tickets than are left.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.ticketing.holdTickets({
    eventId: "eventId",
    tickets: [{
            ticket_type_id: "ticket_type_id",
            quantity: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.events.StoreTicketHoldRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.events.ticketing.<a href="/src/api/resources/customer/resources/events/resources/ticketing/client/Client.ts">releaseHold</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Release the TicketCart holds for the authenticated user and event. Allowed whatever the
event's sales state; another buyer's cart, or one already gone, is left alone (204).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.ticketing.releaseHold({
    eventId: "eventId",
    cartId: "cartId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.events.ReleaseHoldTicketingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.events.ticketing.<a href="/src/api/resources/customer/resources/events/resources/ticketing/client/Client.ts">calculatePrice</a>({ ...params }) -> FiveOneEat.CalculatePriceTicketingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Preview the subtotal, platform fee, and total for a given ticket selection.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.ticketing.calculatePrice({
    eventId: "eventId",
    tickets: [{
            ticket_type_id: "ticket_type_id",
            quantity: 1
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.events.CalculatePriceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.events.ticketing.<a href="/src/api/resources/customer/resources/events/resources/ticketing/client/Client.ts">createPaymentIntent</a>({ ...params }) -> FiveOneEat.CreatePaymentIntentTicketingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Stripe payment intent for the tickets held in the cart for the given event.
Returns a client_secret for the mobile app to confirm payment with Stripe.

A 409 `{status: "paid", message, payment_intent_id}` means these tickets
are already paid for (the webhook issues them; never pay twice). A 409
`{status: "processing", message}` means the payment is still in flight.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.ticketing.createPaymentIntent({
    eventId: "eventId",
    billing_address: {
        line1: "line1",
        city: "city",
        state: "state",
        postal_code: "postal_code",
        country: "country"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.events.CreatePaymentIntentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.events.ticketing.<a href="/src/api/resources/customer/resources/events/resources/ticketing/client/Client.ts">confirmOrder</a>({ ...params }) -> FiveOneEat.ConfirmOrderTicketingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Confirm a completed Stripe payment and create the ticket order.
The payment must have succeeded before calling this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.events.ticketing.confirmOrder({
    eventId: "eventId",
    payment_intent_id: "payment_intent_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.events.StoreTicketOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me Lists
<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">list</a>() -> FiveOneEat.ListListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Every list the authenticated user owns, newest first, each carrying a
cover image drawn from its most recently added business.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new list for the authenticated user. A public list is readable
by anyone holding its share link.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.create({
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.StoreBusinessListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">memberships</a>({ ...params }) -> FiveOneEat.MembershipsListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Which of the authenticated user's lists already contain this business.
Backs the checkbox state in a save-to-list sheet.

Scoped to the caller's own lists, so there is nothing here another user
could learn.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.memberships({
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.MembershipsListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one of the authenticated user's own lists with its businesses.

Owner-only. `view` would return true for any public list, which would
expose this owner-scoped payload — including delisted businesses — to a
signed-in stranger. Strangers read a shared list through the public
endpoint instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.get({
    businessList: "businessList"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.GetListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Change a list's name, description, or visibility.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.update({
    businessList: "businessList",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.UpdateBusinessListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.<a href="/src/api/resources/customer/resources/me/resources/lists/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a list and its notes. The businesses themselves are
unaffected.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.delete({
    businessList: "businessList"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.DeleteListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ListsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me Tickets
<details><summary><code>client.customer.me.tickets.<a href="/src/api/resources/customer/resources/me/resources/tickets/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListTicketsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the authenticated user's tickets with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.tickets.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.ListTicketsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.tickets.<a href="/src/api/resources/customer/resources/me/resources/tickets/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetTicketsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single ticket belonging to the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.tickets.get({
    ticketId: "ticketId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.GetTicketsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.tickets.<a href="/src/api/resources/customer/resources/me/resources/tickets/client/Client.ts">appleWalletPass</a>({ ...params }) -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a signed .pkpass file for import into Apple Wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.tickets.appleWalletPass({
    ticketId: "ticketId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.AppleWalletPassTicketsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me TicketOrders
<details><summary><code>client.customer.me.ticketOrders.<a href="/src/api/resources/customer/resources/me/resources/ticketOrders/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListTicketOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the authenticated user's ticket orders with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.ticketOrders.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.ListTicketOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.ticketOrders.<a href="/src/api/resources/customer/resources/me/resources/ticketOrders/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetTicketOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single ticket order belonging to the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.ticketOrders.get({
    orderId: "orderId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.GetTicketOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TicketOrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me Addresses
<details><summary><code>client.customer.me.addresses.<a href="/src/api/resources/customer/resources/me/resources/addresses/client/Client.ts">list</a>() -> FiveOneEat.ListAddressesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all saved addresses for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.addresses.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AddressesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.addresses.<a href="/src/api/resources/customer/resources/me/resources/addresses/client/Client.ts">create</a>({ ...params }) -> FiveOneEat.CreateAddressesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Save a new address to the authenticated user's account. If this is the first address,
or if `is_default` is true, it will be set as the default (clearing any existing default).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.addresses.create({
    line1: "line1",
    city: "city",
    state: "state",
    postal_code: "postal_code",
    country: "country"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.StoreAddressRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AddressesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.addresses.<a href="/src/api/resources/customer/resources/me/resources/addresses/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a saved address. If the deleted address was the default,
the most recently created remaining address is promoted to default.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.addresses.delete({
    address: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.DeleteAddressesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AddressesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.addresses.<a href="/src/api/resources/customer/resources/me/resources/addresses/client/Client.ts">update</a>({ ...params }) -> FiveOneEat.UpdateAddressesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a saved address. If `is_default` is true, the previous default address will be cleared.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.addresses.update({
    address: 1,
    body: {
        line1: "line1",
        city: "city",
        state: "state",
        postal_code: "postal_code",
        country: "country"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.UpdateAddressesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AddressesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me PaymentMethods
<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">setupIntent</a>() -> FiveOneEat.SetupIntentPaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a Stripe SetupIntent client_secret. Use this with the Stripe mobile SDK
to present the payment sheet and collect card details. Once confirmed, pass the
resulting payment method ID to the store endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.setupIntent();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">ephemeralKey</a>() -> FiveOneEat.EphemeralKeyPaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the Stripe customer id and an ephemeral key secret. Pass these to the
Stripe mobile SDK's `initPaymentSheet` as `customerId` and
`customerEphemeralKeySecret` so the sheet lists the customer's saved cards.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.ephemeralKey();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">customerSession</a>() -> FiveOneEat.CustomerSessionPaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the Stripe customer id and a CustomerSession client secret. Pass these to the
Stripe mobile SDK's `initPaymentSheet` as `customerId` and
`customerSessionClientSecret`. Use this instead of the ephemeral key when the sheet
is built with `confirmationTokenConfirmHandler` (a deferred intent), which Stripe
does not allow with an ephemeral key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.customerSession();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">list</a>() -> FiveOneEat.PaymentMethod[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all saved cards for the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">add</a>({ ...params }) -> FiveOneEat.AddPaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Attaches a confirmed payment method to the customer's account. If `is_default` is
true, or this is the first card saved, it becomes the default payment method.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.add({
    payment_method: "payment_method"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.StorePaymentMethodRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">setDefault</a>({ ...params }) -> FiveOneEat.SetDefaultPaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Marks an existing saved payment method as the default.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.setDefault({
    paymentMethod: "paymentMethod"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.SetDefaultPaymentMethodsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.paymentMethods.<a href="/src/api/resources/customer/resources/me/resources/paymentMethods/client/Client.ts">delete</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes a saved payment method from the customer's account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.paymentMethods.delete({
    paymentMethod: "paymentMethod"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.DeletePaymentMethodsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentMethodsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Me Lists Items
<details><summary><code>client.customer.me.lists.items.<a href="/src/api/resources/customer/resources/me/resources/lists/resources/items/client/Client.ts">add</a>({ ...params }) -> FiveOneEat.AddItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Save a business to one of the authenticated user's lists, with an
optional note. Idempotent: adding a business already in the list leaves
the existing entry and its note untouched.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.items.add({
    businessList: "businessList",
    business: "business"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.lists.AddListItemRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.items.<a href="/src/api/resources/customer/resources/me/resources/lists/resources/items/client/Client.ts">remove</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a business and its note from a list. The business itself is
unaffected.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.items.remove({
    businessList: "businessList",
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.lists.RemoveItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.me.lists.items.<a href="/src/api/resources/customer/resources/me/resources/lists/resources/items/client/Client.ts">updateNote</a>({ ...params }) -> FiveOneEat.UpdateNoteItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Change the note attached to one business within one list. Notes are
per-list, so the same business can carry a different note elsewhere.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.me.lists.items.updateNote({
    businessList: "businessList",
    business: "katzs-deli"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.me.lists.UpdateListItemNoteRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ItemsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Messaging Conversations
<details><summary><code>client.customer.messaging.conversations.<a href="/src/api/resources/customer/resources/messaging/resources/conversations/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of all conversations for the authenticated customer,
ordered by the most recent message first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.conversations.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.ListConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.conversations.<a href="/src/api/resources/customer/resources/messaging/resources/conversations/client/Client.ts">search</a>({ ...params }) -> FiveOneEat.SearchConversationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.conversations.search({
    q: "q"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.SearchConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.conversations.<a href="/src/api/resources/customer/resources/messaging/resources/conversations/client/Client.ts">start</a>({ ...params }) -> FiveOneEat.StartConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new conversation between the authenticated customer and the specified business.
If a conversation already exists, it will be returned instead of creating a duplicate.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.conversations.start({
    business: "marios-pizza"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.StartConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.conversations.<a href="/src/api/resources/customer/resources/messaging/resources/conversations/client/Client.ts">get</a>({ ...params }) -> FiveOneEat.GetConversationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve details of a specific conversation including the business information
and the latest message.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.conversations.get({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.GetConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.conversations.<a href="/src/api/resources/customer/resources/messaging/resources/conversations/client/Client.ts">delete</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a conversation and all its messages.
This action cannot be undone.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.conversations.delete({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.DeleteConversationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Customer Messaging Messages
<details><summary><code>client.customer.messaging.messages.<a href="/src/api/resources/customer/resources/messaging/resources/messages/client/Client.ts">list</a>({ ...params }) -> FiveOneEat.ListMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of all messages in a specific conversation,
ordered by creation time (oldest first).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.messages.list({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.ListMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.messages.<a href="/src/api/resources/customer/resources/messaging/resources/messages/client/Client.ts">send</a>({ ...params }) -> FiveOneEat.SendMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a new message to a specific conversation. The message will be marked
as sent by the authenticated customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.messages.send({
    conversation: "550e8400-e29b-41d4-a716-446655440000",
    content: "content"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.AppHttpRequestsApiV1CustomerMessagingStoreMessageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.messages.<a href="/src/api/resources/customer/resources/messaging/resources/messages/client/Client.ts">markAsRead</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark all messages in a conversation as read by the authenticated customer.
This is typically called when the customer opens a conversation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.messages.markAsRead({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.MarkAsReadMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customer.messaging.messages.<a href="/src/api/resources/customer/resources/messaging/resources/messages/client/Client.ts">unreadCount</a>({ ...params }) -> number</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the count of unread messages in a specific conversation for the authenticated customer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customer.messaging.messages.unreadCount({
    conversation: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `FiveOneEat.customer.messaging.UnreadCountMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MessagesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

