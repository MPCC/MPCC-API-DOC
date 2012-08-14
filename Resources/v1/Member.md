# Member 

## Retrieve a Member

Returns a specific Member object.

### URL
> GET /member/v1/{id}

> GET /member/v1/me _(coming soon)_

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
            <td><code>{id}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The member id. If the member id is <code>me</code> the current authenticated user will be used.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/member/v1/123
```js
{	
	"Apt":"String content",
	"BusinessUnitId":2,		
	"City":"String content",
	"CreatedDate":"2012-07-16T17:23:34Z",
	"DateOfBirth":"1980-01-01T08:00:00Z",
	"Email":"someone@gmail.com",		
	"EnterpriseId":5,
	"FamilyId":154,
	"FirstName":"String content",
	"Image":"String content",
	"IsActive":true,
	"LastName":"String content",
	"LastVisitDate":"2012-07-16T17:23:34Z",
	"MemberId":123,
	"MiddleName":"String content",
	"ModifiedDate":"2012-07-16T17:23:34Z",
	"ProviderUserKey":"1627aea5-8e0a-4371-9022-9b504344e724",
	"StartDate":"2012-07-16T17:23:34Z",
	"State":"IN",
	"Street":"String content",
	"UserName":"String content",
	"Zip":46142	
}
```

## Update a Member

Updates a specific Member object.

### URL
> POST /member/v1/{id}

> POST /member/v1/me _(coming soon)_

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
            <td><code>{id}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The member id. If the member id is <code>me</code> the current authenticated user will be used.</td>
        </tr>
		<tr>
            <td>Apt</td>
            <td>Optional</td>
            <td>string</td>
            <td>The apartment of the member</td>
        </tr>
		<tr>
            <td>City</td>
            <td>Optional</td>
            <td>string</td>
            <td>The city of the member</td>
        </tr>
		<tr>
            <td>DateOfBirth</td>
            <td>Optional</td>
            <td>string</td>
            <td>The date of birth of the member. ISO86 date string format.</td>
        </tr>
		<tr>
            <td>FirstName</td>
            <td>Optional</td>
            <td>string</td>
            <td>The first name of the member.</td>
        </tr>
		<tr>
            <td>Image</td>
            <td>Optional</td>
            <td>string</td>
            <td>A url linking the member image.</td>
        </tr>
		<tr>
            <td>LastName</td>
            <td>Optional</td>
            <td>string</td>
            <td>The last name of the member.</td>
        </tr>
		<tr>
            <td>LastVisitDate</td>
            <td>Optional</td>
            <td>string</td>
            <td>The date that the member visited the church last. ISO86 date string format.</td>
        </tr>
		<tr>
            <td>MiddleName</td>
            <td>Optional</td>
            <td>string</td>
            <td>The middle name of the member.</td>
        </tr>
		<tr>
            <td>StartDate</td>
            <td>Optional</td>
            <td>string</td>
            <td>The date that the member first joined the church. ISO86 date string format.</td>
        </tr>
		<tr>
            <td>State</td>
            <td>Optional</td>
            <td>string</td>
            <td>The state the member resides in.</td>
        </tr>
		<tr>
            <td>Street</td>
            <td>Optional</td>
            <td>string</td>
            <td>The street address of the member.</td>
        </tr>
		<tr>
            <td>Zip</td>
            <td>Optional</td>
            <td>string</td>
            <td>The zip code of the member.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/member/v1/123
```js
{	
	"Apt":"String content",
	"City":"String content",
	"DateOfBirth":"1980-01-01T08:00:00Z",			
	"FamilyId":154,
	"FirstName":"String content",
	"Image":"String content",		
	"LastName":"String content",
	"LastVisitDate":"2012-07-16T17:23:34Z",		
	"MiddleName":"String content",		
	"StartDate":"2012-07-16T17:23:34Z",
	"State":"IN",
	"Street":"String content",		
	"Zip":46142	
}
```


## Retrieve a collection of Members

Returns a collection of Member objects.

### URL
> GET /member/v1/?index={index}&paging={paging}

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
            <td><code>{index}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The page in the data set to be queried.</td>
        </tr>
		<tr>
            <td><code>{paging}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The number of records to be returned in the page. Max is 100.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/member/v1/?index=1&paging=25
```js
{
    "Entities": [
        {	
			"Apt":"String content",
			"BusinessUnitId":2,		
			"City":"String content",
			"CreatedDate":"2012-07-16T17:23:34Z",
			"DateOfBirth":"1980-01-01T08:00:00Z",
			"Email":"someone@gmail.com",		
			"EnterpriseId":5,
			"FamilyId":154,
			"FirstName":"String content",
			"Image":"String content",
			"IsActive":true,
			"LastName":"String content",
			"LastVisitDate":"2012-07-16T17:23:34Z",
			"MemberId":123,
			"MiddleName":"String content",
			"ModifiedDate":"2012-07-16T17:23:34Z",
			"ProviderUserKey":"1627aea5-8e0a-4371-9022-9b504344e724",
			"StartDate":"2012-07-16T17:23:34Z",
			"State":"IN",
			"Street":"String content",
			"UserName":"String content",
			"Zip":46142	
		} 
    ],
    "Index": 1,
    "Paging": 25,
    "Total": 1
}
```

## Change password for a Member

Allows a member to change their password.

### URL
> POST /member/v1/{id}/changepassword

> POST /member/v1/me/changepassword _(coming soon)_

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
            <td><code>{id}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The member id. If the member id is <code>me</code> the current authenticated user will be used.</td>
        </tr>
		<tr>
            <td>oldpassword</td>
            <td>Required</td>
            <td>string</td>
            <td>The current password of the authenticated user.</td>
        </tr>
		<tr>
            <td>newpassword</td>
            <td>Required</td>
            <td>string</td>
            <td>The new password of the authenticated user.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/member/v1/123/changepassword
```js
{	
	"oldpassword":"String content",
	"newpassword":"String content"
}
```
