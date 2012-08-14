# Auth Documentation

## Getting Started

* First [register a member](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#register-a-member) or [retrieve a token](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#retrieve-a-token) to get an oauth token to make resource requests with.
* All resource requests require an `oauth_token` in the request headers.

## [Auth/v1](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md)
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
            <td>/auth/v1/tokenrequest</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#retrieve-a-token">Retrieve a Token</a></td>
        </tr>
        <tr>
            <td>/auth/v1/tokenrefresh</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#refresh-a-token">Refresh a Token</a></td>
        </tr>
        <tr>
            <td>/auth/v1/registermember</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#register-a-member">Register a Member</a></td>
        </tr>        
		<tr>
            <td>/auth/v1/logoff</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#logoff">Logoff</a></td>
        </tr>
		<tr>
            <td>/auth/v1/passwordreset</td>
            <td>POST</td>
            <td><a href="/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md#password-reset">Password Reset</a></td>
        </tr>
    </tbody>
</table>

## Current Releases

* Version 1 or `v1` 

