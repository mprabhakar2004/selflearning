* http://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
* http://blog.mwaysolutions.com/2014/06/05/10-best-practices-for-better-restful-api/
* https://blog.philipphauer.de/restful-api-design-best-practices/
* https://www.owasp.org/index.php/REST_Security_Cheat_Sheet


* HATEOUS :
* VERSIONING : prefer accept header rather than url ( some time people store url in database it would break)
* GET:
     - pagination
          - put link for next/prev/last/first etc
          - offset
          - limit
     - sorting
          - orderBy = fileds

* PUT :
     - Idempotent
     - Create/update
     - always send entire object (full update always)
     - can be cached
* POST:
     - Create
          - Always send location header in response for the created resource with status code 201
     - Partial update
     - Not idempotent
     - not cached 

* Date time representation standard in text : ISO 8601
     - timestamp : UTC format

* Status Code: 
    - 204 - Accepted for async/long lasting task
        - location header need to be set to poll the status
    - 401 : authnetication
    - 403 - authorisation 
* ERROR:
    - status, code, message, developerMessage, moreInfo (link to code)
    - 400 series status codes for client issues & 500 series status codes for server issues

* SECURITY:
     - no session i.e. authneticate every request ( basic over ssl/ apikey/ oauth token/ jwt etc)
     - https://blog.restcase.com/top-5-rest-api-security-guidelines/
     - https://blog.restcase.com/restful-api-authentication-basics/
     - https://stackoverflow.com/questions/4113934/how-is-oauth-2-different-from-oauth-1
     - https://www.youtube.com/watch?v=6VsGhLIkORQ
