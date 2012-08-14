# Family/v1 Documentation

## Retrieve a Family

Returns a specific Family object.

### URL
> GET /family/v1/{id}

> GET /family/v1/me _(coming soon)_

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
            <td>The family id. If the family id is <code>me</code> the current authenticated user's family will be returned.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/family/v1/123
```js
{
	"BusinessUnitId":2,
	"CreatedBy":123,
	"CreatedDate":"2012-07-16T17:23:34Z",
	"EnterpriseId":5,
	"Id":154,
	"Image":"String content",
	"IsActive":true,
	"Members":[{	
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
	}],
		"ModifiedDate":"2012-07-16T17:23:34Z",
		"Name":"String content"
}
```

## Update a Family

Updates a specific Family object.

### URL
> POST /family/v1/{id}

> POST /family/v1/me _(coming soon)_

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
            <td>The family id. If the family id is <code>me</code> the current authenticated user's family will be returned.</td>
        </tr>
		<tr>
            <td>Name</td>
            <td>Optional</td>
            <td>string</td>
            <td>The name of the family</td>
        </tr>
		<tr>
            <td>Image</td>
            <td>Optional</td>
            <td>string</td>
            <td>A url linking the family image.</td>
        </tr>		
    </tbody>
</table>

### Example

> POST http://localhost/rest/family/v1/154
```js
{
	"Image":"String content",	
	"Name":"String content"
}
```


## Retrieve a collection of Families

Returns a collection of Family objects.

### URL
> GET /family/v1/?index={index}&paging={paging}

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

> GET http://localhost/rest/family/v1/?index=1&paging=25
```js
{
	"Entities":[{
		"BusinessUnitId":2,
		"CreatedBy":234,
		"CreatedDate":"2012-07-16T17:23:34Z",
		"EnterpriseId":5,
		"Id":154,
		"Image":"String content",
		"IsActive":true,		
		"ModifiedDate":"2012-07-16T17:23:34Z",
		"Name":"String content"
	}],
	"Index":1,
	"Paging":25,
	"Total":1
}
```

## Create a Family

Creates a Family object.

### URL
> POST /family/v1/

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
            <td>Name</td>
            <td>Required</td>
            <td>string</td>
            <td>The name of the family</td>
        </tr>
		<tr>
            <td>Image</td>
            <td>Optional</td>
            <td>string</td>
            <td>A url linking the family image.</td>
        </tr>		
    </tbody>
</table>

### Example

> POST http://localhost/rest/family/v1/
```js
{
	"Image":"String content",	
	"Name":"String content"
}
```

> Response
```js
{
	"BusinessUnitId":2,
	"CreatedBy":123,
	"CreatedDate":"2012-07-16T17:23:34Z",
	"EnterpriseId":5,
	"Id":154,
	"Image":"String content",
	"IsActive":true,
	"Members":[{	
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
	}],
		"ModifiedDate":"2012-07-16T17:23:34Z",
		"Name":"String content"
}
```

## Delete a Family

Delete a specific Family object.

### URL
> DELETE /family/v1/{id}

> DELETE /family/v1/me _(coming soon)_

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
            <td>The family id. If the family id is <code>me</code> the current authenticated user's family will be returned.</td>
        </tr>
    </tbody>
</table>

### Example

> DELETE http://localhost/rest/family/v1/123

## Add a member to a family

Add a specific member to a family

### URL
> POST /family/v1/{id}/member/{memberid}

> POST /family/v1/{id}/member/me

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
            <td>The family id.</td>
        </tr>
		<tr>
            <td><code>{memberid}</code></td>
            <td>Required</td>
            <td>string</td>
            <td>The member id. If the member id is <code>me</code> the current authenticated user will be used.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/family/v1/154/member/123

## Retrieve a collection of Members in a Family

Retrieve a collection of Member objects in a Family.

### URL
> GET /family/v1/{id}/members?index={index}&paging={paging}

> GET /family/v1/me/members?index={index}&paging={paging}

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
            <td>The family id. If the family id is <code>me</code> the current authenticated user's family will be returned.</td>
        </tr>
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

> GET http://localhost/rest/family/v1/me/members?index=1&paging=25
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