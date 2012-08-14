# Notification/v1 Documentation

## Retrieve a collection of Notifications

Returns a collection of Notification objects.

### URL
> GET /notification/v1/?index={index}&paging={paging}

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

> GET http://localhost/rest/notification/v1/?index=1&paging=25
```js
{
	"Entities":[{
		"ActionApi":"/family/v1/154/member/124",
		"ActionApiMethod":"POST",
		"ActionOccurred":false,
		"ActionText":"Add Jane Doe to the Doe family",
		"BusinessUnitID":2,
		"Category":"REQUEST",
		"CreatedDate":"2012-07-16T17:23:34Z",
		"EnterpriseID":5,
		"FromMemberID":124,
		"FromUsername":"Janedoe",
		"HasRead":false,
		"ID":231234,
		"IsActive":true,
		"Message":"Jane Doe has requested to join the Doe family.",
		"ModifiedDate":"2012-07-16T17:23:34Z",
		"Subject":"Family Member Join Request",
		"ToMemberID":123
	}],
	"Index":1,
	"Paging":25,
	"Total":1
}
```

## Retrieve a collection of sent Notifications

Returns a collection of sent Notification objects.

### URL
> GET /notification/v1/sent?index={index}&paging={paging}

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

> GET http://localhost/rest/notification/v1/sent?index=1&paging=25
```js
{
	"Entities":[{		
		"BusinessUnitID":2,
		"Category":"MESSAGE",
		"CreatedDate":"2012-07-16T17:23:34Z",
		"EnterpriseID":5,
		"FromMemberID":123,
		"FromUsername":"Johndoe",
		"HasRead":true,
		"ID":431234,
		"IsActive":true,
		"Message":"Hey Bob, Just wanted to see how things are going. Ping me when you get minute.",
		"ModifiedDate":"2012-07-16T17:23:34Z",
		"Subject":"How are things going",
		"ToMemberID":432
	}],
	"Index":1,
	"Paging":25,
	"Total":1
}
```

## Retrieve a Notification

Returns a specific Notification object.

### URL
> GET /notification/v1/{id}

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
            <td>The notification id.</td>
        </tr>
    </tbody>
</table>

### Example

> GET http://localhost/rest/notification/v1/231234
```js
{
	"ActionApi":"/family/v1/154/member/124",
	"ActionApiMethod":"POST",
	"ActionOccurred":false,
	"ActionText":"Add Jane Doe to the Doe family",
	"BusinessUnitID":2,
	"Category":"REQUEST",
	"CreatedDate":"2012-07-16T17:23:34Z",
	"EnterpriseID":5,
	"FromMemberID":124,
	"FromUsername":"Janedoe",
	"HasRead":false,
	"ID":231234,
	"IsActive":true,
	"Message":"Jane Doe has requested to join the Doe family.",
	"ModifiedDate":"2012-07-16T17:23:34Z",
	"Subject":"Family Member Join Request",
	"ToMemberID":123
}
```

## Create a Notification

Creates a Notification object.

### URL
> POST /notification/v1/

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
            <td>ActionApi</td>
            <td>Optional</td>
            <td>string</td>
            <td>API endpoint.</td>
        </tr>
		<tr>
            <td>ActionApiMethod</td>
            <td>Optional</td>
            <td>string</td>
            <td>HTTP Method (GET, POST, DELETE, PUT, PATCH).</td>
        </tr>
		<tr>
            <td>ActionText</td>
            <td>Optional</td>
            <td>string</td>
            <td>Text to be displayed on a control.</td>
        </tr>
		<tr>
            <td>Category</td>
            <td>Optional</td>
            <td>string</td>
            <td>Type of message (REQUEST, ALERT, MESSAGE)</td>
        </tr>
		<tr>
            <td>Message</td>
            <td>Required</td>
            <td>string</td>
            <td>The text body of the notification.</td>
        </tr>
		<tr>
            <td>Subject</td>
            <td>Optional</td>
            <td>string</td>
            <td>The subject text of the notification.</td>
        </tr>
		<tr>
            <td>ToMemberID</td>
            <td>Required</td>
            <td>int</td>
            <td>The id of the member the notification is going to.</td>
        </tr>		
    </tbody>
</table>

### Example

> POST http://localhost/rest/family/v1/
```js
{
	"ActionApi":"/family/v1/154/member/124",
	"ActionApiMethod":"POST",	
	"ActionText":"Add Jane Doe to the Doe family",
	"Category":"REQUEST",	
	"Message":"Jane Doe has requested to join the Doe family.",	
	"Subject":"Family Member Join Request",
	"ToMemberID":123
}
```

> Response
```js
{
	"ActionApi":"/family/v1/154/member/124",
	"ActionApiMethod":"POST",
	"ActionOccurred":false,
	"ActionText":"Add Jane Doe to the Doe family",
	"BusinessUnitID":2,
	"Category":"REQUEST",
	"CreatedDate":"2012-07-16T17:23:34Z",
	"EnterpriseID":5,
	"FromMemberID":124,
	"FromUsername":"Janedoe",
	"HasRead":false,
	"ID":231234,
	"IsActive":true,
	"Message":"Jane Doe has requested to join the Doe family.",
	"ModifiedDate":"2012-07-16T17:23:34Z",
	"Subject":"Family Member Join Request",
	"ToMemberID":123
}
```

## Cancel a Notification

Terminates a specific Notification object.

### URL
> POST /notification/v1/{id}/cancel

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
            <td>The notification id.</td>
        </tr>
    </tbody>
</table>

### Example

> POST http://localhost/rest/notification/v1/231234/cancel