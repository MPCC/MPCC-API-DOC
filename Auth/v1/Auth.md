# Auth/v1 Documentation

## Retrieve a Token

Returns an oauth token for a given account context.

### URL
> POST /auth/v1/tokenrequest

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>password</td>
            <td>Required</td>
            <td>string</td>
            <td>The member password.</td>
        </tr>
		<tr>
            <td>username</td>
            <td>Required</td>
            <td>string</td>
            <td>The member username.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/auth/v1/tokenrequest
```js
{
	"password":"String content",
	"username":"String content"
}
```

> Response
```js
{
	"oauth_timestamp":"2012-07-16T17:23:34Z",
	"oauth_token":"String content"
}
```

## Refresh a Token

Returns a oauth token for a given account context.

### URL
> POST /auth/v1/tokenrefresh

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>oauth_token</td>
            <td>Required</td>
            <td>string</td>
            <td>The current authenticated oauth token.</td>
        </tr>
		<tr>
            <td>oauth_timestamp</td>
            <td>Optional</td>
            <td>string</td>
            <td>The oauth timestamp.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/auth/v1/tokenrefresh
```js
{
	"oauth_timestamp":"2012-07-16T17:23:34Z",
	"oauth_token":"String content"
}
```

> Response
```js
{
	"oauth_timestamp":"2012-08-16T17:23:34Z",
	"oauth_token":"String content"
}
```

## Register a Member

Returns a oauth token for a given account context.

### URL
> POST /auth/v1/registermember

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>password</td>
            <td>Required</td>
            <td>string</td>
            <td>The member password.</td>
        </tr>
		<tr>
            <td>username</td>
            <td>Required</td>
            <td>string</td>
            <td>The member username.</td>
        </tr>
		<tr>
            <td>email</td>
            <td>Required</td>
            <td>string</td>
            <td>The member email.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/auth/v1/registermember
```js
{
	"email":"someone@gmail.com",
	"password":"String content",
	"username":"String content"
}
```

> Response
```js
{
	"oauth_timestamp":"2012-07-16T17:23:34Z",
	"oauth_token":"String content"
}
```

## Logoff

Terminates an oauth token's access.

### URL
> POST /auth/v1/logoff

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>oauth_token</td>
            <td>Required</td>
            <td>string</td>
            <td>The current authenticated oauth token.</td>
        </tr>
		<tr>
            <td>oauth_timestamp</td>
            <td>Optional</td>
            <td>string</td>
            <td>The oauth timestamp.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/auth/v1/logoff
```js
{
	"oauth_timestamp":"2012-07-16T17:23:34Z",
	"oauth_token":"String content"
}
```

## Password Reset

Triggers the system password reset process for a given email. Only available three times per 24 hours.

### URL
> POST /auth/v1/passwordreset

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>       
		<tr>
            <td>email</td>
            <td>Required</td>
            <td>string</td>
            <td>The member email.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/auth/v1/passwordreset
```js
{
	"email":"someone@gmail.com"	
}
```

> Response
```js
{
	"message":"String content"
}
```