# Resource Documentation

## Getting Started

* First [register a member](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#register-a-member) or [retrieve a token](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#retrieve-a-token) to get an oauth token to make resource requests with.
* All resource requests require an `oauth_token` in the request headers.

## [Member/v1](/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md)
<table>
    <thead>
        <tr>
            <th>Path</th>
            <th>HTTP Method</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>/member/v1/{id}</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#retrieve-a-member">Retrieve a Member</a></td>
        </tr>
		<tr>
            <td>/member/v1/me</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#retrieve-a-member">Retrieve a Member</a></td>
        </tr>
		<tr>
            <td>/member/v1/{id}</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#update-a-member">Update a Member</a></td>
        </tr>
		<tr>
            <td>/member/v1/me</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#update-a-member">Update a Member</a></td>
        </tr>
        <tr>
            <td>/member/v1/?index={index}&paging={paging}</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#retrieve-a-collection-of-members">Retrieve a collection of Members</a></td>
        </tr>
		<tr>
            <td>/member/v1/{id}/changepassword</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#change-password-for-a-member">Change password for a Member</a></td>
        </tr>
		<tr>
            <td>/member/v1/me/changepassword</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md#change-password-for-a-member">Change password for a Member</a></td>
        </tr>		
    </tbody>
</table>

## [Family/v1](/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md)
<table>
    <thead>
        <tr>
            <th>Path</th>
            <th>HTTP Method</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>/family/v1/{id}</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#retrieve-a-family">Retrieve a Family</a></td>
        </tr>
		<tr>
            <td>/family/v1/me</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#retrieve-a-family">Retrieve a Family</a></td>
        </tr>
		<tr>
            <td>/family/v1/{id}</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#update-a-family">Update a Family</a></td>
        </tr>
		<tr>
            <td>/family/v1/me</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#update-a-family">Update a Family</a></td>
        </tr>
        <tr>
            <td>/family/v1/?index={index}&paging={paging}</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#retrieve-a-collection-of-families">Retrieve a collection of Families</a></td>
        </tr>	
		<tr>
            <td>/family/v1/</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#create-a-family">Create a Family</a></td>
        </tr>		
		<tr>
            <td>/family/v1/{id}</td>
            <td>DELETE</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#delete-a-family">Delete a Family</a></td>
        </tr>
		<tr>
            <td>/family/v1/me</td>
            <td>DELETE</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#delete-a-family">Delete a Family</a></td>
        </tr>
		<tr>
            <td>/family/v1/{id}/member/{memberid}</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#add-a-member-to-a-family">Add a member to a family</a></td>
        </tr>
		<tr>
            <td>/family/v1/{id}/member/{me}</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#add-a-member-to-a-family">Add a member to a family</a></td>
        </tr>
		<tr>
            <td>/family/v1/{id}/members?index={index}&paging={paging}</td>
            <td>GET</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md#retrieve-a-collection-of-members-in-a-family">Retrieve a collection of Members in a Family</a></td>
        </tr>	
    </tbody>
</table>

## Current Releases

* Version 1 or `v1` 



