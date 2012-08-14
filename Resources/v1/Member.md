# Member 

## Retrieve a Member

Returns a specific Member object.

### URL
> /member/v1/{id}
> /member/v1/me _(coming soon)_

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
	"Entity":{
		"Apt":"String content",
		"BusinessUnitId":2,		
		"City":"String content",
		"CreatedDate":"2012-07-16T17:23:34Z",
		"DateOfBirth":"2012-07-16T17:23:34Z",
		"Email":"someone@gmail.com",
		"EndDate":"2012-07-16T17:23:34Z",
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
		"State":"String content",
		"Street":"String content",
		"UserName":"String content",
		"Zip":46142
	}
}
```

* Get Members

* Update a Member

* Change Password